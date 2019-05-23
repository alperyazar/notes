.. _lec_dood_s18_lec05_page:

Lecture 05 - Combinational Logic
==============================================

Info
----

* `Video Link <https://www.youtube.com/watch?v=6rpxEQQg01E>`__
* `Lecture Slides <https://safari.ethz.ch/digitaltechnik/spring2018/lib/exe/fetch.php?media=onur-digitaldesign-2018-lecture5-combinational-logic-afterlecture.pdf>`__

Reading
-------

* Chapter 2 in [harris2012digital]_
* Chapter 4 until 4.3 and 4.5 in [harris2012digital]_
* Chapter 3 until 3.3 in [patt2005introduction]_
* [moore1965cramming]_
* [dennard1974design]_
* [boole1847mathematical]_

Reading Notes
^^^^^^^^^^^^^

Lecture Minutes
---------------

* **02:00** Video assignment: `Onur Mutlu - Future Computing Architectures - ETH Zurich Inaugural Lecture (May 15, 2017) <https://www.youtube.com/watch?v=kgiZlSOcGFM>`__
* **04:00** Bloom filter recall, it was mentioned :ref:`there <lec_dood_s18_lec04_page>`.
* **14:00** Bloom filter advantages and disadvantages. Bloom filters are also
  used by search engines. 
* **16:45** Bloom filters never overflow unlike fixed-size tables. You can
  insert new elements without increasing storage space. However this will
  increase false positive rate likely. It is scalable.
* **20:00** Takeaways: This field has probably
  many challenging and exciting problems that no one has attacked. It is driven
  by huge hunger for data and its analysis ("Big data"). We can easily collect
  more data than we can analyze/understand. Field is driven by significant
  difficulties. Three walls: **energy, reliability, complexity**.
* **22:30** *Dream and they will come*.
* **24:00** A memory access consumes ~1000x the energy of a complex addition.
  Communication Dominates Arithmetic (Daily, HiPEAC 2015).
* **35:30** Three key components of a computer: computation, communication and
  storage (memory).
* **39:45** Differences between microprocessors, FPGAs, ASICs.
* **42:30** Introduction to transistors. Today processors have transistors
  at billion scale.
* **43:40** MOS Transistor: Conductors (Metal), Insulators (Oxide)
  Semiconductors. It is controlled switch. N and P types are mentioned.
* **51:00** Logic gates.
* **51:34** CMOS technology = nMOS + pMOS. C stands for complementary.
* **52:50** Gender neutrality in Turkish :). "Haklısınız hocam :)"
* **54:00** Operation of a simple CMOS inverter.
* **1:00:11** CMOS NAND gate.
* **1:05:30** NAND gate is "logically complete". You can build any logic just
  only using NAND gates.

  .. note ::
    
    Note that AND gate doesn't have this property. You can't invert using AND.
    NAND and NOR are functionally complete.

* **1:06:00** CMOS AND gate. AND gate is more complicated than NAND in terms of
  number of transistors.
* **1:07:00** General CMOS structure has PMOS transistors connected to VCC and
  the output. It works as pull-up network. NMOS transistors are connected to
  GND and form a pull-down network.
* **1:08:40** Common logic gates.
* **1:10:45** :term:`Moore's Law` is mentioned.
* **1:13:44** :term:`Dennard scaling` is mentioned.
* **1:15:00** What is the limit on transistor size? We don't know!
* **1:15:45** Heat is a real problem in computer design.
* **1:17:45** :term:`functional specification` and :term:`timing specification`
  are defined.
* **1:18:15** Combinational logic is memoryless. It doesn't remember anything.
  Some books call Combinatorial Logic. Sequential Logic has memory.
* **1:19:00** :term:`functional specification` and examples. First example:
  full 1-bit adder.
* **1:21:50** Simple equations: NOT / AND / OR.
* **1:22:20** [boole1847mathematical]_ is mentioned.
* **1:23:07** Axioms of Boolean Algebra
* **1:24:45** Duality in Boolean Algebra. All the axioms come in dual form.
  This form can be derived by replacing: every AND with OR, every OR with AND,
  every 1 to 0, every 0 to 1 BUT don't change any literals or play with
  complements.
* **1:25:50** Some useful Boolean Algebra laws.

Glossary
--------

.. glossary::

    Dennard scaling

        From Wikipedia: "Originally formulated for MOSFETs, it states, roughly,
        that as transistors get smaller, their power density stays constant, so
        that the power use stays in proportion with area; both voltage and
        current scale (downward) with length" and "Therefore, in every
        technology generation the transistor density doubles, the circuit
        becomes 40% faster, and power consumption (with twice the number of
        transistors) stays the same." See: [dennard1974design]_

    functional specification

        Describes relationship between inputs and outputs

    Moore's Law

        See: [moore1965cramming]_ Moore is one of founders of Intel. He says
        that component on a chip counts double every other year. Some says
        that interval is 18 months. Key idea is a fixed interval. Size of
        transistor is shrinking so we can put more on a chip. Also cost of
        per circuit varies. We can say that rule was still valid until 2016.
        (I don't mean that this is invalid since 2016. That was the data
        shown given on the slides)

    timing specification

        Describes the delay between inputs changing and outputs responding

.. index::
    Placheolder


.. sectionauthor:: Alper Yazar
