Basic Function Definitions
:::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: bfunc1_pre

   groceries = ['milk', 'bread', 'eggs', 'chocolate (dark)']

.. raw:: html

   </div>

.. question:: bfunc1_q
   :number: 1

    .. tabbed:: bfunc1_tabs

        .. tab:: Question

            .. activecode:: bfunc1

               Define a function ``greet()`` that receives a string ``name`` as a parameter and
               prints ``Hi,`` followed by the value of ``name``.  E.g., if ``name`` is
               "Georgia", it prints ``Hi, Georgia``.

               The function returns nothing.
               ~~~~
               ====
               greet('Georgia')
               greet('Victor')

        .. tab:: Hint

           A function definition starts with ``def`` and then the name of the function.
           The contents (or "body") of the function is indented.

        .. tab:: Answer

           .. activecode:: bfunc1_a
              :nocanvas:

              def greet(name):
                  print("Hi, " + name)

.. question:: bfunc2_q

    .. tabbed:: bfunc2_tabs

        .. tab:: Question

            .. activecode:: bfunc2

               Define a function ``greet()`` that receives a string ``name`` as a parameter and
               *returns* ``Hi,`` followed by the value of ``name``.  (Note: the previous question
               had the code *print* the result. Here you should *return* the result.)

               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(greet('Georgia'), "Hi, Georgia")
                     self.assertEqual(greet('Victor'), "Hi, Victor")
                     self.assertEqual(greet(''), "Hi, ")
               myTests().main()

        .. tab:: Hint

           Build the string and then return it.  You can assume that the parameter ``name`` is a string.  The test cases are:
           ::

             greet('Susan')		# returns "Hi, Susan"
             greet('James')             # returns "Hi, James"
             greet('')                  # returns "Hi, "

        .. tab:: Answer

           .. activecode:: bfunc2_a
              :nocanvas:

              def greet(name):
                  return "Hi, " + name

.. question:: bfunc3_q

    .. tabbed:: bfunc3_tabs

        .. tab:: Question

            .. activecode:: bfunc3

               Define a function ``add()`` that receives two numbers and returns the sum of the numbers.
               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(add(1, 2), 3)
                     self.assertAlmostEqual(add(1.5, 2.0), 3.5)
                     self.assertEqual(add(-1, 1), 0)
               myTests().main()

        .. tab:: Hint

           The function *prints* nothing.  It returns the sum of the two values passed in.
           
           The test cases are:
           ::

             add(1, 2)             # returns 3
             add(1.5, 2.0)         # returns 3.5
             add(-1, 1)            # returns 0

        .. tab:: Answer

           .. activecode:: bfunc3_a
              :nocanvas:

              def add(num1, num2):
                  return num1 + num2

.. question:: bfunc4_q

    .. tabbed:: bfunc4_tabs

        .. tab:: Question

            .. activecode:: bfunc4

               Define a function ``add()`` that receives two numbers and returns the value
               that is 100 more than the sum of the two numbers.
               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(add(1, 2), 103)
                     self.assertAlmostEqual(add(1.5, 2.0), 103.5)
                     self.assertEqual(add(-1, 1), 100)
               myTests().main()

        .. tab:: Hint

           The function *prints* nothing.  It returns the sum of the two values passed in.
           
           The test cases are:
           ::

             add(1, 2)             # returns 103
             add(1.5, 2.0)         # returns 103.5
             add(-1, 1)            # returns 100

        .. tab:: Answer

           .. activecode:: bfunc4_a
              :nocanvas:

              def add(num1, num2):
                  return num1 + num2 + 100

.. question:: bfunc5_q

    .. tabbed:: bfunc5_tabs

        .. tab:: Question

            .. activecode:: bfunc5

               Define a function ``makeUserId()`` that receives two
               parameters -- a string ``name`` and a number ``num``, and
               returns a string that is the concatenation of the user name
               and the number.
               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(makeUserId("susan", 2), "susan2")
                     self.assertEqual(makeUserId("erica", 0), "erica0")
                     self.assertEqual(makeUserId("", -1), "-1")
               myTests().main()

        .. tab:: Hint

           Remember that you can only concatenate two strings -- not a
           string and an integer.
           
           The test cases are:
           ::

             makeUserId('susan', 2)             # returns "susan2"
             makeUserId('erica', 0)             # returns "erica0"
             makeUserId('', -1)                 # returns "-1"

        .. tab:: Answer

           .. activecode:: bfunc5_a
              :nocanvas:

              def makeUserId(name, num):
                  return name + str(num)

.. question:: bfunc6_q

    .. tabbed:: bfunc6_tabs

        .. tab:: Question

            .. activecode:: bfunc6

               Define a function ``max()`` that receives two
               numbers and returns the larger of the two.  Use an ``if-else`` statement.
               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(max(0, 1), 1)
                     self.assertEqual(max(44, -4.0), 44)
                     self.assertAlmostEqual(max(7.2, 7.2), 7.2)
               myTests().main()

        .. tab:: Hint

           You need an if-else statement in the function.
           
           The test cases are:
           ::

             max(0, 1)             # returns 1
             max(44, -4.0)         # returns 44
             max(7.2, 7.2)         # returns 7.2

        .. tab:: Answer

           .. activecode:: bfunc6_a
              :nocanvas:

              def max(num1, num2):
                  if num1 > num2:
                      return num1
                  else:
                      return num2

.. question:: bfunc7_q

    .. tabbed:: bfunc7_tabs

        .. tab:: Question

            .. activecode:: bfunc7

               Define a function ``makeFilledList()`` that takes two
               parameters:

               * length: the number of elements in the list
               * value: the value that should be repeated ``length`` times in the list.

               E.g., if the inputs where 3 and 0, the result would be [0, 0, 0]

               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(makeFilledList(4, 1), [1, 1, 1, 1])
                     self.assertEqual(makeFilledList(0, 4), [ ])
                     self.assertEqual(makeFilledList(10, "a"), [ "a", "a", "a", "a", "a", "a", "a", "a", "a", "a" ])
               myTests().main()

        .. tab:: Hint

           The test cases are:
           ::

             makeFilledList(4, 1)             # returns [1, 1, 1, 1]
             makeFilledList(0, 4)             # returns [ ]
             makeFilledList(10, "a")          # returns [ "a", "a", "a", "a", "a", "a", "a", "a", "a", "a" ]

        .. tab:: Answer

           .. activecode:: bfunc7_a
              :nocanvas:

              def makeFilledList(length, value):
                  res = [ ]
                  for i in range(length):
                      res.append(value)
                  return res
