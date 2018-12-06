Input and Output
:::::::::::::::::::::::::::

.. question:: io1_q
   :number: 1

   .. tabbed:: io1_tabs

        .. tab:: Question

            .. activecode:: io1

               Write code to print ``Hello, World``
               ~~~~

        .. tab:: Hint

           Use the print() function, and remember that strings are surrounded by double-quotes or single-quotes.

        .. tab:: Answer

           .. activecode:: io1_a
              :nocanvas:

              print("Hello, World")
              # or print('Hello, World')

.. question:: io2_q

   .. tabbed:: io2_tabs

        .. tab:: Question

            .. activecode:: io2

               Write code to print

                  ``Hello``
                  
                  ``World``

               using 2 print statements.
               ~~~~

        .. tab:: Hint

           Call ``print()`` twice, on two consecutive lines.

        .. tab:: Answer

           .. activecode:: io2_a
              :nocanvas:

              print("Hello")
              print("World")


.. question:: io3_q

   .. tabbed:: io3_tabs

        .. tab:: Question

            .. activecode:: io3

               Write code to print

                  ``Hello``

               leaving the cursor on the same line.
               ~~~~

        .. tab:: Hint

           You have to use the optional parameter, ``end``, in the print statement.

        .. tab:: Answer

           .. activecode:: io3_a
              :nocanvas:

              print("Hello", end='')


.. question:: io4_q

   .. tabbed:: io4_tabs

        .. tab:: Question

            .. activecode:: io4

               Assume you have a variable ``ranking`` set to some integer value. 
               Write a line of code to print the value of ``ranking``.
               ~~~~
               ranking = 99
               # Replace this comment with your code
               ====

        .. tab:: Hint

           ``print()`` evaluates each variable or expression before printing it.

        .. tab:: Answer

           .. activecode:: io4_a
              :nocanvas:

              print(ranking)

.. raw:: html

   <div style='display:none;'>

.. activecode:: io5_pre

   ranking = 32
   average = 34

.. raw:: html

   </div>

.. question:: io5_q

   .. tabbed:: io5_tabs

        .. tab:: Question

            .. activecode:: io5
               :include: io5_pre

               Assume you have two variables ``ranking`` and ``average`` set to some values. 
               Write a line of code to print the values with a single space between.
               ~~~~
               # Replace this comment with your code.
               ====

        .. tab:: Hint

           The comma in ``print('x', 'y')`` will automatically insert a space between the two values

        .. tab:: Answer

           .. activecode:: io5_a
              :nocanvas:
              :include: io5_pre

              print(ranking, average)


.. question:: io6_q

   .. tabbed:: io6_tabs

        .. tab:: Question

            .. activecode:: io6

               Assume you have two variables ``start`` and ``interval``. Write a line of 
               code to print the sum of the two values.
               ~~~~
               start = 103233.1
               interval = 201787.33
               # Replace this comment with your code.
               ====

        .. tab:: Hint

           You can put expressions, like ``x + y`` into a ``print`` statement, too.

        .. tab:: Answer

           .. activecode:: io6_a
              :nocanvas:

              print(start + interval)

.. question:: io7_q

   .. tabbed:: io7_tabs

        .. tab:: Question

            .. activecode:: io7

               Assume you have a variable ``ranking`` set to some integer value.  
               Write a line of code to print ``Ranking:`` followed by 
               the value that ``ranking`` refers to.  Note that there should be 
               one space between the ``:`` and the value.
               E.g., if ``ranking`` was 7, the output would be ``Ranking: 7``.
               ~~~~
               ranking = 7
               # Replace this comment with your code.
               ====

        .. tab:: Hint

           Remember, the comma in a ``print`` adds a space, so be careful!

        .. tab:: Answer

           .. activecode:: io7_a
              :nocanvas:

              print('Ranking:', ranking)

.. raw:: html

   <div style='display:none;'>

.. activecode:: io8_pre

   name = 'Joe McDonald'
   score = 7

.. raw:: html

   </div>

.. question:: io8_q

   .. tabbed:: io8_tabs

        .. tab:: Question

            .. activecode:: io8
               :include: io8_pre

               Assume you have a variable ``name`` set to a student's name, and
               a variable ``score`` set to the score the student got on the last quiz.
               Write a line of code to print out the student's name and the student's score, 
               in the following format.
               Name: Joe McDonald Score: 7
               where the student's name is `Joe McDonald` and the student's score is `7`.
               ~~~~
               # Replace this comment with your code.
               ====

        .. tab:: Hint

           You can pass as many parameters as you want to ``print``, separated by commas.

        .. tab:: Answer

           .. activecode:: io8_a
              :nocanvas:
              :include: io8_pre

              print('Name:', name, 'Score:', score)

.. question:: io9_q

   .. tabbed:: io9_tabs

        .. tab:: Question

            .. activecode:: io9

               Write code to read in a string value from the user, storing the result
               in a variable ``name``.
               ~~~~
               # Replace this comment with your code.
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertIs(type(name), str, 'variable must be a str')

               myTests().main()

        .. tab:: Hint

           Use ``input()``.  You do *NOT* have to convert the result to a string, because
           ``input()`` returns a string.

        .. tab:: Answer

           .. activecode:: io9_a
              :nocanvas:

              name = input()
              # or, better: name = input("Enter a name: ")

.. question:: io10_q

   .. tabbed:: io10_tabs

        .. tab:: Question

            .. activecode:: io10

               Write code to prompt the user for a score, reading in the score into a variable
               ``score``.  The type of score should be a ``float``.

               ~~~~
               # Replace this comment with your code.
               ====
               from unittest.gui import TestCaseGui

               class myTests(TestCaseGui):

                  def testOne(self):
                      self.assertIs(type(score), float, 'variable must be a float')

               myTests().main()

        .. tab:: Hint

           Use ``input()``.  You have to convert the result to a float, because
           ``input()`` returns a string.

        .. tab:: Answer

           .. activecode:: io10_a
              :nocanvas:

              score = float(input('Enter a score: '))
              # or, 
              # print("Enter a score: ", end='')
              # score = float(input())
