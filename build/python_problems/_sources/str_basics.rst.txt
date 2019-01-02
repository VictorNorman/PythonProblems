String Basics
:::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: str1_pre

   last_name = 'Lincoln'
   first_name = 'Abraham'

.. raw:: html

   </div>

.. question:: str1_q
   :number: 1

   .. tabbed:: str1_tabs

        .. tab:: Question

            .. activecode:: str1
               :include: str1_pre

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

           .. activecode:: str1_a
              :nocanvas:
              :include: str1_pre

              name = first_name + ' ' + last_name
              
.. question:: str2_q

   .. tabbed:: str2_tabs

        .. tab:: Question

            .. activecode:: str2
               :include: str1_pre

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

           .. activecode:: str2_a
              :nocanvas:
              :include: str1_pre

              name = first_name[0] + ' ' + last_name


.. question:: str3_q

    .. tabbed:: str3_tabs

        .. tab:: Question

            .. activecode:: str3

               Write a two-line program to read in a string from the user and then print out
               the length of that string.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use len(theString) to get the length of the string.

        .. tab:: Answer

           .. activecode:: str3_a
              :nocanvas:

              userStr = input("Enter a string: ")
              print(len(userStr))

.. question:: str4_q

    .. tabbed:: str4_tabs

        .. tab:: Question

            .. activecode:: str4

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

           .. activecode:: str4_a
              :nocanvas:

              userInput = input("Enter a string: ")
              print("First and last characters are:", userInput[0], userInput[-1])

