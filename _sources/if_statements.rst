If Statements
:::::::::::::::::::::::::::

**if statements** have this general form:

**if** ``conditional`` :

     **body**

and

**if-else statements** have this general form:

**if** ``conditional`` :

     **if-body**

**else:**

     **else-body**

and

**if-elif-else statements** have this general form:

**if** ``conditional`` :

     **if-body**

**elif** ``conditional`` :

     **elif-body**

**else:**

     **else-body**

.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt1_pre

   v1 = 4
   v2 = 5

.. raw:: html

   </div>

.. question:: ifstmt1_q
   :number: 1

    .. tabbed:: ifstmt1_tabs

        .. tab:: Question

            .. activecode:: ifstmt1
               :include: ifstmt1_pre

               Write an if statement that executes the **body** only if ``v1`` is less than ``v2``.
               The **body** should simply contain ``print('yes')``.

               ~~~~
               # replace this comment with your if statement
                   print('yes')
               ====

        .. tab:: Hint

	   Look at the top of this file for a reminder about the formatting of an if statement.

           You do not need an else part.

        .. tab:: Answer

           .. activecode:: ifstmt1_a
              :nocanvas:
              :include: ifstmt1_pre

              if v1 < v2:
                  print('yes')
              
.. question:: ifstmt2_q

    .. tabbed:: ifstmt2_tabs

        .. tab:: Question

            .. activecode:: ifstmt2
               :include: ifstmt1_pre

               Write an if statement that prints ``yes`` if ``v1`` is greater than ``v2`` and prints ``no`` otherwise.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Look at the top of this file for a reminder about the formatting of an if-else statement.

           You need an else part.

        .. tab:: Answer

           .. activecode:: ifstmt2_a
              :nocanvas:
              :include: ifstmt1_pre

              if v1 > v2:
                  print('yes')
              else:
                  print('no')

.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt3_pre

   v1 = 7
   v2 = 5
   v3 = 4
   v4 = 8

.. raw:: html

   </div>

.. question:: ifstmt3_q

    .. tabbed:: ifstmt3_tabs

        .. tab:: Question

            .. activecode:: ifstmt3
               :include: ifstmt3_pre

               Write an if statement that prints ``yes`` if ``v1`` is less than ``v2`` and ``v3`` is equal to ``v4``.
               Nothing is printed otherwise.
               ~~~~
               # replace this comment with your if statement
               ====

        .. tab:: Hint

	   Use ``and`` to join the two boolean expressions.

           You do not need an else part.

           Don't forget to use ``==``, not ``=`` (which is assignment).

        .. tab:: Answer

           .. activecode:: ifstmt3_a
              :nocanvas:
              :include: ifstmt3_pre

              if v1 < v2 and v3 == v4:
                  print('yes')

.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt4_pre

   v1 = 1
   v2 = 2

.. raw:: html

   </div>

.. question:: ifstmt4_q

    .. tabbed:: ifstmt4_tabs

        .. tab:: Question

            .. activecode:: ifstmt4
               :include: ifstmt4_pre

               If ``v1`` = 1, and ``v2`` = 2, create string variable ``resStr`` which refers to
               ``variable 1 is 1 (1.0) and variable 2 is 2 (2.0)``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(resStr, 'variable 1 is 1 (1.0) and variable 2 is 2 (2.0)')
               myTests().main()

        .. tab:: Hint

           To make sure you have only 1 digit after the decimal, use this format specifier: ``%.1f``

           You can use a variable multiple times in the same tuple.

        .. tab:: Answer

           .. activecode:: ifstmt4_a
              :nocanvas:
              :include: ifstmt4_pre

              resStr = 'variable 1 is %d (%.1f) and variable 2 is %d (%.1f)' % (v1, v1, v2, v2)

.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt5_pre

   v1 = 17
   v4 = 4

.. raw:: html

   </div>

.. question:: ifstmt5_q

    .. tabbed:: ifstmt5_tabs

        .. tab:: Question

            .. activecode:: ifstmt5
               :include: ifstmt5_pre

               Write an if statement that prints ``is not 3 times`` if ``v1`` is not equal to 3 times the value
               of ``v4``.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           To make sure you have only 1 digit after the decimal, use this format specifier: ``%.1f``

           Not equal to is ``!=``.

        .. tab:: Answer

           .. activecode:: ifstmt5_a
              :nocanvas:
              :include: ifstmt5_pre

              if v1 != 3 * v4:
                  print('is not 3 times')

.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt6_pre

   idx = 17

.. raw:: html

   </div>

