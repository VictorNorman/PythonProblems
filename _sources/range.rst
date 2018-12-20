Range Function 
:::::::::::::::::::::::::::

.. question:: range1_q
   :number: 1

    .. tabbed:: range1_tabs

        .. tab:: Question

            .. activecode:: range1

               Replace ``<1>`` in the following code with a call to
	       ``range()`` so that the for loop prints out all integers from 1 to 10, inclusive.

               ~~~~
               for i in <1>:
                   print(i)
               ====

        .. tab:: Hint

           The ``range`` function takes 1, 2, or 3 integer parameters.  The
           parameters are ``range(start=0, stop, step=1)``.  If a ``start``
           value is not provided, the value ``0`` is used.  If a ``step``
           value is not provided, the value ``1`` is used. The ``stop``
           value indicates the upper limit that the result should be *less
           than*. E.g., if ``stop`` is ``10``, then the result of the
           ``range`` call will end at ``9``.

        .. tab:: Answer

           .. activecode:: range1_a
              :nocanvas:

              for i in range(1, 11):
                  print(i)
              
.. question:: range2_q

    .. tabbed:: range2_tabs

        .. tab:: Question

            .. activecode:: range2

               Replace ``<1>`` in the following code with a call to
	       ``range()`` so that the for loop prints out all integers from 0 to 99, inclusive.

               ~~~~
               for i in <1>:
                   print(i)
               ====

        .. tab:: Hint

           Remember that you can omit the first parameter if you want the
           result to start at 0.

        .. tab:: Answer

           .. activecode:: range2_a
              :nocanvas:

              for i in range(100):
                  print(i)

.. question:: range3_q

    .. tabbed:: range3_tabs

        .. tab:: Question

            .. activecode:: range3

               Replace ``<1>`` in the following code with a call to
	       ``range()`` so that the for loop prints out all integers from -10 to 10, inclusive.

               ~~~~
               for i in <1>:
                   print(i)
               ====

        .. tab:: Hint

           Parameters can be negative, and if ``step`` is one, the results
           will increase by 1 each time through the loop.

        .. tab:: Answer

           .. activecode:: range3_a
              :nocanvas:

              for i in range(-10, 11):
                  print(i)

.. question:: range4_q

    .. tabbed:: range4_tabs

        .. tab:: Question

            .. activecode:: range4

               Replace ``<1>`` in the following code with a call to
	       ``range()`` so that the for loop prints out all even
	       integers from 0 to 100, inclusive.

               ~~~~
               for i in <1>:
                   print(i)
               ====

        .. tab:: Hint

           Parameters can be negative, and if ``step`` is 1, the results
           will increase by 1 each time through the loop.

        .. tab:: Answer

           .. activecode:: range4_a
              :nocanvas:

              for i in range(0, 101, 2):
                  print(i)

.. question:: range5_q

    .. tabbed:: range5_tabs

        .. tab:: Question

            .. activecode:: range5

               Replace ``<1>`` in the following code with a call to
	       ``range()`` so that the for loop prints out all multiples of 5
	       from 0 to 200, inclusive.

               ~~~~
               for i in <1>:
                   print(i)
               ====

        .. tab:: Hint

           Go back and review previous questions if you need a hint.

        .. tab:: Answer

           .. activecode:: range5_a
              :nocanvas:

              for i in range(0, 201, 5):
                  print(i)

.. question:: range6_q

    .. tabbed:: range6_tabs

        .. tab:: Question

            .. activecode:: range6

               Replace ``<1>`` in the following code with a call to
	       ``range()`` so that the for loop prints out all integers
	       from 10 down to 1, inclusive.

               ~~~~
               for i in <1>:
                   print(i)
               ====

        .. tab:: Hint

           Provide a step of ``-1``.

           ``range()`` produces values down to but not equal
           to or less than the ``stop`` value, if the step is negative.           
           

        .. tab:: Answer

           .. activecode:: range6_a
              :nocanvas:

              for i in range(10, 0, -1):
                  print(i)

.. raw:: html

   <div style='display:none;'>

.. activecode:: range1_pre

   groceries = ['milk', 'bread', 'eggs', 'chocolate (dark)', 'oatmeal']

.. raw:: html

   </div>

.. question:: range7_q

    .. tabbed:: range7_tabs

        .. tab:: Question

            .. activecode:: range7
               :include: range1_pre

               Integers are used as indices into sequences, like lists and
               strings. So, if you want to access each element in a
               sequence at a certain index, you need to use a ``for`` loop
               to iterate over each index appropriate for indexing the
               sequence.

               To get the indices appropriate for indexing a sequence, use
               ``range(len(sequence))``. 

               Replace ``<1>`` in the following code with a call to
	       ``range(len(sequence))`` so that the for loop prints out all indices
	       useful for indexing into the sequence ``groceries``.

               ~~~~
               for idx in <1>:
                   print(idx)
               ====

        .. tab:: Hint

           ``len(groceries)`` returns the number of items in the sequence.

        .. tab:: Answer

           .. activecode:: range7_a
              :nocanvas:
              :include: range1_pre

              for idx in range(len(groceries)):
                  # print out the index for this item in the groceries list.
                  print(idx)
              
.. question:: range8_q

    .. tabbed:: range8_tabs

        .. tab:: Question

            .. activecode:: range8
               :include: range1_pre

               Replace ``<1>`` in the following code with a call to
	       ``range(len(sequence))`` so that the for loop uses indexes
	       useful for indexing into the sequence ``groceries``.

               Replace ``<2>`` with code to access the value in sequence
               ``groceries`` at index ``idx``.

               Your resulting code should print each item in the ``groceries``
               list, regardless of how long the ``groceries`` list is.

               ~~~~
               for idx in <1>:
                   print(<2>)
               ====

        .. tab:: Hint

           ``len(groceries)`` returns the number of items in the sequence.

        .. tab:: Answer

           .. activecode:: range8_a
              :nocanvas:
              :include: range1_pre

              for idx in range(len(groceries)):
                  print(groceries[idx])
              
.. question:: range9_q

    .. tabbed:: range9_tabs

        .. tab:: Question

            .. activecode:: range9
               :include: range1_pre

               Replace ``<1>`` in the code so that the for loop prints each
	       item *except the last* in the list ``groceries``.

               ~~~~
               for idx in <1>:
                   print(groceries[idx])
               ====

        .. tab:: Hint

           ``len(groceries)`` returns the number of items in the sequence,
           but we want to access all items except the last one, so subtract
           one from that value.

        .. tab:: Answer

           .. activecode:: range9_a
              :nocanvas:
              :include: range1_pre

              for idx in range(len(groceries) - 1):
                  print(groceries[idx])
              
.. question:: range10_q

    .. tabbed:: range10_tabs

        .. tab:: Question

            .. activecode:: range10
               :include: range1_pre

               Replace ``<1>`` in the code so that the for loop prints each
	       item *except the first and the last* in the list ``groceries``.

               ~~~~
               for idx in <1>:
                   print(groceries[idx])
               ====

        .. tab:: Hint

           To skip the first item, start with index ``1``, not the default
           of ``0``.

           ``len(groceries)`` returns the number of items in the sequence,
           but we want to access all items except the last one, so subtract
           one from that value.

        .. tab:: Answer

           .. activecode:: range10_a
              :nocanvas:
              :include: range1_pre

              for idx in range(1, len(groceries) - 1):
                  print(groceries[idx])
