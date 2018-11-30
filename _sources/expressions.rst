SECTION 3: Expressions
:::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: expr1_pre

   x = 4.2

.. raw:: html

   </div>

.. question:: expr1_q
   :number: 1

   .. tabbed:: expr1_tabs

        .. tab:: Question

            .. activecode:: expr1
               :include: expr1_pre

               Write the following statement in legal python ``y = x^2 + 2x + 10``, assuming that 
               variable ``x`` already refers to a value.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(x, 4.2)
                      self.assertAlmostEqual(y, 36.04)

               myTests().main()
        .. tab:: Hint

           The exponentiation operator is ``**``.  Also, you cannot put ``2`` and ``x`` directly next
           to each other to do multiplication.  You have to use ``*``.

        .. tab:: Answer

           .. activecode:: expr1_a
              :nocanvas:

              y = x ** 2 + 2 * x + 10
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: expr2_pre

   miles = 42.5
   gallons = 1.3

.. raw:: html

   </div>

.. question:: expr2_q

   .. tabbed:: expr2_tabs

        .. tab:: Question

            .. activecode:: expr2
               :include: expr2_pre

               Given two variables, ``miles`` and ``gallons``, write an assignment statement
               that creates the variable ``mpg`` set to the computed number of miles per gallon.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(mpg, miles / gallons)

               myTests().main()
        .. tab:: Hint

           Use the true division operator ``/``.

        .. tab:: Answer

           .. activecode:: expr2_a
              :nocanvas:

              mpg = miles / gallons


.. question:: expr3_q

    .. tabbed:: expr3_tabs

        .. tab:: Question

            .. activecode:: expr3

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

           .. activecode:: expr3_a
              :nocanvas:

              remainder = 17 % 5

.. question:: expr4_q

    .. tabbed:: expr4_tabs

        .. tab:: Question

            .. activecode:: expr4

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

           .. activecode:: expr4_a
              :nocanvas:

              numerator = int(input('Enter the numerator: '))
              denominator = int(input('Enter the denominator: '))
              print('The remainder when dividing is', numerator % denominator)

.. question:: expr5_q

    .. tabbed:: expr5_tabs

        .. tab:: Question

            .. activecode:: expr5

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

           .. activecode:: expr5_a
              :nocanvas:

              beans = int(input('Enter # of beans: '))
              print(beans // 16)

.. question:: expr6_q

    .. tabbed:: expr6_tabs

        .. tab:: Question

            .. activecode:: expr6

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

           .. activecode:: expr6_a
              :nocanvas:

              beans = int(input('Enter # of beans: '))
              piles = beans // 16
              remaining = beans % 16
              print(beans, 'beans is', piles, 'piles with', remaining, 'remaining')

.. question:: expr7_q

    .. tabbed:: expr7_tabs

        .. tab:: Question

            .. activecode:: expr7

               The *discriminant* of the quadratic formula is the expression:
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

           .. activecode:: expr7_a
              :nocanvas:

              a = int(input('Enter a: '))
              b = int(input('Enter b: '))
              c = int(input('Enter c: '))
              print(b * b - 4 * a * c)
