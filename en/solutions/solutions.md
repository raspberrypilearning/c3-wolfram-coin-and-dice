## Solutions

![coin set up](images/setup.png)

```
coinOptions = {heads, tails};
```

Either:

![dice set up](images/dicelist.png)

Or:

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

```
diceOptions = {one, two, three, four, five, six}
```

```
Grid[
 {
  {dice = one;
   Button["Roll the Dice", 
    dice = RandomChoice[diceOptions]],
    
   coin = heads;
   Button["Flip the Coin", 
    coin = RandomChoice[coinOptions]]
   },
  
  {Dynamic[dice], Dynamic[coin]}
  }
 ]
 ```
 
 Challenge
 
 ```
 Manipulate[
 Grid[{RandomChoice[{one, two, three, four, five, six}, i]}], {{i, 1, 
   "Number of Rolls"}, 1, 6, 1, ControlType -> RadioButton}] 
```