.. question:: ifstmt6_q

    .. tabbed:: ifstmt6_tabs

        .. tab:: Question

            .. activecode:: ifstmt6
               :include: ifstmt6_pre

               Write an if statement that assigns ``res`` to 'even number' if variable ``idx``
               is an even number and ``res`` to 'odd number' otherwise.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(res, 'odd number')
               myTests().main()

        .. tab:: Hint

           You can tell if a value is even if when you divide it by 2, the remainder is 0.

        .. tab:: Answer

           .. activecode:: ifstmt6_a
              :nocanvas:
              :include: ifstmt6_pre

              if idx % 2 == 0:
                  res = 'even number'
              else:
                  res = 'odd number'

.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt7_pre

   v1 = 199.9999

.. raw:: html

   </div>

.. question:: ifstmt7_q

    .. tabbed:: ifstmt7_tabs

        .. tab:: Question

            .. activecode:: ifstmt7
               :include: ifstmt7_pre

               Write an if statement that assigns ``res`` to 1 if variable ``v1``
               is strictly between 100 and 200.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(res, 1)
               myTests().main()

        .. tab:: Hint

           Use ``<`` and ``>`` and ``and``.

           Remember that you have to have a value, variable, or expression on each side of
           a ``<`` or ``>``.  You cannot write ``v1 > 100 and < 200`` because there is no expression
           on the left side of the ``<``.

        .. tab:: Answer

           .. activecode:: ifstmt7_a
              :nocanvas:
              :include: ifstmt7_pre

              if v1 > 100 and v1 < 200:
                  res = 1
              # could also write: if 100 < v1 < 200:


.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt8_pre

   year = 2000

.. raw:: html

   </div>

.. question:: ifstmt8_q

    .. tabbed:: ifstmt8_tabs

        .. tab:: Question

            .. activecode:: ifstmt8
               :include: ifstmt8_pre

               Write an if statement that assigns ``leap`` to ``True`` if variable ``year`` is a multiple of 4
               and is not a multiple of 100, and to ``False`` otherwise.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(leap, False)
               myTests().main()

        .. tab:: Hint

           A number ``n`` is a multiple of another number ``d``, if when you divide ``n`` by ``d``,
           the remainder is 0.

        .. tab:: Answer

           .. activecode:: ifstmt8_a
              :nocanvas:
              :include: ifstmt8_pre

              if year % 4 == 0 and year % 100 != 0:
                  leap = True
              else:
                  leap = False


.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt9_pre

   result = 44

.. raw:: html

   </div>

.. question:: ifstmt9_q

    .. tabbed:: ifstmt9_tabs

        .. tab:: Question

            .. activecode:: ifstmt9
               :include: ifstmt9_pre

               Write an if statement that assigns 1 to ``answer`` if variable ``result`` has the value ``100``,
               and sets ``answer`` to 2 otherwise.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(answer, 2)
               myTests().main()

        .. tab:: Hint

           Use an if-else statement.
           

        .. tab:: Answer

           .. activecode:: ifstmt9_a
              :nocanvas:
              :include: ifstmt9_pre

              if result == 100:
                  answer = 1
              else:
                  answer = 2

.. raw:: html

   <div style='display:none;'>

.. activecode:: ifstmt10_pre

   score = 72

.. raw:: html

   </div>

.. question:: ifstmt10_q

    .. tabbed:: ifstmt10_tabs

        .. tab:: Question

            .. activecode:: ifstmt10
               :include: ifstmt10_pre

               Write an ifelse statement that sets the value of a variable ``gradepoint`` to 4
               if a variable ``score`` is greater than 90, 3 if ``score`` is between 80 and 89, 
               2 if ``score`` is between 70 and 79, 1 if ``score`` is between 60 and 69, and 0 otherwise.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(gradepoint, 2)
               myTests().main()

        .. tab:: Hint

           Use an if-elif-else statement.

        .. tab:: Answer

           .. activecode:: ifstmt10_a
              :nocanvas:
              :include: ifstmt10_pre

              if score > 90:
                  gradepoint = 4
              elif score > 80:
                  gradepoint = 3
              elif score > 70:
                  gradepoint = 2
              elif score > 60:
                  gradepoint = 1
              else:
                  gradepoint = 0

.. question:: ifstmt11_q

    .. tabbed:: ifstmt11_tabs

        .. tab:: Question

            .. activecode:: ifstmt11

               Write a short program that first asks the user to input 3 numbers.
               (Do this with 3 individual ``input()`` calls, storing the results in 3 variables.)
               Then, the program prints out the largest of the 3 numbers.
               You may assume the user enters three distinct values.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use multiple if/elif statements, each with multiple boolean operators connected together with ``and`` s.


        .. tab:: Answer

           .. activecode:: ifstmt11_a
              :nocanvas:

              v1 = float(input("Enter first value:"))
              v2 = float(input("Enter second value:"))
              v3 = float(input("Enter third value:"))
              if v1 > v2 and v1 > v3:
                  print(v1)
              elif v2 > v1 and v2 > v3:
                  print(v2)
              else:
                  print(v3)

