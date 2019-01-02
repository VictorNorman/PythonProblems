While Loops
:::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: while1_pre

   groceries = ['milk', 'bread', 'eggs', 'chocolate (dark)']

.. raw:: html

   </div>

.. question:: while1_q
   :number: 1

    .. tabbed:: while1_tabs

        .. tab:: Question

            .. activecode:: while1
               :include: while1_pre

               Assume a list ``groceries`` has been defined. Replace ``<1>`` and
               ``<2>`` in the code below so that the code prints out each item in the list. 

               ~~~~
               idx = 0
               while <1>:
                   print(groceries[idx])
                   <2>
               ====

        .. tab:: Hint

           For ``<1>``, you must provide a condition that will be true when ``idx`` is
           a viable index into ``groceries``.

           For ``<2>``, the code should increment the value of ``idx``.

        .. tab:: Answer

           .. activecode:: while1_a
              :nocanvas:
              :include: while1_pre

              idx = 0
              while idx < len(groceries):
                  print(groceries[idx])
                  idx += 1      # or idx = idx + 1


.. question:: while2_q

    .. tabbed:: while2_tabs

        .. tab:: Question

            .. activecode:: while2

               Write code to ask the user to type the letter ``y`` and keep
               asking the user to enter the letter ``y`` until they do.
               ~~~~
               letter = input('Enter the letter y: ')
               # put a while loop here.
               ====

        .. tab:: Hint

           You have to ask the user to enter a letter again inside the ``while`` loop.

        .. tab:: Answer

           .. activecode:: while2_a
              :nocanvas:

              letter = input('Enter the letter y: ')
              while letter != 'y':
                  letter = input('Enter the letter y: ')

.. question:: while3_q

    .. tabbed:: while3_tabs

        .. tab:: Question

            .. activecode:: while3
               
               Write code to ask the user for an integer or to enter the number 0 to quit.

               When the user enters an integer, print out the number
               squared. E.g.,
               ::

                    Enter an integer, or 0 to quit: 12
                    12 squared is 144
                    Enter an integer, or 0 to quit: 0
                    Thanks for playing.

               .. note:: In this environment, you won't see output from your print statement until the program ends.
               ~~~~

               ====

        .. tab:: Hint

           Figure out what your condition for the while loop will be. I.e.,
           when do you want to asking the user for another number.

           You will have to repeat your ``input()`` call inside the
           ``while`` loop.

        .. tab:: Answer

           .. activecode:: while3_a
              :nocanvas:

              num = int(input('Enter an integer, or 0 to quit: '))
              while num != 0:
                  print(num, 'squared is', num * num)
                  num = int(input('Enter an integer, or 0 to quit: '))

.. question:: while4_q

    .. tabbed:: while4_tabs

        .. tab:: Question

            .. activecode:: while4

               Write a short program that asks the user to enter a positive
               number, and then repeatedly doubles that number until the
               result is more than 1 million. The program then prints out
               how many times the number was doubled.  E.g.,
	       ::
               Enter a positive number: 2
               Your number was doubled 19 times before the result was greater than 1000000

               ~~~~

               ====

        .. tab:: Hint

           What is the condition that will stop the while loop?

           You need to create a variable, say, ``numTimesDoubled``, that
           you will increment each time in the while loop.

        .. tab:: Answer

           .. activecode:: while4_a
              :nocanvas:

              num = float(input("Enter a positive number: "))
              numTimesDoubled = 0
              while num < 1000000:
                  num = num * 2     # or num *= 2
                  numTimesDoubled += 1
              print('Your number was doubled', numTimesDoubled, 'times before the result was greater than 1000000')


.. question:: while5_q

    .. tabbed:: while5_tabs

        .. tab:: Question

            .. activecode:: while5
               :include: while1_pre

               Convert the following index-based for loop to use a while loop::               

	               for idx in range(len(groceries)):
        	           print(groceries[idx])

               ~~~~
               idx = 0
               # replace this comment with your code
               ====

        .. tab:: Hint

           Figure out the condition for the ``while`` loop: you want the ``while``
           loop to continue as long as ``idx`` is legal -- i.e., until is 
           the index of the last element in ``groceries``.

        .. tab:: Answer

           .. activecode:: while5_a
              :nocanvas:
              :include: while1_pre

              idx = 0
              while idx < length(groceries):
                  print(groceries[idx])
                  idx += 1


.. question:: while6_q

    .. tabbed:: while6_tabs

        .. tab:: Question

            .. activecode:: while6
               :include: while1_pre

               Convert the following code to use a while loop::               

	               for item in groceries:
        	           print(item)

               ~~~~
               idx = 0
               # replace this comment with your code
               ====

        .. tab:: Hint

           You will have to use index-based looping, incrementing
           ``idx`` inside the while loop.

        .. tab:: Answer

           .. activecode:: while6_a
              :nocanvas:
              :include: while1_pre

              idx = 0
              while idx < length(groceries):
                  print(groceries[idx])
                  idx += 1




