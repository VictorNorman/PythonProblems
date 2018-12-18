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
               # replace this comment with your code
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
               # replace this comment with your code
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
               # replace this comment with your code
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
               # replace this comment with your code
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
               # replace this comment with your code
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
               every other letter  -- i.e., the letters with indices
               which are even.  That is, only the 0th, 2nd, 4th, etc., letters.
               ~~~~
               # replace this comment with your code
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
               # replace this comment with your code
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
               # replace this comment with your code
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

.. raw:: html

   <div style='display:none;'>

.. activecode:: for9_pre

   numbers = [ 44, 3, 12, 22, 71, 47.3, 99.22, 105.1, 3, 7]

.. raw:: html

   </div>

.. question:: for9_q

    .. tabbed:: for9_tabs

        .. tab:: Question

            .. activecode:: for9
               :include: for9_pre

               Given a list ``numbers``, write code to print ``Found it!`` if
               the list contains the number 7. Do not use the ``in`` operator.  Use a for loop,
               with an if statement in it.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use item-based iteration.  Put a simple if statement in the for loop.

        .. tab:: Answer

           .. activecode:: for9_a
              :nocanvas:
              :include: for9_pre

              for num in numbers:
                  if num == 7:
                      print("Found it!")

.. raw:: html

   <div style='display:none;'>

.. activecode:: for10_pre

   numbers = [ 44, 3, 12, 22, 71, 47.3, 99.22, 105.1, 3, 7, 50]

.. raw:: html

   </div>

.. question:: for10_q

    .. tabbed:: for10_tabs

        .. tab:: Question

            .. activecode:: for10
               :include: for10_pre

               Given a list ``numbers``, write code to create two lists, ``bignums`` and ``littlenums``,
               by adding each number in ``numbers`` to ``bignums`` if it is greater than 50, and adding
               all the other numbers to ``littlenums``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(littlenums) + len(bignums), len(numbers))
                      self.assertTrue(50 in littlenums, "50 should be in littlenums")
                      self.assertEqual(len(littlenums), 8)
                      self.assertTrue(99.22 in bignums)
               myTests().main()


        .. tab:: Hint

           Create the resulting lists before the for loop.

           Use item-based iteration with an if-else in it.

        .. tab:: Answer

           .. activecode:: for10_a
              :nocanvas:
              :include: for10_pre

              bignums = []
              littlenums = []
              for num in numbers:
                  if num > 50:
                      bignums.append(num)
                  else:
                      littlenums.append(num)

.. raw:: html

   <div style='display:none;'>

.. activecode:: for11_pre

   class Block:
       def __init__(self, x, y):
           pass

.. raw:: html

   </div>

.. question:: for11_q

    .. tabbed:: for11_tabs

        .. tab:: Question

            .. activecode:: for11
               :include: for11_pre

               This code was recently seen in a project:

               ``block_list = [Block(20,20), Block(20,60), Block(20,100), Block(20,140), Block(20,180), Block(60,20), Block(60,60), Block(60,100), Block(60,140), Block(60,180), Block(100,20), Block(100,60), Block(100,100), Block(100,140), Block(100,180), Block(140,20), Block(140,60), Block(140,100), Block(140,140), Block(140,180), Block(180,20), Block(180,60), Block(180,100), Block(180,140), Block(180,180), Block(220,20), Block(220,60), Block(220,100), Block(220,140), Block(220,180),Block(260,20), Block(260,60), Block(260,100), Block(260,140), Block(260,180), Block(300,20), Block(300,60), Block(300,100), Block(300,140), Block(300,180), Block(340,20), Block(340,60), Block(340,100), Block(340,140), Block(340,180), Block(380,20), Block(380,60), Block(380,100), Block(380,140), Block(380,180), Block(420,20), Block(420,60), Block(420,100), Block(420,140), Block(420,180), Block(460,20), Block(460,60), Block(460,100), Block(460,140), Block(460,180), Block(500,20), Block(500,60), Block(500,100), Block(500,140), Block(500,180), Block(540,20), Block(540,60), Block(540,100), Block(540,140), Block(540,180), Block(580,20), Block(580,60), Block(580,100), Block(580,140), Block(580,180), Block(620,20), Block(620,60), Block(620,100), Block(620,140), Block(620,180), Block(660,20), Block(660,60), Block(660,100), Block(660,140), Block(660,180), Block(700,20), Block(700,60), Block(700,100), Block(700,140), Block(700,180)]``

               Rewrite this code to use a doubly-nest for loop.
               ~~~~
               block_list = []
               # add your code below
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(block_list), 90)
               myTests().main()


        .. tab:: Hint

           Create the resulting list before the for loops.

           Create a for loop to iterate from 20 to 700, by 40s.

           Inside the first for loop, write a for loop to iterate from 20 to 180 by 40s.

           Inside that for loop, call the ``Block()`` call, and append the result to your ``block_list``.

        .. tab:: Answer

           .. activecode:: for11_a
              :nocanvas:
              :include: for11_pre

              block_list = []
              for vert in range(20, 701, 40):
                  for horiz in range(20, 181, 40):
                      block_list.append(Block(vert, horiz))





