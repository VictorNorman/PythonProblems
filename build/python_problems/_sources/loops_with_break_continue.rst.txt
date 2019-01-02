Loops with continue and break statements
::::::::::::::::::::::::::::::::::::::::

.. raw:: html

   <div style='display:none;'>

.. activecode:: break1_pre

   groceries = ['milk', 'bread', 'jalapeno peppers', 'ghee', 'almonds', \
   'chicken thighs', 'eggs', 'chocolate (dark)']

.. raw:: html

   </div>

.. question:: break1_q
   :number: 1

    .. tabbed:: break1_tabs

        .. tab:: Question

           .. activecode:: break1
              :include: break1_pre

              Write code to search through a list ``groceries`` for the
              string "eggs". When you find "eggs" in the list,
              print ``Found it!`` and discontinue searching by using
              ``break``.  If "eggs" is not found in the list, nothing is printed.
              ~~~~
              ====

        .. tab:: Hint

           Use a ``for`` loop, containing an ``if`` statement, containing the ``break`` statement.

        .. tab:: Answer

           .. activecode:: break1_a
              :nocanvas:
              :include: break1_pre

              for item in groceries:
                  if item == 'eggs':
                      print("Found it!")
                      break

.. question:: break2_q

    .. tabbed:: break2_tabs

        .. tab:: Question

           .. activecode:: break2
              :include: break1_pre

              Write code to search through a list ``groceries`` for the
              string "eggs". When you find "eggs" in the list,
              print ``Found it at index <n>`` (where <n> is the index of
              where "eggs" was found) and discontinue searching by using
              ``break``.
              ~~~~
              ====

        .. tab:: Hint

           Use an index-based ``for`` loop.  If you need more hints, see
           the previous question's hint.

        .. tab:: Answer

           .. activecode:: break2_a
              :nocanvas:
              :include: break1_pre

              for idx in range(len(groceries)):
                  if groceries[idx] == 'eggs':
                      print("Found it at index", idx)
                      break



