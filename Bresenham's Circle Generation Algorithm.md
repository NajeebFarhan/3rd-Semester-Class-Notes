![[Pasted image 20250812094150.png]]


# Procedure of Bresenhams' circle generation algorithm

Given, 
Center point of circle = $(X_0, Y_0)$
Radius of Circle = $R$

**Step I:** We will assign the starting point coordinates as 
$X_0 = 0$
$Y_0 = R$

**Step II:** Calculate the value of initial decision parameter
$$ P_0 = 3 - 2R$$

**Step III:** Suppose the current position is $(X_k, Y_k)$ and the next point is $(X_{k+1}, Y_{k+1})$. Find the next point of the first octant depending upon the value of decision parameter.
We will have two cases.
**Case I:**
if $P_k < 0$:
$X_{k+1} = X_k + 1$
$Y_{k+1} = Y_k$
$P_{k+1}  = P_k + 4X_{k+1} + 6$

**Case II:**
if $P_k >= 0$:
$X_{k+1} = X_k + 1$
$Y_{k+1} = Y_k - 1$
$P_{k+1} = P_k + 4(X_{k+1} - Y_{k+1}) + 10$


**Step IV:**  if the given center point $(X_0, Y_0)$ is not (0, 0), then do the following and plot the following
$X_{plot} = X_c + X_0$
$Y_{plot} = Y_c + Y_0$
here $X_c$, $Y_c$ denotes the current value of X and Y coordinates.

**Step V:** Keep repeating step III and IV until $X_{plot} >= Y_{plot}$

**Step VI:** Step no. V generates all the points for 1 octants. To find the points for other 7 octants we follow the 8-symmetry property of the circle.

### Example
Given the center point coordinates (0, 0) and Radius is 8, generate all points to form a circle.

**Step 1:**

**Step 2:**


| $P_k$ | $P_{k+1}$ | $(X_{k+1}$ |     |
| ----- | --------- | ---------- | --- |
|       |           |            |     |
