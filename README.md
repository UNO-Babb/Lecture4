# Lecture 4 - CIST 1600
## Objectives:
- Demonstrate Turtle Graphics
- Create algorithms with Turtle

### Accessing the Turtle
- You can use the IDE in your computer or CodeHS's Sandbox
- Github Code Space will not work since it does not have a graphical componenet
- [CodeHS Sandbox](https://codehs.com/explore/sandbox/python)

### Turtle Graphics
Drawing with a "turtle" is a popular way to visualize algorithms. It was part of the original Logo programming language developed in the 1960s by Wally Feruzig and Seymour Papert. Originally, a turtle was a robot that used a marker to make lines on a sheet of paper.

```
>>> import turtle
>>> bob = turtle.Turtle() #bob is a Turtle
>>> bob.forward(100)
```

### Turtle Methods
What can you do with a turtle? Any of these methods work:

| METHOD |PARAMETER |	DESCRIPTION |
| --- | --- | --- |
|Turtle()	| None | Creates and returns a new tutrle object|
|forward() |	amount | Moves the turtle forward by the specified amount|
|backward() | amount | Moves the turtle backward by the specified amount|
|right() |	angle |	Turns the turtle clockwise|
|left() |	angle |	Turns the turtle counter clockwise|
|penup() |	None |	Picks up the turtle’s Pen|
|pendown() |	None |	Puts down the turtle’s Pen|
|up() |	None |	Picks up the turtle’s Pen|
|down() |	None |	Puts down the turtle’s Pen|
|color() |	Color name |	Changes the color of the turtle’s pen|
|fillcolor() |	Color name |	Changes the color of the turtle will use to fill a polygon|
|heading() |	None |	Returns the current heading|
|position() |	None |	Returns the current position|
|goto()	| x, y |	Move the turtle to position x,y|
|begin_fill() |	None |	Remember the starting point for a filled polygon|
|end_fill() |	None |	Close the polygon and fill with the current fill color|
|dot() |	None |	Leave the dot at the current position|
|stamp() |	None |	Leaves an impression of a turtle shape at the current location|
|shape() |	shapename |	Should be ‘arrow’, ‘classic’, ‘turtle’ or ‘circle’|

### Algorithms with Turtles
How can we use these commands to make shapes?  
An **Algorithm** is a process or set of rules to be followed in calculations or other problem-solving operations, especially by a computer.

```
>>> bob = turtle.Turtle()
>>> for i in range(4):
...     bob.forward(100)
...     bob.right(90)
...
```
![Square Turtle](square.PNG)

How could we make the following shape:  
![Star Turtle](star.PNG)

### Functions
In python, we can define functions. This can be useful in removing code that is repeated in multiple places in your program and placing it in a function. Functions can be used multiple times throughout your code.

```
def drawSquare(myTurtle):
  for i in range(4):
    myTurtle.forward(100)
    myTurtle.right(90)
```
Notice in this function that the ***myTurtle*** is in the parenthesis. This is an argument, you will have to put the name of your turtle in the parenthesis when you call this function.
```
bob = turtle.Turtle()
drawSquare(bob)
```

Finally, we can add parameters to make the drawSquare function more general. In this case, we will add a second parameter for the **size** of the sides.
```
def drawSquare(myTurtle, size):
  for i in range(4):
    myTurtle.forward(size)
    myTurtle.right(90)
```
### Challenge:
Create a *X-Y* grid using the turtle.
- Use the draw square tool to create each square.
- Create a function that generates a column of *Y* squares.
- Create a function that generates a row of *X* columns.
- Can you get X and Y from user input?
