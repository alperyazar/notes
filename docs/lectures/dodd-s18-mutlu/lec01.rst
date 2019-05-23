Lecture 01 - Introduction and Basics
====================================

Info
----

* `Video Link <http://www.youtube.com/watch?v=PMJxcArLU1E>`__
* `Lecture Slides <https://safari.ethz.ch/digitaltechnik/spring2018/lib/exe/fetch.php?media=digitaldesign-s18-lecture1-intro.pdf>`__

Reading
-------

* [jouppi2017datacenter]_
* Chapter 1 in [harris2012digital]_
* Chapter 1-2 in [patt2005introduction]_
* `Binary Numbers <https://safari.ethz.ch/digitaltechnik/spring2018/lib/exe/fetch.php?media=reading-week1_binarynumbers.pdf>`__ (`Done`)
* [hamming1986you]_ (`Done`)
* [hamming2012numerical]_
* [hamming1950error]_

Reading Notes
^^^^^^^^^^^^^

Binary Numbers
""""""""""""""

Basic stuff..

.. todo::

    Expand notes on number representation, possibly on separate page.

Lecture Minutes
---------------

* **29:00** Importance of principled design

* **40:00** "architecture based upon principle not upon precedent"
  Precedent means examples from past. Design should have some principles and
  shouldn't build blindly on past or wide spread approaches. For example, let's
  consider Spectre and Meltdown. In those cases, precedent is building a fast
  processor. But designer might have considered security principle to avoid
  this kind of flaws.

* **44:00** Although technology changes over time, fundamental techniques and
  principles may remain similar.

* **48:00** Mini talk about :term:`systolic array` although it is kind of
  out of context.

* **01:03:00** Electrons → Transistors → Logic Gates →
  Combinational Logic Circuits →
  Sequential Logic Circuits (Storage Elements and Memory) → … →
  Cores → Caches → Interconnect → Memories → …

* **01:13:00** The transformation hierarchy is shown below. How can we talk
  with electrons? This is a fundamental question.

  .. figure:: images/l01-layers.png
     :align: center

     *Taken directly from the lecture notes. © belongs to Prof. Mutlu*

* **01:15:00** :term:`algorithm` is defined.

  .. figure:: images/l01-isa.png
     :align: center

     *Taken directly from the lecture notes. © belongs to Prof. Mutlu*

  See :term:`ISA` and :term:`microarchitecture` definitions.

* **01:24:00** VAX architecture, 3D array checking at hardware (?)

  .. todo::

    What are they? 3D array checking?

Glossary
--------

.. glossary::

    algorithm
        Algorithm is step-by-step procedure that is guaranteed to
        terminate where each step is precisely stated and can be carried out
        by a computer

    ISA
        **Instruction Set Architecture**. It is a contract between Hardware
        and Software. It is programmers assumption about hardware.

    microarchitecture
        An implementation of the :term:`ISA`.

    systolic array
        It looks like a type of parallel processing architecture. It is used
        by Google Tensor. It is a memory bandwidth efficient architecture.
        https://www.geeksforgeeks.org/parallel-processing-systolic-arrays/

        .. todo::

            I may not have fully understood.

.. sectionauthor:: Alper Yazar
