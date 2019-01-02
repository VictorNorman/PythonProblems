List Basics
:::::::::::::::::::::::::::

.. question:: list1_q
   :number: 1

    .. tabbed:: list1_tabs

        .. tab:: Question

            .. activecode:: list1

               Write code to create a list called ``greetings`` containing the string 'hello' and the string 'nihao'.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(greetings, ['hello', 'nihao'])
               myTests().main()

        .. tab:: Hint

           Use ``[`` and ``]`` and separate the strings with commas.

        .. tab:: Answer

           .. activecode:: list1_a
              :nocanvas:

              greetings = ['hello', 'nihao']

.. question:: list2_q

    .. tabbed:: list2_tabs

        .. tab:: Question

            .. activecode:: list2

               Write a statement to create a variable ``emptyList`` referring to an empty list.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(emptyList, [])
               myTests().main()

        .. tab:: Hint

	   You can create an empty list by using ``[`` and ``]`` with nothing in between.

        .. tab:: Answer

           .. activecode:: list2_a
              :nocanvas:

	      emptyList = []              
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: list3_pre

   groceries = ['milk', 'eggs', 'chocolate!', 'Doritos!', 'bread']

.. raw:: html

   </div>

.. question:: list3_q

    .. tabbed:: list3_tabs

        .. tab:: Question

            .. activecode:: list3
               :include: list3_pre

               Write code to print the element at index 2 from a previously-defined list ``groceries``.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Call print(), accessing groceries inside it.

        .. tab:: Answer

           .. activecode:: list3_a
              :nocanvas:
              :include: list3_pre

	      print(groceries[2])

.. question:: list4_q

    .. tabbed:: list4_tabs

        .. tab:: Question

            .. activecode:: list4
               :include: list3_pre

               Write code to print the 2nd-to-last element of previously-defined list ``groceries``.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Use -2 to access the 2nd-to-last element.

        .. tab:: Answer

           .. activecode:: list4_a
              :nocanvas:
              :include: list3_pre

	      print(groceries[-2])

.. question:: list5_q

    .. tabbed:: list5_tabs

        .. tab:: Question

            .. activecode:: list5

               Write code to create a list containing 3 elements, your name, your age, your eye color,
               where your name and eye color are strings, and your age is a number.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Lists can contain elements of any type.

        .. tab:: Answer

           .. activecode:: list5_a
              :nocanvas:

	      myInfo = ['Victor Norman', 53, 'hazel']


.. raw:: html

   <div style='display:none;'>

.. activecode:: list6_pre

   groceries = ['milk', 'eggs', 'chocolate!', 'Doritos!', 'bread']

.. raw:: html

   </div>

.. question:: list6_q

    .. tabbed:: 6_tabs

        .. tab:: Question

            .. activecode:: list6
               :include: list16_pre

               Write a line of code to replace the element at index 1 of a previously-defined
               list ``groceries`` with the string 'chocolate milk'.
               
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(groceries[1], 'chocolate milk')
                      self.assertEqual(len(groceries), 5)
               myTests().main()

        .. tab:: Hint

	   To replace an element in a list, access that element on the left-hand-side of an assignment statement.

        .. tab:: Answer

           .. activecode:: list6_a
              :nocanvas:
              :include: list6_pre

	      groceries[1] = 'chocolate milk'

.. question:: list7_q

    .. tabbed:: list7_tabs

        .. tab:: Question

            .. activecode:: list7
               :include: list6_pre

               Write code that removes the first item (at index 0) from a list ``groceries``
	       and adds that item back at the end of the list.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(groceries), 5)
                      self.assertEqual(groceries[-1], 'milk')
                      self.assertEqual(groceries[-2], 'bread')
                      self.assertEqual(groceries[0], 'eggs')
               myTests().main()

        .. tab:: Hint

	   Use two lines of code.  Use ``pop()`` in the first line, and ``append()`` in the second.

        .. tab:: Answer

           .. activecode:: list7_a
              :nocanvas:
              :include: list6_pre

	      item = groceries.pop(0)
	      groceries.append(item)

