## Challenge: Build a Manipulate

Build a `Manipulate` function which allows the user to roll between 1 and 6 dice at the same time.

![Complete](images/complete.png)

--- hints ---
--- hint ---
Look up how `Manipulate` is used in the documentation.

```Manipulate[expression,{u,minimum u, maximum u, size of steps}]```

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
