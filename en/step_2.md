## Creating a Coin Flipper

First, we will be building the coin flipper. The coin flipper is fairly simple: we want to be able to press a button and randomly return either heads or tails.

--- task ---

First, we'll need images of both heads and tails. Right click on each of these images and save them to your desktop. Drag the images from your desktop into your notebook. If you are using a desktop version of Wolfram, you can drag and drop the images straight into your notebook.

You could also search on the internet for a a different coin, maybe in your own currency.

![Heads](images/Head.png)
![Tails](images/Tail.png)

Assign each coin a variable name. `heads` for the head coin, and `tails` for the tail coin. Use a `;` after each line to supress the output, otherwise the image of the coin will print whenever you run this code.

![Set Up](images/setup.png)

--- /task ---

We need a list of the coin options.

Lists start with `{` and end with `}`, and each element is separated by a `,`.

--- task ---
Make a list which contains your coins.

Assign this list to the variable name `coinOptions`.

![Making a List](images/assigningvariables.png)

--- /task ---

We want to be able to flip the coin and randomly get either heads or tails. We do this using `RandomChoice`.

```
RandomChoice[coinOptions]
```

It would be useful to have a button for the user to press in order to flip the coin.

--- task ---
Create a button which randomly outputs either Heads or Tails.

```
Button["Flip Coin", 
 Print[RandomChoice[coinOptions]]]
```
--- /task ---

You might notice that every time you press the button, the new output appears underneath the old output. It would be better to replace the old output with the new output each time you press the button.

We do this using `Dynamic`. `Dynamic` displays the updated value, so each time we reevaluate the code by pressing the button, `Dynamic` will update to the new value.

--- task ---
Use `Dynamic` to create a button. 

```
coin = heads;
Button["Flip Coin", 
 coin = RandomChoice[coinOptions]]
Dynamic[coin]
```
--- /task ---

Replace your old button with the new Dynamic one.
