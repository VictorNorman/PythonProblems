Function Definitions
:::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: func1_pre

   groceries = ['milk', 'bread', 'eggs', 'chocolate (dark)']

.. raw:: html

   </div>

.. question:: func1_q
   :number: 1

    .. tabbed:: func1_tabs

        .. tab:: Question

            .. activecode:: func1

               Define a function ``greet()`` that receives a string ``name`` as a parameter and
               prints ``Hi,`` followed by the value of ``name``.  E.g., if ``name`` is `Georgia`, it prints
               ``Hi, Georgia``.

               The function returns nothing.
               ~~~~
               ====
               greet('Georgia')
               greet('Victor')

        .. tab:: Hint

           A function definition starts with ``def`` and then the name of the function.
           The contents (or "body") of the function is indented.

        .. tab:: Answer

           .. activecode:: func1_a
              :nocanvas:

              def greet(name):
                  print("Hi, " + name)

.. question:: func2_q

    .. tabbed:: func2_tabs

        .. tab:: Question

            .. activecode:: func2

               Define a function ``greet()`` that receives a string ``name`` as a parameter and
               *returns* ``Hi,`` followed by the value of ``name``.

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

           .. activecode:: func2_a
              :nocanvas:

              def greet(name):
                  return "Hi, " + name

.. question:: func3_q

    .. tabbed:: func3_tabs

        .. tab:: Question

            .. activecode:: func3

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

           .. activecode:: func3_a
              :nocanvas:

              def add(num1, num2):
                  return num1 + num2

.. question:: func4_q

    .. tabbed:: func4_tabs

        .. tab:: Question

            .. activecode:: func4

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

           .. activecode:: func4_a
              :nocanvas:

              def add(num1, num2):
                  return num1 + num2

.. question:: func5_q

    .. tabbed:: func5_tabs

        .. tab:: Question

            .. activecode:: func5

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

           .. activecode:: func5_a
              :nocanvas:

              def makeUserId(name, num):
                  return name + str(num)

.. question:: func6_q

    .. tabbed:: func6_tabs

        .. tab:: Question

            .. activecode:: func6

               Define a function ``max()`` that receives two
               numbers and returns the larger of the two.
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

           .. activecode:: func6_a
              :nocanvas:

              def max(num1, num2):
                  if num1 > num2:
                      return num1
                  else:
                      return num2

.. question:: func7_q

    .. tabbed:: func7_tabs

        .. tab:: Question

            .. activecode:: func7

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

           .. activecode:: func7_a
              :nocanvas:

              def makeFilledList(length, value):
                  res = [ ]
                  for i in range(length):
                      res.append(value)
                  return res

.. question:: func8_q

    .. tabbed:: func8_tabs

        .. tab:: Question

            .. activecode:: func8

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

           .. activecode:: func8_a
              :nocanvas:

              def makeFilledList(length, value):
                  res = [ ]
                  for i in range(length):
                      res.append(value)
                  return res

.. question:: func9_q

    .. tabbed:: func9_tabs

        .. tab:: Question

            .. activecode:: func9

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

           .. activecode:: func9_a
              :nocanvas:

              def makeFilledList(length, value):
                  res = [ ]
                  for i in range(length):
                      res.append(value)
                  return res
