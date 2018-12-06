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

               If ``v1`` = 1, and ``v2`` = 2, create a string in variable ``resStr`` which refers to
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


