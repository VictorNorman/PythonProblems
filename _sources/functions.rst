More Function Definitions
:::::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: mfunc1_pre

   groceries = ['milk', 'bread', 'eggs', 'chocolate (dark)']

.. raw:: html

   </div>

.. question:: mfunc1_q
   :number: 1

    .. tabbed:: mfunc1_tabs

        .. tab:: Question

            .. activecode:: mfunc1

               Define a function ``minmax()`` that receives a list of numbers ``nums`` as
               a parameter.  The function finds the minimum value in the list and the maximum
               value in the list, and returns then both in a tuple. If the list is empty,
               the function returns ``0`` for both min and max values.

               E.g.::

                 minmax([44, 2, -3, 7])   # returns (-3, 44)
                 minmax([])               # returns (0, 0)
               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(minmax([-4, 7, -2, 5]), (-4, 7))
                     self.assertEqual(minmax([1]), (1, 1))
                     self.assertEqual(minmax([]), (0, 0))
               myTests().main()

        .. tab:: Hint

           Use ``min()`` and ``max()`` to find the mininum and maximum values in the
           list.

           You can return two items by returning them in a tuple: e.g., ``return (1, 2)``

        .. tab:: Answer

           .. activecode:: mfunc1_a
              :nocanvas:

              def minmax(nums):
                  if len(nums) == 0:
                      return (0, 0)
                  lMin = min(nums)
                  lMax = max(nums)
                  return (lMin, lMax)

.. question:: mfunc2_q

    .. tabbed:: mfunc2_tabs

        .. tab:: Question

            .. activecode:: mfunc2

               Define a function ``average()`` that receives a list of numbers ``nums`` as
               a parameter.  The function returns 0 if the list is empty.  Otherwise, it
               returns the average of the numbers in the list.  You may use ``sum()`` and
               ``len()`` to compute the average for the non-empty list.

               E.g.::

                 average([3, 4, 5, 6])    # returns 4.5
                 average([])              # returns 0
               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertAlmostEqual(average([3, 4, 5, 6]), 4.5)
                     self.assertAlmostEqual(average([]), 0.0)
               myTests().main()

        .. tab:: Hint

           First, use an if statement to test if the length is 0.

        .. tab:: Answer

           .. activecode:: mfunc2_a
              :nocanvas:

              def average(nums):
                  if len(nums) == 0:
                      return 0
                  return sum(nums) / len(nums)

.. question:: mfunc3_q

    .. tabbed:: mfunc3_tabs

        .. tab:: Question

            .. activecode:: mfunc3

               Define a function ``add()`` that receives two numbers ``v1`` and ``v2`` as 
               parameters, and also has a third optional parameter ``v3`` with a
               default value of 0.  The function returns the sum of the 2 (or 3) values.
               
               E.g.::

                 add(3, 4)                # returns 7
                 add(3, 4, 5)             # returns 12
               ~~~~
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertAlmostEqual(add(3, 4), 7.0)
                     self.assertAlmostEqual(add(1.1, 2.2, 3.3), 6.6)
               myTests().main()

        .. tab:: Hint

           An optional parameter with default value must be at the end of the list
           of parameters.

        .. tab:: Answer

           .. activecode:: mfunc3_a
              :nocanvas:

              def add(v1, v2, v3=0):    # v3 is the optional parameter with def. value 0
                  return v1 + v2 + v3

.. question:: mfunc4_q

    .. tabbed:: mfunc4_tabs

        .. tab:: Question

            .. activecode:: mfunc4

               Define a function ``sqrtsum()`` that takes 2 required parameters, plus 1 optional
               parameter ``debug``. The function returns the sum of the sqrt() of each parameter.
               If ``debug`` is True, it prints the result first before
               returning it.  The default value for ``debug`` is ``False``.

               E.g.::

                 sqrtsum(4.0, 25)             # returns 7.0
                 sqrtsum(100., 0, True)       # prints 10.0 and then returns 10.0

               ~~~~
               import math
               # Write your function definition here.
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertAlmostEqual(sqrtsum(4.0, 25), 7.0)
                     self.assertAlmostEqual(sqrtsum(100., 0, True), 10.0)
               myTests().main()

        .. tab:: Hint

           Compute the result into a local variable, say, ``result``. Then
           write an if statement to check if debug is True.  If so, print
           the result.  In either case, return the result.

        .. tab:: Answer

           .. activecode:: mfunc4_a
              :nocanvas:

              import math
              def sqrtsum(v1, v2, debug=False):
                  result = math.sqrt(v1) + math.sqrt(v2)
                  if debug:		# same as if debug == True:
                      print(result)
                  return result

.. question:: mfunc5_q

    .. tabbed:: mfunc5_tabs

        .. tab:: Question

            .. activecode:: mfunc5

               Define a function ``scaleby()`` that takes 2 parameters: a
               list ``inlist`` and a number, ``scale``.
               The function returns a new list, which contains each element in
               ``inlist`` multipled by ``scale``.

               E.g.::

                     scaleby([4, -3, 7], 3)  # returns [12, -9, 21]
                     scaleby([], 5)          # returns []
                     scaleby([0, 1000, -40], -5)  # returns [0, -5000, 200]

               ~~~~
               import math
               # Write your function definition here.
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertEqual(scaleby([4, -3, 7], 3), [12, -9, 21])
                     self.assertEqual(scaleby([], 5), [])
                     self.assertEqual(scaleby([0, 1000, -40], -5), [0, -5000, 200])
               myTests().main()

        .. tab:: Hint

           Create an empty list called ``result``.  Then, iterate through
           ``inlist``. For each value, multiply it by ``scale`` and
           append it to the result list.  At the end, return that list.

        .. tab:: Answer

           .. activecode:: mfunc5_a
              :nocanvas:

              def scaleby(inlist, scale):
                  result = []
                  for item in inlist:
                      result.append(item * scale)
                  return result

.. question:: mfunc6_q

    .. tabbed:: mfunc6_tabs

        .. tab:: Question

            .. activecode:: mfunc6

               Define a function ``constrain()`` that takes 2 or 3
               parameters. The first parameter is a required number. The
               second parameter, ``min``, is optional, with a default value
               of -1000000000 (negative 1 billion). The third parameter,
               ``max``, is optional, with a default value of 1000000000.

               The function returns the first value such that it has been
               constrained between ``min`` and ``max``. Thus, if the value
               is less than ``min`` it returns ``min``.  If the value is
               greater than ``max``, it returns ``max``.  Otherwise, the
               function returns the value unchanged.

               Note that if the caller provides values for min and/or max
               and min > max, the first parameter is returned unchanged.

               E.g.::

                 constrain(3, 0, 10)     # returns 3 because 0 < 3 < 10
                 constrain(10, 50)       # returns 50 because 10 < min of 50.
                 constrain(10, 0, 9)     # returns 9 because 10 > max of 9.
                 constrain(10, 20, -10)  # returns 10 because min > max.
                 
               ~~~~
               # Write your function definition here.
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                     self.assertAlmostEqual(constrain(3, 0, 10), 3)
                     self.assertAlmostEqual(constrain(10, 50), 50)
                     self.assertAlmostEqual(constrain(10, 0, 9), 9)
                     self.assertAlmostEqual(constrain(10, 20, -10), 10)
               myTests().main()

        .. tab:: Hint

           First, test if min is greater than max.  If so, return the
           value.
           
        .. tab:: Answer

           .. activecode:: mfunc6_a
              :nocanvas:

              def constrain(val, min=-1000000000, max=1000000000):
                  if min > max:
                      return val
                  if val < min:
                      return min
                  if val > max:
                      return max
                  return val