.. question:: ifstmt12_q

    .. tabbed:: ifstmt12_tabs

        .. tab:: Question

            .. activecode:: ifstmt12

               Write a short program that asks the user for a payrate and a number of hours, and then
               prints out the total pay. Any hours over 40 are paid with time and a half.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use an if-else statement.

        .. tab:: Answer

           .. activecode:: ifstmt12_a
              :nocanvas:

              payrate = float(input("Enter hourly payrate: "))
              hours = float(input("Enter total hours worked: "))
              if hours > 40:
                  pay = payrate * 1.5 * (hours - 40) + payrate * 40
              else:
                  pay = payrate * hours
              print('Your pay will is', pay)

.. question:: ifstmt13_q

    .. tabbed:: ifstmt13_tabs

        .. tab:: Question

            .. activecode:: ifstmt13

               On a roulette wheel, the pockets are numbered from 0 to 36.  The colors of the pockets
               are as follows:

               * Pocket 0 is green.
               * For pockets 1 through 10, the odd-numbered pockets are red and the even-numbered pockets are black.
               * For pockets 11 through 18, the odd-numbered pockets are black and the even-numbered pockets are red.
               * For pockets 19 through 28, the odd-numbered pockets are red and the even-numbered pockets are black.
               * For pockets 29 through 36, the odd-numbered pockets are black and the even-numbered pockets are red.

               Write a program that asks the user to enter a pocket number
               and displays whether the pocket is green, red, or black.
               The program should display an error message if the user
               enters a number that is outside the range of 0 through 36. 
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use an if-elif-else statement with nested if statements in each
           part.  An odd number is one where when you divide by 2, the
           remainder is 1.

        .. tab:: Answer

           .. activecode:: ifstmt13_a
              :nocanvas:

              pocket = int(input("Enter a pocket number from 0 to 36, inclusive: "))
              if pocket < 0 or pocket > 36:
                  print("That is not a legal pocket number.")
              elif pocket == 0:
                  print("Pocket is green")
              elif pocket >= 1 and pocket <= 10:
                  if pocket % 2 == 1:
                      print("Pocket is red")
                  else:
                      print("Pocket is black")
              elif pocket >= 11 and pocket <= 18:
                  if pocket % 2 == 0:
                      print("Pocket is red")
                  else:
                      print("Pocket is black")
              elif pocket >= 19 and pocket <= 28:
                  if pocket % 2 == 1:
                      print("Pocket is red")
                  else:
                      print("Pocket is black")
              else:
                  if pocket % 2 == 0:
                      print("Pocket is red")
                  else:
                      print("Pocket is black")


.. question:: ifstmt14_q

    .. tabbed:: ifstmt14_tabs

        .. tab:: Question

            .. activecode:: ifstmt14

               Write a program that asks the user to enter two numbers and
               an operator to apply to them.  The operator must be one of
               ``+``, ``-``, ``*``, ``/``, ``//``, or ``%``. The program
               applies the operator to the numbers and prints the result.

               Here is an example run:

               Enter first number: ``46``

               Enter second number: ``13.5``

               Enter an operator (one of +, -, \*, /, //, %): ``-``

               ``46.0000000 - 13.5000000 = 32.500000`` 

               If the user enters an illegal operator, the program prints
               an error message.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

           Use an if-elif-else statement.
           The print statement for the + operator looks like this:

	   ``print('%f + %f = %f' % (num1, num2, num1 + num2))``

        .. tab:: Answer

           .. activecode:: ifstmt14_a
              :nocanvas:

              num1 = float(input("Enter first number: "))
              num2 = float(input("Enter second number: "))
              op = input("Enter an operator (one of +, -, *, /, //, %): ")
              if op == '+':
                  print('%f + %f = %f' % (num1, num2, num1 + num2))
              elif op == '-':
                  print('%f - %f = %f' % (num1, num2, num1 - num2))
              elif op == '*':
                  print('%f * %f = %f' % (num1, num2, num1 * num2))
              elif op == '/':
                  print('%f / %f = %f' % (num1, num2, num1 / num2))
              elif op == '//':
                  print('%f // %f = %f' % (num1, num2, num1 // num2))
              elif op == '%':
                  print('%f % %f = %f' % (num1, num2, num1 % num2))
              else:
                  print('%s is an unknown operator' % op)



