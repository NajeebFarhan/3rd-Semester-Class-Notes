---
Subject: "[[Computer Graphics and Multemedia]]"
tags:
  - coa
chapter/unit: 
related links: 
date: 2025-08-11
---

---

# Bresenham's Line Drawing Algorithm
- Bresenham's algorithm is a method used in computer graphics to draw straight lines on a pixel based screen.
- It is fast since since it uses only integers, no floating point math.
- It is accurate since it makes the line look as close as possible to the real line.


## Working of Bresenham's line drawing algorithm
For slope $0 < m < 1$

1. Input
	We give the algorithm 2 points:
	- Starting point: $(x_o, y_o)$
	- Ending point: $(x_1, y_1)$ or $(x_n, y_n)$
	
2. Calculate how far the line travels:
	$\Delta x = x_1 - x_o$, how far the line goes sideways
	$\Delta y = y_1 - y_o$, how far the line goes upwards.
	
3. Initialize the decision parameter($P_k$):
	$$
	P_k = 2\Delta y - \Delta x
	$$
	This decision variable is used to decide whether x-coordinate should be incremented or y-coordinate should be incremented or both.
	
4. Suppose the current point is $(X_k, Y_k)$ and the next point is $(X_{k+1}, Y_{k+1})$. We find the next point by following the two cases.
	**Case 1:**
		if $P_k < 0$
		$X_{k+1} = X_{k} + 1$
		$Y_{k+1} = Y_k$
		$P_{k+1} = P_k + 2\Delta Y$
	**Case 2:**
		if $P_k >= 0$
		$X_{k+1} = X_k + 1$
		$Y_{k+1} = Y_k + 1$
		$P_{k+1} = P_k + 2\Delta Y - 2\Delta X$
	
5. $P_{k+1}$ will become the decision parameter for the next iteration $(X_{k+1}, Y_{k+1})$ is the next iteration. Keep repeating step no. 3 until the n point is reached or the number of iteration equals to $\Delta X - 1$


### Example
Calculate the points between the starting point (9, 18) and ending point (14, 22).

**Step I:**
Starting coordinates = $(X_o, Y_o)$ = (9, 18)
Ending coordinates = $(X_n, Y_n)$ = (14, 22)

**Step II-V:**





| $P_k$ | $P_{k+1}$ | $X_{k+1}$ | $Y_{k+1}$ |
| ----- | --------- | --------- | --------- |
| 3     | 1         | 10        | 19        |
| 1     | -1        | 11        | 20        |
| -1    | 7         | 12        | 20        |
| 7     | 5         | 13        | 21        |
| 5     | 3         | 14        | 22        |
