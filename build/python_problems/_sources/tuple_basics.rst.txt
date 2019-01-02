Tuple Basics
:::::::::::::::::::::::::::

.. question:: tuples1_q
   :number: 1

    .. tabbed:: tuples1_tabs

        .. tab:: Question

            .. activecode:: tuples1

               Create a variable ``xycoords`` that refers to a *tuple* containing two
               values: ``3`` and ``-7``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertIs(type(xycoords), tuple, 'variable must be a tuple')
                      self.assertEqual(xycoords, (3, -7))
               myTests().main()

        .. tab:: Hint

	   Create a tuple with ``(`` and ``)`` and a comma separating each element.

        .. tab:: Answer

           .. activecode:: tuples1_a
              :nocanvas:

              xycoords = (3, -7)
              
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: tuples2_pre

   xycoords = (3, -7)

.. raw:: html

   </div>

.. question:: tuples2_q

    .. tabbed:: tuples2_tabs

        .. tab:: Question

            .. activecode:: tuples2
               :include: tuples2_pre

               Write code to print out the item at index 1 of already-defined tuple ``xycoords``.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   You can index a tuple just like you index a list or string, since a tuple is also a sequence.

        .. tab:: Answer

           .. activecode:: tuples2_a
              :nocanvas:
              :include: tuples2_pre

              print(xycoords[1])
              
