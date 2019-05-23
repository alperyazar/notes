.. _lec_dood_s18_lec02_page:

Lecture 02 - Mysteries in Comp Arch
===================================

Info
----

* `Video Link <http://www.youtube.com/watch?v=_D0D0m2fBks>`__
* `Lecture Slides <https://safari.ethz.ch/digitaltechnik/spring2018/lib/exe/fetch.php?media=onur-digitaldesign-2018-lecture2-mysteries-afterlecture.pdf>`__

Reading
-------

* [klaiber2000technology]_
* [dehnert2003transmeta]_
* [horn2018reading]_
* [kim2014flipping]_
* [seaborn2015exploiting]_
* [gruss2016rowhammer]_
* [van2016drammer]_
* [lamport1982byzantine]_
* [mutlu2017rowhammer]_

Reading Notes
^^^^^^^^^^^^^

Lecture Minutes
---------------

* **05:17** User-centric view of "transformations". Entire stack should be
  optimized for the user. But there are many users with different expectations
  from a computer. Also some users write OS and some of them write algorithms.
  User also interacts with computer with different levels.

    .. figure:: images/l02-user_view_of_stack.png
        :align: center

        *Taken directly from the lecture notes. © belongs to Prof. Mutlu*

* **07:15** :term:`abstraction` is defined. Programmer doesn't need to know
  details of processor because it is abstracted by many levels. Abstraction
  improves productivity. Then why worry about details?

* **13:00** If you know details of a processor, you can write better programs.
  As long as everything is OK, no need to dive in details. But what if program
  runs slow? not correct results? energy hungary? security? efficiency?
  From hardware
  designer perspective, if designer doesn't know what a programmer expects from
  a processor he/she design a processor which is very hard to program. Designer
  needs to know software perspective to implement right primitives.

* **15:00** As an example, **IBM Cell Broadband Engine** was the first
  heterogenous multi-core processor. Beautiful design but missing cache
  coherency in hardware. So, it was very hard to program.

* **16:40** Another example: **Transmeta**. They tried to compete with Intel.
  They wanted to design x86 processor. They wrote a software translation layer
  which takes x86 code and translates to a code for the internal
  microarchitecture (:term:`VLIW` type) that is simpler than x86. Why? Because
  implementing an efficient x86 ISA microarchitecture isn't a trivial thing
  especially for a small, startup company. They chose to design
  very fast
  internal microarchitecture but they needed an efficient translation layer.
  Notice that translation layer is a software. But the bottleneck was that
  layer. In the end, they failed racing. Read [klaiber2000technology]_
  and [dehnert2003transmeta]_.

* **23:10** Course goals: 1) How processor works underneath. 2) Making design
  and optimizations.

* **24:10** Mysteries

* **25:10** **Meltdown** and **Spectre**. Someone can steal secret data
  even though no software bugs, hardware behaves according to specifications.
  But why this happens? These are hardware security vulnerabilities that
  affects almost all modern processors. :term:`speculative execution` is the
  main cause (I mean main "trigger"). You predict code and do something. If
  you realize that prediction was wrong, you undo. For example you may prefer
  it in an `if` statement if accessing the control variable takes many cycles.
  You assume a result, go on then when access is completed you check your
  assumption. But processor operates this mechanism such that it obeys
  programmers assumption about processor like sequential execution and ISA.
  Programmers aren't interested in microarchitecture. In these flaws, processor
  leaks data due to this mechanism. With help of caching, attacker may
  guess processor state about speculative execution. Processor brings data
  which should not be accessed if there is no speculative execution
  into cache due to speculative execution. Attacker can inspect the contents
  of the cache to "sniff" secret data (by measuring how long it takes to access
  the data). It is also possible to execute another
  program by abusing flaws. They are sophisticated attacks.

* **38:30** Processor cache is a :term:`side channel`.

* **41:30** :term:`branch prediction` is mentioned.

* **42:45** Read: [horn2018reading]_

* **43:00** If you don't "cross layers", you can't detect and fix the problem
  in case of Meltdown and Spectre. You can't create an another attack.

