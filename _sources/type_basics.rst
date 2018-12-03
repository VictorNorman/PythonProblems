SECTION 4: Basic Types
:::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: types1_pre

   last_name = 'Lincoln'
   first_name = 'Abraham'

.. raw:: html

   </div>

.. question:: types1_q
   :number: 1

   .. tabbed:: types1_tabs

        .. tab:: Question

            .. activecode:: types1
               :include: types1_pre

               Assume two variables, ``last_name`` and ``first_name``, have been defined
	       and refer to strings.
               Write an assignment statement to make a new string, ``name``, that is the
	       concatenation of ``first_name`` and ``last_name`` with a space between.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertEqual(name, 'Abraham Lincoln')

               myTests().main()
        .. tab:: Hint

           Remember that you use ``+`` to concatenate strings.  Remember that you have to
	   put a space between the first and last names.

        .. tab:: Answer

           .. activecode:: types1_a
              :nocanvas:
              :include: types1_pre

              name = first_name + ' ' + last_name
              
.. question:: types2_q

   .. tabbed:: types2_tabs

        .. tab:: Question

            .. activecode:: types2
               :include: types1_pre

               Assume two variables, ``last_name`` and ``first_name``, have been defined
	       and refer to strings.
               Write an assignment statement to make a new string, ``name``, that is the
	       concatenation of the first initial of ``first_name`` and ``last_name`` with a space between.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertEqual(name, 'A Lincoln')

               myTests().main()
        .. tab:: Hint

           The first character in a string is accessed by indexing at 0.  E.g.,

           greeting = 'hello'

           firstLetter = greeting[0]

        .. tab:: Answer

           .. activecode:: types2_a
              :nocanvas:
              :include: types1_pre

              name = first_name[0] + ' ' + last_name


.. question:: types3_q

    .. tabbed:: types3_tabs

        .. tab:: Question

            .. activecode:: types3

               Write a two-line program to read in a string from the user and then print out
               the length of that string.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use len(theString) to get the length of the string.

        .. tab:: Answer

           .. activecode:: types3_a
              :nocanvas:

              userStr = input("Enter a string: ")
              print(len(userStr))

.. question:: types4_q

    .. tabbed:: types4_tabs

        .. tab:: Question

            .. activecode:: types4

               Write a small program that asks the user for a string and then prints out
               the first and last characters of that string. E.g.,

               Enter a string: ``Hello, world``

               First and last characters are: H d

               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use -1 as the index to get the last character of the string.

        .. tab:: Answer

           .. activecode:: types4_a
              :nocanvas:

              userInput = input("Enter a string: ")
              print("First and last characters are:", userInput[0], userInput[-1])


.. question:: types5_q

    .. tabbed:: types5_tabs

        .. tab:: Question

            .. activecode:: types5

               Write code to create a list called ``greetings`` containing the string 'hello' and the string 'nihao'.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertEqual(greetings, ['hello', 'nihao'])

               myTests().main()

        .. tab:: Hint

           Use ``[`` and ``]`` and separate the strings with commas.

        .. tab:: Answer

           .. activecode:: types5_a
              :nocanvas:

              greetings = ['hello', 'nihao']

.. question:: types6_q

    .. tabbed:: types6_tabs

        .. tab:: Question

            .. activecode:: types6

               Write a statement to create a variable ``emptyList`` referring to an empty list.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertEqual(emptyList, [])

               myTests().main()

        .. tab:: Hint

	   You can create an empty list by using ``[`` and ``]`` with nothing in between.

        .. tab:: Answer

           .. activecode:: types6_a
              :nocanvas:

	      emptyList = []              
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: types7_pre

   groceries = ['milk', 'eggs', 'chocolate!', 'Doritos!', 'bread']

.. raw:: html

   </div>

.. question:: types7_q

    .. tabbed:: types7_tabs

        .. tab:: Question

            .. activecode:: types7
               :include: types7_pre

               Write code to print the element at index 2 from a previously-defined variable ``groceries``.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Call print(), accessing groceries inside it.

        .. tab:: Answer

           .. activecode:: types7_a
              :nocanvas:
              :include: types7_pre

	      print(groceries[2])

.. question:: types8_q

    .. tabbed:: types8_tabs

        .. tab:: Question

            .. activecode:: types8
               :include: types7_pre

               Write code to print the 2nd-to-last element of previously-defined variable ``groceries``.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Use -2 to access the 2nd-to-last element.

        .. tab:: Answer

           .. activecode:: types8_a
              :nocanvas:
              :include: types7_pre

	      print(groceries[-2])

.. question:: types9_q

    .. tabbed:: types9_tabs

        .. tab:: Question

            .. activecode:: types9

               Write code to create a list containing 3 elements, your name, your age, your eye color,
               where your name and eye color are strings, and your age is a number.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Lists can contain elements of any type.

        .. tab:: Answer

           .. activecode:: types9_a
              :nocanvas:

	      myInfo = ['Victor Norman', 53, 'hazel']


.. raw:: html

   <div style='display:none;'>

.. activecode:: types10_pre

   groceries = ['milk', 'eggs', 'chocolate!', 'Doritos!', 'bread']

.. raw:: html

   </div>

.. question:: types10_q

    .. tabbed:: types10_tabs

        .. tab:: Question

            .. activecode:: types10
               :include: types10_pre

               Write a line of code to replace the element at index 1 of a previously-defined
               list ``groceries`` with the string 'chocolate milk'.
               
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertEqual(groceries[1], 'chocolate milk')
                      self.assertEqual(len(groceries), 5)

               myTests().main()

        .. tab:: Hint

	   To replace an element in a list, access that element on the left-hand-side of an assignment statement.

        .. tab:: Answer

           .. activecode:: types10_a
              :nocanvas:
              :include: type10_pre

	      groceries[1] = 'chocolate milk'

