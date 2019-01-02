Dictionary Basics
::::::::::::::::::::::::::::


.. question:: dict1_q
   :number: 1

   .. tabbed:: dict1_tabs

        .. tab:: Question

            .. activecode:: dict1

               Write code to create a dictionary ``grades`` that maps a student's name
               to their assignment grade.  ``grades`` has two entries in it:

               `Sam Reimer --> 84.3`

               `Steve Bardeau --> 90.5`
               
	       
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertIs(type(grades), dict)
                      self.assertEqual(len(grades), 2, 'dictionary must have 2 entries in it')
                      self.assertAlmostEqual(grades['Sam Reimer'], 84.3)
                      self.assertAlmostEqual(grades['Steve Bardeau'], 90.5)
               myTests().main()

        .. tab:: Hint

           You create a dictionary with ``{`` and ``}``, and you put entries in it separating the
           key from the value with ``:``.

        .. tab:: Answer

           .. activecode:: dict1_a
              :nocanvas:

              grades = { 'Sam Reimer': 84.3, 'Steve Bardeau': 90.5 }
              
.. raw:: html

   <div style='display:none;'>

.. activecode:: dict2_pre

   grades = { 'Sam Reimer': 84.3, 'Steve Bardeau': 90.5, 'Colette Gonzales': 94.5 }

.. raw:: html

   </div>

.. question:: dict2_q

   .. tabbed:: dict2_tabs

        .. tab:: Question

            .. activecode:: dict2
               :include: dict2_pre

               Write code to retrieve from dictionary ``grades`` the grade of 'Colette Gonzales'. Store
               her grade in a variable ``colette_score``.
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertIs(type(grades), dict, 'grades is a dictionary')
                      self.assertAlmostEqual(colette_score, 94.5, 'colette_score has the correct value')
               myTests().main()

        .. tab:: Hint

           Suppose you have a dictionary ``aDict``. You can print the value with key ``key`` by
           doing ``print(aDict[key])``

        .. tab:: Answer

           .. activecode:: dict2_a
              :nocanvas:
              :include: dict2_pre

              colette_score = grades['Colette Gonzales']
              

.. question:: dict3_q

   .. tabbed:: dict3_tabs

        .. tab:: Question

            .. activecode:: dict3

               Write code to map floating point numbers to strings in a dictionary `posOrNeg`,
               initially containing these entries:

	       `-3.14 --> 'negative'`

	       `40.79 --> 'positive'`

	       `0.01  --> 'positive'`
               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertIs(type(posOrNeg), dict, 'posOrNeg is a dictionary')
                      self.assertEqual(len(posOrNeg), 3, 'posOrNeg has 3 entries')
                      self.assertEqual(posOrNeg[-3.14], 'negative')
                      self.assertEqual(posOrNeg[40.79], 'positive')
                      self.assertEqual(posOrNeg[0.01], 'positive')
               myTests().main()

        .. tab:: Hint

           You create a dictionary with ``{`` and ``}``, and you put entries in it separating the
           key from the value with ``:``.

        .. tab:: Answer

           .. activecode:: dict3_a
              :nocanvas:

              posOrNeg = { -3.14: 'negative',
                           40.79: 'positive',
                            0.01: 'positive' }
              
.. question:: dict4_q

   .. tabbed:: dict4_tabs

        .. tab:: Question

            .. activecode:: dict4
               :include: dict2_pre

               Given a dictionary ``grades``, write code to add an entry mapping `John Fleenor`
               to the grade `92.5`.

               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertIs(type(grades), dict, 'grades is a dictionary')
                      self.assertEqual(len(grades), 4, 'grade has 4 entries')
                      self.assertAlmostEqual(grades['John Fleenor'], 92.5)
               myTests().main()

        .. tab:: Hint

           After a dictionary has been created you add entries using the syntax:

	   ``aDict[key] = value``
           

        .. tab:: Answer

           .. activecode:: dict4_a
              :nocanvas:
              :include: dict2_pre

	      grades['John Fleenor'] = 92.5
              
.. question:: dict5_q

   .. tabbed:: dict5_tabs

        .. tab:: Question

            .. activecode:: dict5
               :include: dict2_pre

               Given a dictionary ``grades`` containing a mapping of `Sam Reimer` to 
               the grade `84.3`, update the dictionary to change the grade to `94.3`.

               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertIs(type(grades), dict, 'grades is a dictionary')
                      self.assertEqual(len(grades), 3, 'grades has 3 entries')
                      self.assertAlmostEqual(grades['Sam Reimer'], 94.3)
               myTests().main()

        .. tab:: Hint

           After a dictionary has been created you can update an entry using the syntax:

	   ``aDict[key] = value``

	   (Just like creating a new entry.)

        .. tab:: Answer

           .. activecode:: dict5_a
              :nocanvas:
              :include: dict2_pre

	      grades['Sam Reimer'] = 94.3
              
.. question:: dict6_q

   .. tabbed:: dict6_tabs

        .. tab:: Question

            .. activecode:: dict6
               :include: dict2_pre

               Given a dictionary ``grades`` containing a mapping of `Sam Reimer` to a
               floating point number, write code to add 1 to the grade.

               ~~~~
               # replace this comment with your code
               ====
               from unittest.gui import TestCaseGui
               class myTests(TestCaseGui):
                  def testOne(self):
                      self.assertIs(type(grades), dict, 'grades is a dictionary')
                      self.assertEqual(len(grades), 3, 'grades has 3 entries')
                      self.assertAlmostEqual(grades['Sam Reimer'], 85.3)
               myTests().main()

        .. tab:: Hint

           Your code will have to access the value, add one to 1, and then update the entry.
           This can be done in one line of code.

        .. tab:: Answer

           .. activecode:: dict6_a
              :nocanvas:
              :include: dict2_pre

	      grades['Sam Reimer'] = grades['Sam Reimer'] + 1
              
