For Loops
:::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: for1_pre

   groceries = ['milk', 'bread', 'eggs', 'chocolate (dark)']

.. raw:: html

   </div>

.. question:: for1_q
   :number: 1

    .. tabbed:: for1_tabs

        .. tab:: Question

            .. activecode:: for1
               :include: for1_pre

               Assume a variable ``groceries`` has been defined to be a
               list of grocery items.

               Write code to print out each item on its own line.

               ~~~~
               # replace this comment with your if statement
               ====

        .. tab:: Hint

           The for loop pattern is:

           ``for item in list:``

               ``loop-body``

        .. tab:: Answer

           .. activecode:: for1_a
              :nocanvas:
              :include: for1_pre

              for item in groceries:
                  print(item)
              
.. question:: for2_q

    .. tabbed:: for2_tabs

        .. tab:: Question

            .. activecode:: for2
               :include: for1_pre

               Assume a variable ``groceries`` has been defined to be a
               list of grocery items.

               Write code to print out all items in the list on separate
               lines, prefixed by the number of the item in the list.
               E.g.,

               1. milk
               2. eggs
               3. chips

               ~~~~
               # replace this comment with your if statement
               ====

        .. tab:: Hint

           You will have to use an index-based loop, with
           ``range(len(groceries))`` and indexing groceries as ``groceries[idx]``.

        .. tab:: Answer

           .. activecode:: for2_a
              :nocanvas:
              :include: for1_pre

              for idx in range(len(groceries)):
                  print(str(idx + 1) + '. ' + groceries[idx])

.. question:: for3_q

    .. tabbed:: for3_tabs

        .. tab:: Question

            .. activecode:: for3
               :include: for1_pre

               Assume a variable ``groceries`` has been defined to be a
               list of grocery items.

               Write code to print out all items in the list on a single
               line, separated by commas.  It is OK to have a comma after
               the last item.

               ~~~~
               # replace this comment with your if statement
               ====

        .. tab:: Hint

           Remember that you can use ``print(..., end='')`` to keep the cursor
           on the same line.

        .. tab:: Answer

           .. activecode:: for3_a
              :nocanvas:
              :include: for1_pre

              for item in groceries:
                  print(item, end=', ')
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: for4_pre

   n = 10

.. raw:: html

   </div>

.. question:: for4_q

    .. tabbed:: for4_tabs

        .. tab:: Question

            .. activecode:: for4
               :include: for4_pre

               Write a for loop to sum up all numbers from 0 to ``n - 1`` into
               a variable ``sum``.  Assume ``n`` is already defined.

               ~~~~
               # replace this comment with your if statement
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(sum, 45)
               myTests().main()

        .. tab:: Hint

           Your code should have this format:

           * initialize sum to 0.
           * for loop, using ``range``.
           	* add the value to sum

        .. tab:: Answer

           .. activecode:: for4_a
              :nocanvas:
              :include: for4_pre

              sum = 0
              for num in range(0, n):
                  sum = sum + num
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: for5_pre

   name = 'Abraham Lincoln'

.. raw:: html

   </div>

.. question:: for5_q

    .. tabbed:: for5_tabs

        .. tab:: Question

            .. activecode:: for5
               :include: for5_pre

               Write a for loop to print out each letter in a str ``name``
               on one line with a space between.
               ~~~~
               # replace this comment with your if statement
               ====

        .. tab:: Hint

           A string is iterable, so you can use it right in the for loop:

           e.g.,

           ``for char in str:``


        .. tab:: Answer

           .. activecode:: for5_a
              :nocanvas:
              :include: for5_pre

              for char in name:
                  print(char, end=' ')

.. raw:: html

   <div style='display:none;'>

.. activecode:: for6_pre

   name = 'Abraham Lincoln'

.. raw:: html

   </div>

.. question:: for6_q

    .. tabbed:: for6_tabs

        .. tab:: Question

            .. activecode:: for6
               :include: for6_pre

               Write a for loop to iterate over a string ``name`` and print
               every other letter  -- i.e., on the letters with indices
               which are even.  That is, only the 0th, 2nd, 4th, etc., letters.
               ~~~~
               # replace this comment with your if statement
               ====

        .. tab:: Hint

           Use an index-based loop, since you will need to know if you are
           looking at an even or odd index.

           Use an if statement in the for loop to determine if the index is even.

        .. tab:: Answer

           .. activecode:: for6_a
              :nocanvas:
              :include: for6_pre

              for idx in range(len(name)):
                  if idx % 2 == 0:
                      print(name[idx])

.. question:: for7_q

    .. tabbed:: for7_tabs

        .. tab:: Question

            .. activecode:: for7

               Write code to create a list ``rands`` that contains
               20 random numbers from 0 to 100 inclusive.
               ~~~~
               from random import randint
               # replace this comment with your if statement
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(rands), 20)
                      for item in rands:
                          self.assertTrue(item >= 0 and item <= 100)
               myTests().main()

        .. tab:: Hint

           Above the for loop, create the variable ``rands`` to be an empty list.

           Call ``randint(0, 100)`` to get random integers from 0 to 100,
           inclusive.

           Use ``append()`` to add a random number to the list.

           Use ``range(20)`` to iterate 20 times.

        .. tab:: Answer

           .. activecode:: for7_a
              :nocanvas:

              from random import randint
              rands = []
              for idx in range(20):
                  rands.append(randint(0, 100))


.. question:: for8_q

    .. tabbed:: for8_tabs

        .. tab:: Question

            .. activecode:: for8

               Write a for loop to create a list ``tenths`` containing
               numbers 0.0, 0.1, 0.2, 0.3, 0.4, ..., 9.9
               ~~~~
               # replace this comment with your if statement
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(tenths), 100)
                      self.assertAlmostEqual(tenths[0], 0.0)
                      self.assertAlmostEqual(tenths[99], 9.9)
                      self.assertAlmostEqual(tenths[50], 5.0)
               myTests().main()

        .. tab:: Hint

           Above the for loop, create the variable ``tenths`` to be an empty list.

           There will be 100 numbers in the list, so use ``range(100)`` to iterate 100 times.

        .. tab:: Answer

           .. activecode:: for8_a
              :nocanvas:

              tenths = []
              for i in range(100):
                  tenths.append(i / 10)

