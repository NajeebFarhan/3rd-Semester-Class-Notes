---
Subject: "[[Computer Graphics and Multemedia]]"
tags:
  - CG
chapter/unit: 
related links: 
date: 2025-07-30
---

---

# Raster Scan Display

- In a raster scan system the electron beam is swept across the screen one row at a time from top to bottom. 
- As the electron beam moves across each row, the beam intensity is turned on and off to create a pattern of illuminated spots 
**Drawing letter E using Raster scan system**
placeholder

- Pixel definition is stored in memory area called the refresh buffer. These memory area holds the set of intensity values for all the screen points. 
- Stored intensity values are then retrieved from the refresh buffer and painted on the screen one row at a time.
- Each screen point is referred as a pixel 
- at the end of each line the electron beam returns to the left side of the screen to begin displaying the next scan line.
- Types of Scanning on travelling of beam in raster scan
	1. Interlaced Scanning
		here each horizontal line of the screen is creased from top to bottom due to which fading of display of object may occur.
		This problem can be solved by Non-interlaced Scanning. In which first of all odd number of lines are visited by an electron beam then in the next circle even number of lines are located.
		
	2. Non-interlaced Scanning
		It displays refresh rate of 30 frames per second is used but it gives flickers. for interlaced display refresh rate of 60 frames per second is used.

## Advantage of Using Raster scan image
1. Realistic image.
2. Million different colors to be generated.
3. Shadow scenes are possible

## Disadvantages of Using Raster scan image
- No resolution.
- Expensive.
- Scan conversion.


### Note
Computer understand math(coordinates, equations) but the screen only shows tiny dots called as pixels so scan conversion is the process of converting this math_based shapes(vector graphics) into pixels(in Raster graphics). This is also called as Rasterization