 ## Making the Die using Wolfram in the Browser

Now we will build the dice roller.

If you are using Wolfram in the desktop application, skip this step and go to 'Making the Die using Wolfram Desktop'.

We will build the dice roller in the same way we built the coin flipper.

---task---

First, we'll need images for each side of the die. Right click on each of these images and save them to your desktop. Drag the images from your desktop into your notebook.

![Dice 1](images/Dice1.png)
![Dice 2](images/Dice2.png)
![Dice 3](images/Dice3.png)
![Dice 4](images/Dice4.png)
![Dice 5](images/Dice5.png)
![Dice 6](images/Dice6.png)

Assign each image to a variable name: `one`, `two`, `three`, `four`, `five`, `six`.
Put the variables into a list, and assign the list to the variable name `diceOptions`.

```
diceOptions = {one, two, three, four, five, six}
```
---/task---

In order to roll the dice, just like we did earlier to create a coin flipper, all we have to do is set up a `RandomChoice` between the six options in the list.

--- task ---
Use `RandomChoice` to randomly pick one of the sides in the list.

```
RandomChoice[diceOptions]
```

--- /task ---

--- task ---
Take the code you wrote to create a button for the coin flipper, and alter it to roll the die instead.

![Dynamic Button Dice](images/ButtonDynamicDice.png)

--- /task ---
