SECTION 4: Strings
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

               Create a variable ``remainder`` that refers to the remainder when dividing 17 by 5.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(remainder, 17 % 5)

               myTests().main()

        .. tab:: Hint

           To get the remainder when dividing two numbers, you need to use the *modulo* operator ``%``.

        .. tab:: Answer

           .. activecode:: str3_a
              :nocanvas:

              remainder = 17 % 5

.. question:: str4_q

    .. tabbed:: str4_tabs

        .. tab:: Question

            .. activecode:: str4

               Write a small program that asks the user for two numbers and prints out the remainder 
               when dividing the first by the second.  An example run should look like this:

               Enter the numerator: ``22``

               Enter the denominator: ``4``

               The remainder when dividing is 2
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           To get the remainder when dividing two numbers, you need to use the *modulo* operator ``%``.

        .. tab:: Answer

           .. activecode:: str4_a
              :nocanvas:

              numerator = int(input('Enter the numerator: '))
              denominator = int(input('Enter the denominator: '))
              print('The remainder when dividing is', numerator % denominator)

.. question:: str5_q

    .. tabbed:: str5_tabs

        .. tab:: Question

            .. activecode:: str5

               You are a bean counter who counts beans and puts them into piles of 16 beans each.
               Your manager gives you some number of beans and asks you to tell him how many full piles
               that will produce.  Write a program that asks for the number of beans and prints
               out the number of full piles.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use integer division, which divides two numbers, and then "throws out" the fractional part.

        .. tab:: Answer

           .. activecode:: str5_a
              :nocanvas:

              beans = int(input('Enter # of beans: '))
              print(beans // 16)

.. question:: str6_q

    .. tabbed:: str6_tabs

        .. tab:: Question

            .. activecode:: str6

               Remainder and integer division can often be used together.
               Alter the program from the last exercise to print out not only the number of 
               full piles of beans, but also the number of beans that remain.
               E.g., a run of your program might look like this:

               Enter # of beans: ``99``

               99 beans is 6 piles with 3 remaining

               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use integer division, which divides two numbers, and then "throws out" the fractional part,
           and modulo division, which divides two numbers, keeping the remainder.
           You might find it useful to create 3 variables: ``beans`` is the count of beans the user entered, 
           ``piles`` is the computed number of piles, and ``remaining`` is the computed remainder.

        .. tab:: Answer

           .. activecode:: str6_a
              :nocanvas:

              beans = int(input('Enter # of beans: '))
              piles = beans // 16
              remaining = beans % 16
              print(beans, 'beans is', piles, 'piles with', remaining, 'remaining')

.. question:: str7_q

    .. tabbed:: str7_tabs

        .. tab:: Question

            .. activecode:: str7

               The *discriminant* of the quadratic formula is the stression:
               ``b^2 - 4ac``

               Write a program to ask the user for a value for ``a``, a value for ``b``,
               and a value for ``c``, and then prints the discriminant.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Don't forget that you cannot just put variables ``a`` and ``c`` next to each
           other.  You have to use ``*``.

        .. tab:: Answer

           .. activecode:: str7_a
              :nocanvas:

              a = int(input('Enter a: '))
              b = int(input('Enter b: '))
              c = int(input('Enter c: '))
              print(b * b - 4 * a * c)


.. question:: str8_q

    .. tabbed:: str8_tabs

        .. tab:: Question

            .. activecode:: str8

               Write a short program that asks the user to enter an integer, and then prints
	       out the last digit of the number that was entered.  E.g.,

	       Enter an integer: ``162``

	       The last digit is 2
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           The last digit of a number is the remainder when dividing by 10.
           

        .. tab:: Answer

           .. activecode:: str8_a
              :nocanvas:

              anInt = int(input('Enter an integer: '))
              lastDigit = anInt % 10
              print('The last digit is', lastDigit)

.. question:: str9_q

    .. tabbed:: str9_tabs

        .. tab:: Question

            .. activecode:: str9

               Write a short program that computes a total restaurant bill, including a 15%
	       tip.  E.g., 

	       Enter the amount on the bill: ``30.00``

               The 15% tip amount is: $4.5

	       The total is: $34.5
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use multiple variables and create your program one line at a time.  Remember that
           15% is 0.15. Don't worry about always having 2 digits after the decimal point.

        .. tab:: Answer

           .. activecode:: str9_a
              :nocanvas:

              subtotal = float(input('Enter the amount on the bill: '))
              tip = subtotal * 0.15
              print("The 15% tip amount is: $" + str(tip))
	      total = subtotal + tip
              print('The total is: $' + str(total))

