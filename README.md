# Plotting B-spline curves

One of the good ways to develop a working knowledge of B-spline techniques is two actually write programming codes. This assignment is to write a program using C programming language and OpenGL (or any other programming language), which can plot an arbitrary degree B-spline curve. The program accepts an input file as follows, which defines a B-spline curve:
```````
degree
cnt_num
u0 u1 u2 …
x0 y0
x1 y1
...
```````
where “degree” is the degree of the B-spline curve, “cnt_num” is the number of the control points, “u0, u1, …” are the knot sequence of the curve, “x0 y0” are the x- and y-coordinates of the first control point, “x1 y1” are the x- and y-coordinates of the second control point, and so on.
Below “cubic.txt” is an example file of a cubic B-spline curve with 4 control points.
```````
cubic.txt ---
3
4
0 0.5 1 2 3 3.5 4.5 5
0 0
10 50
30 10
100 100
```````
The program will display both the control polygon and the curve. The curve will be plotted using two rendering methods: uniform and adaptive, as explained below.

1. With the uniform method, the program tessellates the curve by evenly sampling the parameter in the parameter domain of the curve. The program uses the number of the sampling points to control the tessellation.

2. With the adaptive method, the program first converts each curve segment of the Bspline curve into a Bezier curve and then adaptively tessellates the Bezier curve using the method given in the lecture (see Module 3. Bezier curves). The program uses the approximation tolerance to control the tessellation.

Your program should at least have the following features:
1. The student’s name should be displayed in the title bar of the application window.
2. Key “c” will switch between the control polygon and no control polygon
3. Key “p” will toggle displaying sampling points
4. Key “a” will switch between adaptive and uniform rendering modes.
5. Key “+” will increase the number of tessellation line segments.
6. Key “-” will decrease the number of tessellation line segments.
7. Key “ESC” will exit the program.

In particular,
* “cubic.txt”, “cubic1.txt”, and “quartic.txt” are some sample data files that you can use to
test your program.
