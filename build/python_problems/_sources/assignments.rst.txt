Simple Assignments
:::::::::::::::::::::::::::::


.. question:: sass1_q
   :number: 1

   .. tabbed:: sass1_tab

        .. tab:: Question

            .. activecode:: sass1

               Write code to create a variable ``score`` and make it refer to
               the integer 1.
               ~~~~
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                     self.assertEqual(score, 1)
                     self.assertIs(type(score), int, "variable must refer to an int")

               myTests().main()

        .. tab:: Hint

           Remember that an assignment is a ``=`` with a variable on the left-hand
           side and a value or expression on the right-hand side.

        .. tab:: Answer

           .. activecode:: sass1_a
              :nocanvas:

              score = 1

.. question:: sass2_q

   .. tabbed:: sass2_tab

        .. tab:: Question

           .. activecode:: sass2

              Write code to create a variable ``temperature`` and make it refer to a floating point number.
              ~~~~
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                     self.assertIs(type(temperature), float, "variable must refer to a float")

              myTests().main()
        .. tab:: Hint

           A floating point number is a real number. I.e., it has a ``.`` in it.

        .. tab:: Answer

           .. activecode:: sass2_a
              :nocanvas:

              temperature = 57.3

.. question:: sass3_q

   .. tabbed:: sass3_tab

        .. tab:: Question

           .. activecode:: sass3

              Write code to create a variable ``name`` and make it refer to a string.
              ~~~~
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                     self.assertIs(type(name), str, "variable must refer to a string")

              myTests().main()

        .. tab:: Hint

           A string is enclosed by single or double quotes.

        .. tab:: Answer

           .. activecode:: sass3_a
              :nocanvas:

              name = "Desmond Tutu"


.. question:: sass4_q

   .. tabbed:: sass4_tab

        .. tab:: Question

           .. activecode:: sass4

              Write code to create a variable ``matches`` and make it refer to a boolean value.
              ~~~~
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                     self.assertIs(type(matches), bool, "variable must refer to a boolean")

              myTests().main()

        .. tab:: Hint

           The two booleans values are ``True`` and ``False``.

        .. tab:: Answer

           .. activecode:: sass4_a
              :nocanvas:

              matches = False


.. question:: sass5_q

   .. tabbed:: sass5_tab

        .. tab:: Question

           .. activecode:: sass5
              :include: sass2_a

              Assume the variable ``temperature`` has been initialized to some value.
              Write code to add 1 to the variable ``temperature``.
              ~~~~
              # replace this comment with your code
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(temperature, 58.3)

              myTests().main()

        .. tab:: Hint

           The right-hand side of an equation is evaluated first, so you can take
           ``temperature`` and add 1 to it on the right-hand side, and then put
           ``temperature`` on the left-hand side of the ``=`` sign.

        .. tab:: Answer

           .. activecode:: sass5_a
              :nocanvas:
              :include: sass2_a

              temperature = temperature + 1
              # Also, could be written temperature += 1

.. raw:: html

   <div style='display:none;'>

.. activecode:: sass6_pre

   hours = 30.0
   hourly_rate = 11.50

.. raw:: html

   </div>

.. question:: sass6_q

   .. tabbed:: sass6_tab

        .. tab:: Question

           .. activecode:: sass6
              :include: sass6_pre

              Assume you have two variables ``hours`` and ``hourly_rate``.  Write code to compute the
              ``total_pay``, by multiplying ``hours`` and ``hourly_rate`` and storing in ``total_pay``.
              ~~~~
              # Assume hours and hourly_rate have been defined and given values.

              # replace this comment with your code
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(total_pay, hours * hourly_rate)

              myTests().main()

        .. tab:: Hint

           Multiply ``hours`` and ``hourly_rate`` on the right-hand side of the assignment statement.

        .. tab:: Answer

           .. activecode:: sass6_a
              :nocanvas:
	      :include: sass6_pre

              total_pay = hours * hourly_rate
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: sass7_pre

   p1_points = 17
   p2_points = 44

.. raw:: html

   </div>

.. question:: sass7_q

   .. tabbed:: sass7_tabs

        .. tab:: Question

           .. activecode:: sass7
              :include: sass7_pre

              Assume you have two variables ``p1_points`` and ``p2_points``.  Write a line of code
              to indicate that player p1 added all of player p2's points to her own.
              ~~~~
              # replace this comment with your code
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(p1_points, 61)
                      self.assertAlmostEqual(p2_points, 44)

              myTests().main()

        .. tab:: Hint

           Your code needs to add ``p2_points`` to ``p1_points`` and make ``p1_points`` refer to the
           result.

        .. tab:: Answer

           .. activecode:: sass7_a
              :nocanvas:
              :include: sass7_pre

              p1_points = p1_points + p2_points
              # or  p1_points = p2_points + p1_points

.. raw:: html

   <div style='display:none;'>

.. activecode:: sass8_pre

   ball1_direction = 17 

.. raw:: html

   </div>

.. question:: sass8_q

   .. tabbed:: sass8_tabs

        .. tab:: Question

           .. activecode:: sass8
              :include: sass8_pre

              Assume you have a variable ``ball1_direction``.  Write a line of code
              that set ball2's direction to be the same as ball1's direction.
              ~~~~
              # replace this comment with your code
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(ball2_direction, ball1_direction)
                      self.assertAlmostEqual(ball1_direction, 17)

              myTests().main()

        .. tab:: Hint

           Your code creates variable ``ball2_direction`` on the left-hand side of the ``=``
           sign and sets it value to ``ball1_direction``.

        .. tab:: Answer

           .. activecode:: sass8_a
              :nocanvas:
              :include: sass8_pre

              ball2_direction = ball1_direction

.. question:: sass9_q

   .. tabbed:: sass9_tabs

        .. tab:: Question

           Replace these statements with a single statement so that you don't use the variable ``y`` --
           just the variable ``x`` being set to a value.

           .. activecode:: sass9

              x = 7
              y = x + 1
              x = y
              ====
              from unittest.gui import TestCaseGui

              class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertAlmostEqual(x, 8)

              myTests().main()

        .. tab:: Answer

           .. activecode:: sass9_a
              :nocanvas:

	           x = 8

.. question:: sass10_q

   .. tabbed:: sass10_tabs

        .. tab:: Question

           Before running the following code, predict what value will be printed.

           .. activecode:: sass10

              x = 7
              y = 9
              y = x
              x = 4
              print(y)

           If you don't understand the answer, using **CodeLens** might help.
