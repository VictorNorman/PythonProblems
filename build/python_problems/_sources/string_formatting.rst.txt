String Formating
:::::::::::::::::::::::::::

.. question:: strform1_q
   :number: 1

    .. tabbed:: strform1_tabs

        .. tab:: Question

            .. activecode:: strform1

               Assume you have a variable ``x`` that refers to an integer.
	       Write code to print out the value of x surrounded by arrows.  E.g.,
               if the value of x is 7, you should print this:

	       ``-->7<--``

               ~~~~
               x = 7
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Use ``%d`` as the specifier in the format string.

        .. tab:: Answer

           .. activecode:: strform1_a
              :nocanvas:

              print('-->%d<--' % x)
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: strform2_pre

   v1 = 73
   v2 = -2

.. raw:: html

   </div>

.. question:: strform2_q

    .. tabbed:: strform2_tabs

        .. tab:: Question

            .. activecode:: strform2
               :include: strform2_pre

               Given two integers ``v1`` and ``v2``, use string formatting to create a string ``values``
               showing the values of ``v1`` and ``v2`` with a ', ' between (a comma and a space).
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(values, '73, -2')
               myTests().main()

        .. tab:: Hint

	   Make sure you put your values in a tuple.

        .. tab:: Answer

           .. activecode:: strform2_a
              :nocanvas:
              :include: strform2_pre

              values = '%d, %d' % (v1, v2)
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: strform3_pre

   v1 = 1
   v2 = 3.75
   v3 = 'hi'

.. raw:: html

   </div>

.. question:: strform3_q

    .. tabbed:: strform3_tabs

        .. tab:: Question

            .. activecode:: strform3
               :include: strform3_pre

               If ``v1`` = 1, ``v2`` = 3.75, and ``v3`` = "hi", create a string in
               variable ``resStr`` with value ``hi! 1 != 3.75 :-(``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(resStr, 'hi! 1 != 3.75 :-(')
               myTests().main()

        .. tab:: Hint

	   Put your three values in a tuple in the order ``v3``, ``v1``, ``v2``.
           To make sure you have only 2 digits after the decimal, use this format specifier: ``%.2f``

        .. tab:: Answer

           .. activecode:: strform3_a
              :nocanvas:
              :include: strform3_pre

              resStr = '%s! %d != %.2f :-(' % (v3, v1, v2)

.. raw:: html

   <div style='display:none;'>

.. activecode:: strform4_pre

   v1 = 1
   v2 = 2

.. raw:: html

   </div>

.. question:: strform4_q

    .. tabbed:: strform4_tabs

        .. tab:: Question

            .. activecode:: strform4
               :include: strform4_pre

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

           .. activecode:: strform4_a
              :nocanvas:
              :include: strform4_pre

              resStr = 'variable 1 is %d (%.1f) and variable 2 is %d (%.1f)' % (v1, v1, v2, v2)