* **45:45**

    .. figure:: images/l02-meltdown_spectre_solution_stack.png
        :align: center

        *Taken directly from the lecture notes. © belongs to Prof. Mutlu*

* **46:30**

    .. figure:: images/xkcd-meltdown_and_spectre.png
        :align: center

        *https://xkcd.com/1938/ © belongs to XKCD*

* **48:30** Design goal of a system determines the design mindset and
  evaluation metrics. Design goal of cutting edge processors is a reason of
  Meltdown and Spectre. But security is not main design goal.

* **50:30** Other course goals: Think Critically, Think Broadly.

* **51:10** Videos about Meltdown and Spectra:
  https://www.youtube.com/watch?v=syAdX44pokE
  https://www.youtube.com/watch?v=mgAN4w7LH2o

* **52:50** **RowHammer** DRAM Disturbance Error. It is a story of how a simple
  hardware failure mechanism can create a widespread system security
  vulnerability. Reading a row in DRAM disturb adjacent rows. It is also
  possible in SSDs or HDDs, etc. When you want to read a row in memory, you
  apply high voltage to it. After reading, you apply low voltage. If you
  repeat this in most DRAM chips you get errors in adjacent rows. Notice that
  corruption is triggered by only reading adjacent rows. You hammer row by
  reading.

* **57:30** It is interesting that this flaw is observed chips manufactured
  after ~2010. More recent chips have higher error rates. This is because
  physical decrease in distance between rows, similar to Moore's Law.

* **58:15** DRAM cells are too close to each other. Actually they are not
  completely electrically isolated from each other. Another term is
  cell-to-cell coupling. Some cells are more vulnerable than other cells.
  DRAM memory store information as charge. You can drain charge with this
  attack.

* **1:01:30** Some implementation details about RowHammer, assembly codes.

* **1:03:30** Read [kim2014flipping]_ and [seaborn2015exploiting]_

* **1:04:30** [seaborn2015exploiting]_ gained root access on a Linux system
  by exploiting RowHammer.

* **1:09:10** [gruss2016rowhammer]_

* **1:09:30** [van2016drammer]_ Hammer and root millions of Androids

* **1:10:00** How can we fix? Better DRAM chips (cost), refresh frequently
  (power, performance), sophisticated error correction (cost, power), access
  counter (a method of detecting attack but cost, power, complexity)

* **1:14:00** https://support.apple.com/en-gb/HT204934 is Apple solution to
  problem. They refresh whole memory more frequently but it will increase
  power consumption.

* **1:15:25** **PARA**: Probabilistic Adjacent Row Activation is a cheaper
  solution to RowHammer problem. Key idea: After closing a row, with some
  probability (probably low value like 0.005) you refresh its neighbors.

* **1:17:45** RowHammer also shows that one should be able to "cross layers"
  to understand, fix or repeat the problem.

* **1:19:35** These are example of :term:`byzantine failures`. Read
  [lamport1982byzantine]_

* **1:24:05** [mutlu2017rowhammer]_

Glossary
--------

.. glossary::

    abstraction
        A higher level only needs to know about the interface to the lower
        level, not how the lower level is implemented.

    branch prediction
        A way of "guessing" mentioned in :term:`speculative execution`.

    byzantine failures
        They are characterized by undetected erroneous computation (
        opposite of fail fast (with an error or no result)). They are "sneaky"
        errors. "erroneous" can be "malicious" because one can abuse it. They
        are very difficult to detect and confine. It is a real problem in
        distributed systems (may be like blockcahin :)). Avoidance is the best
        solution.
        [lamport1982byzantine]_

    side channel
        A channel through which someone sophisticated can extract information.

    speculative execution
        Doing something before you know what it is needed. If you realize that
        it is not needed after some time, you revert. In overall, this saves
        time and improves performance.

    VLIW
        Very Long Instruction World. A type of architecture.

.. index::
    double-sided RowHammer
    IBM Cell Broadband Engine
    meltdown
    PARA
    RowHammer
    spectre
    Transmeta

.. sectionauthor:: Alper Yazar
