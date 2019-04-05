## Make the dice
Now, you will build the dice roller.

Each face (side) on a die is made up of nine squares, and some squares have circles in them to show the number on that face of the die.

You can use `Grid` and `Graphics` to make the faces of the die.

Look at this example of `Grid`.

![Grid](images/Grid.png)

`Grid` is made up of a list of lists, where each list becomes a row in the grid.

You can use `Graphics` and `Disk` to make a circle. 

![Graphics Disk](images/GraphicsDisk.png)

--- task ---

Create a variable of a `Graphics[Disk[]]` called dot.

```dot = Graphics[Disk[]]```

--- /task ---

You will now create the number 1 side of a die. To begin with, type in the following line of code:

![Random Choice](images/GridGraphicsDisk1.png)

Now, make all the squares inside the grid the same size. To do this, put in the `ItemSize`, to make sure that the disk and the `Null` gaps are all the same size.

![Random Choice](images/GridGraphicsDisk2.png)

Perfect! Now, remove the `Frame` to make it look a bit more like a die.

![Random Choice](images/GridGraphicsDisk3.png)

`Panel` puts a very nice grey background around objects, so add in `Panel` to improve the appearance of your die.

![Random Choice](images/GridGraphicsDisk4.png)


--- task ---

Make each of the six sides of the die, and assign each side to a variable name.


```
dot = Graphics[Disk[]];

one = Panel[
  Grid[{{Null, Null, Null}, {Null, dot, Null}, {Null, Null, Null}}, 
   ItemSize -> {2, 2}]];
   
two = Panel[
  Grid[{{dot, Null, Null}, {Null, Null, Null}, {Null, Null, dot}}, 
   ItemSize -> {2, 2}]];
   
three = Panel[
  Grid[{{dot, Null, Null}, {Null, dot, Null}, {Null, Null, dot}}, 
   ItemSize -> {2, 2}]];

four = Panel[
  Grid[{{dot, Null, dot}, {Null, Null, Null}, {dot, Null, dot}}, 
   ItemSize -> {2, 2}]];


five = Panel[
  Grid[{{dot, Null, dot}, {Null, dot, Null}, {dot, Null, dot}}, 
   ItemSize -> {2, 2}]];

six = Panel[
  Grid[{{dot, dot, dot}, {Null, Null, Null}, {dot, dot, dot}}, 
   ItemSize -> {2, 2}]];
   
```
--- /task ---

--- task ---

Make a list which contains all of the sides of the die, and assign it the variable name `diceOptions`.

```
diceOptions = {one, two, three, four, five, six}
```

--- /task ---

To roll the dice, set up a `RandomChoice` between the options in the list, just like you did when you created the coin flipper.

--- task ---
Use `RandomChoice` to randomly pick one of the sides in the list.

```
RandomChoice[diceOptions]
```

--- /task ---

--- task ---
Copy the code you wrote to create a button for the coin flipper, and change it so that it rolls the die.

![Dynamic Button Dice](images/ButtonDynamicDice.png)

--- hints ---
--- hint ---

To create a dynamic button for your coin-flipper, you created a button and then marked the `coin` variable as dynamic, like this:

```
coin = heads;
Button["Flip Coin", 
 coin = RandomChoice[coinOptions]]
Dynamic[coin]
```
--- /hint ---
--- /hints ---
--- /task ---
