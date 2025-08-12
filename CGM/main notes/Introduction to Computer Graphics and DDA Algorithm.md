# Computer graphics
* Is the field of computer science that deals with creating, manipulating and displaying visual content using computers.

* When we draw a line on paper it is continuous but on a computer screen which is made of pixels, lines are drawn by turning on specific pixels that based match the lines

- Pixels are small screen pixel elements. 

- This is where these line drawing algorithms enter to decide which pixel to turn on between two points to form a line
	- DDA Algorithm(Digital Differential Analyzer): This is a simple step by step method to draw a line by incrementing x or y by small amounts and calculating the corresponding y or x value

# DDA Algorithm
DDA is step-by-step method to draw a line by incrementing x or y by small amounts and calculating the corresponding y or x value. 

# How DDA works
1. Find slop of the line. 
   $\text{slope}  = \frac{dy}{dx}$
2. Decide the number of steps based on the longer distance:
   Steps = max($|dx|$, $|dy|$) // basically max function in many programming languages 
3. Increment x and y for each step:
   x = x + x<sub>increment</sub>
   y = y + y<sub>increment</sub>
4. Plot the pixel at each (x, y) position using putpixel() (function in <graphics.h> in C)

### Example 
We want to draw a line from point (2,3) to (10,7) using the DDA algorithm.
-  We will first from pixel (2, 3) and move pixel by pixel towards (10, 7) by calculating which pixels to turn ON.

**STEP I**: Find slope of the line
$\text{slope} = \frac{dy}{dx}$
To calculate $dx$ and $dy$
$dx = x_2 - x_1 = 10 -2 = 8$
$dy = y_2 - y_1 = 7 - 3 = 4$

We will move 8 steps in x-direction and 4 steps in y-direction


**STEP II:** Find the number of steps
We will take the maximum of $dx$ and $dy$
```
steps = max(dx, dy)
	= max(8, 4)
	= 8
```

**STEP III:*** Find x-increment and y-increment
We calculate how much to move in x and y for each scale
$x_{increment} = \frac{dx}{steps} = 8/8 = 1.0$
$y_{increment} = \frac{dy}{steps} = 4/8 = 0.5$
For every one pixel step in x-axis we will move 0.5 pixels in y

**STEP IV:** Start from (2, 3)
We begin at (x, y) = (2, 3)
Then, we keep adding $x_{increment}$ and $y_{increment}$ in each step and round the values to plot pixels.



| Steps | x   | y   | Rounded pixel |
| ----- | --- | --- | ------------- |
| 0     | 2.0 | 3.0 | (2, 3)        |
| 1     | 3.0 | 3.5 | (3, 4)        |
| 2     | 4.0 | 4   | (4, 4)        |
| 3     | 5   | 4.5 | (5, 5)        |
| 4     | 6   | 5   | (6, 5)        |
| 5     | 7   | 5.5 | (7, 6)        |
| 6     | 8   | 6   | (8, 6)        |
| 7     | 9   | 6.5 | (9, 7)        |
| 8     | 10  | 7   | (10, 7)       |