.. question:: list8_q

    .. tabbed:: list8_tabs

        .. tab:: Question

            .. activecode:: list8
               :include: list6_pre

               Write code to remove the last item of the list ``groceries`` and insert it
               in the middle of the list.  Assume the list has an odd number of elements
               before removing the last item (and, thus, an even number of elements after
               removing the last item).  (Hint: use integer division ``//``.)
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(groceries), 5)
                      self.assertEqual(groceries[0], 'milk')
                      self.assertEqual(groceries[1], 'eggs')
                      self.assertEqual(groceries[2], 'bread')
                      self.assertEqual(groceries[3], 'chocolate!')
                      self.assertEqual(groceries[4], 'Doritos!')
               myTests().main()

        .. tab:: Hint

	   Use multiple lines of code.  First, ``pop()`` the last item off and store it
           in a variable.  Then, get the length of the list.  Then insert the item back
           into the list in the middle.

        .. tab:: Answer

           .. activecode:: list8_a
              :nocanvas:
              :include: list6_pre

	      item = groceries.pop()
              listlen = len(groceries)
	      groceries.insert(listlen // 2, item)

.. question:: list9_q

    .. tabbed:: list9_tabs

        .. tab:: Question

            .. activecode:: list9
               :include: list6_pre

               Write code to swap the first and last items in the list ``groceries``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(groceries), 5)
                      self.assertEqual(groceries[0], 'bread')
                      self.assertEqual(groceries[1], 'eggs')
                      self.assertEqual(groceries[2], 'chocolate!')
                      self.assertEqual(groceries[3], 'Doritos!')
                      self.assertEqual(groceries[4], 'milk')
               myTests().main()

        .. tab:: Hint

	   Do this in 4 steps: remove the last item and store in a variable.  Remove the first
           item and store in a variable.  Then, in two lines of code, add the items back to the list,
           using ``insert()`` and ``append()``.

        .. tab:: Answer

           .. activecode:: list9_a
              :nocanvas:
              :include: list6_pre

	      firstitem = groceries.pop(0)
              lastitem = groceries.pop()
              groceries.insert(0, lastitem)
              groceries.append(firstitem)

.. raw:: html

   <div style='display:none;'>

.. activecode:: list10_pre

   clothes = ['socks', 'leggings']

.. raw:: html

   </div>

.. question:: list10_q

    .. tabbed:: list10_tabs

        .. tab:: Question

            .. activecode:: list10
               :include: list6_pre list10_pre

               Write code to create a new list ``allitems`` that is the concatenation of 
               list ``groceries`` and list ``clothes``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(len(allitems), 7)
                      self.assertEqual(allitems[0], 'milk')
                      self.assertEqual(groceries[4], 'bread')
                      self.assertEqual(groceries[5], 'socks')
                      self.assertEqual(groceries[6], 'leggings')
               myTests().main()

        .. tab:: Hint

	   You can concatenate lists using ``+``.

        .. tab:: Answer

           .. activecode:: list10_a
              :nocanvas:
              :include: list6_pre list10_pre

              allitems = groceries + clothes

.. question:: list11_q

    .. tabbed:: list11_tabs

        .. tab:: Question

            .. activecode:: list11
               :include: list6_pre

               Given a list ``groceries``, print out the item from the list with the
               minimum value and the index of where that item is in ``groceries``.
               ~~~~
               # replace this comment with your code
               ====

        .. tab:: Hint

	   Use ``min(groceries)`` to find the minimum item.  Use ``index()`` to get the index of
           that item.

           The answer should be ``Doritos! 3``.

        .. tab:: Answer

           .. activecode:: list11_a
              :nocanvas:
              :include: list6_pre

              minItem = min(groceries)
              location = groceries.index(minItem)
              print(minItem, location)

.. raw:: html

   <div style='display:none;'>

.. activecode:: list12_pre

   scores = [78, 44, 99, 93, 86, 91, 68, 68, 90, 82, 85, 79, 77, 72, 94]

.. raw:: html

   </div>

.. question:: list12_q

    .. tabbed:: list12_tabs

        .. tab:: Question

            .. activecode:: list12
               :include: list12_pre

               Given a list ``scores``, write code to store the average in a variable
               called ``average_score``.  Then, print ``average_score``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertEqual(average_score, sum(scores) / len(scores))
               myTests().main()

        .. tab:: Hint

	   Use ``sum(scores)`` and ``len(scores)`` in your computation.

        .. tab:: Answer

           .. activecode:: list12_a
              :nocanvas:
              :include: list12_pre

              average_score = sum(scores) / len(scores)
              print(average_score)
