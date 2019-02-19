## Building An Interface

Now that we have two buttons, one which flips a coin and one which rolls a die, we can combine them into an interface.
We can construct this using `Grid`.
Look at this example of `Grid`.

![Complete](images/complete.png)

`Grid` is made up of a list of lists, where each list becomes a row in the grid.

--- task ---

Replace `expression` with your code for the `RandomChoice`. You don't need to include a `Button`.

--- /hint---
--- hint ---

You should have created a `Manipulate` with a slider to change the number of dice.
Look in the documentation for `Manipulate` to work out how to change the `Control Type` to a `Radio Button`.

--- /hint---
--- hint ---

Give your `Manipulate` buttons a name, like "Number of Rolls".

--- /hint---

--- hint ---
```
Manipulate[Grid[{RandomChoice[{one, two, three, four, five, six}, i]}], {{i, 1, "Number of Rolls"}, 1, 6, 1, ControlType -> RadioButton}]
```
--- /hint---

---/hints---
