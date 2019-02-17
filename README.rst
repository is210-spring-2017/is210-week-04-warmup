####################
IS 210 Assignment 04
####################


:College: CUNY School of Professional Studies
:Course-Name: Software Application Programming I
:Course-Code: IS 210

Overview
========

In this assignment, we'll focus on the construction of basic functions. The
functions we create will be intentionally simple to make it easier to isolate
the task at hand.

Instructions
============

.. important::

    In these exercises, you may, on occasion, come across a task that requres
    you to research or use a function or method not directly covered by the
    course text. Since Python is such a large language it would be impossible
    for the author to have included descriptions of each and every available
    function which would largely duplicate the offical Python documentation.

    A *vital* skill to successful programming is being comfortable searching
    for and using official language documentation sources like the
    `Python String Documentation`_ page. Throughout our coursework we will be
    practicing both the use of the language in practice and the search skills
    necessary to become functional programmers.

Tasks
============

Task 01
-------

In this task, you'll be defining a function with three parameters.

Specifications
^^^^^^^^^^^^^^

1.  Open a new Jupyter notebook 

2.  Define a new function named ``too_many_kittens`` that takes three
    arguments, in order:

    1.  kittens, the number of kittens

    2.  litterboxes, the (integer) number of available litterboxes

    3.  catfood, a boolean representing whether or not any catfood exists

3.  In the function return the value of the following comparison statement:

    .. code:: python

        not (litterboxes >= kittens and catfood)

    This statement ensures we have at least one litterbox for each kitten and
    that we have some catfood. It then uses inversion via ``not`` to answer
    whether or not we have too many kittens.

.. note::

    Note the spacing of the ``not`` operator. There should always be spacing
    around all logical operators like ``and``, ``not`` or ``or``. Without it,
    ``not`` would look like a function, eg ``not()``.

..  note::

    A fun fact of the polymorphic properties of python is the fact that
    truthiness would allow ``catfood`` to either be a boolean (eg, ``True``) or
    some number like ``0`` or even ``None`` and this would continue to operate
    in a reasonably sane manner.

Expected Output
^^^^^^^^

.. code:: pycon

    >>> too_many_kittens(12, 12, False)
    True
    
    >>> too_many_kittens(13, 12, True)
    True

    >>> too_many_kittens(12, 13, True)
    False

Task 05
-------

Here we'll set a default value in our function definition.

Specifications
^^^^^^^^^^^^^^

1.  Keep working on the same notebook

2.  Create a new function named ``defaults`` with two parameters:
    
    1.  ``my_optional`` which has a default value of True

    2.  ``my_required`` which is a required param and has no default value

3.  Return the following logical comparison:

    .. code:: python

        my_optional is my_required

Expected Output
^^^^^^^^

.. code:: pycon

    >>> defaults(True)
    True

    >>> defaults(True, False)
    False

    >>> defaults(False, False)
    True



Submission
==========

Code should be submitted via Blackboard as a single Jupyter notebook file.

In order to receive full credit you must complete the assignment as-instructed and without any violations (reported in the build status).

.. _GitHub: https://github.com/
.. _Python String Documentation: https://docs.python.org/2/library/stdtypes.html
