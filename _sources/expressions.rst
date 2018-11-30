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

               Write a small program that asks the user for a number of days and then prints out
               the number of complete weeks for that number of days.  E.g., if the user enters
               9, the program prints out 9 days is 1 complete week (and some remaining days).
               If the user enters 15, the program prints out 2.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use integer division, which divides two numbers, and then "throws out" the fractional part.

        .. tab:: Answer

           .. activecode:: expr5_a
              :nocanvas:

              days = int(input('Enter days: '))
              print(days // 7)
