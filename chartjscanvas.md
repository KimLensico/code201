# Chart.js, Canvas

## Canvas

``` <canvas></canvas>``` element has only two attributes, ```width``` and ```height```.
- both are optional and can also be set using DOM properties
- the ```<canvas>``` element differs from an ```<img>``` tag in that, like for ```<video>```, ```<audio>```, or ```<picture>``` elements

Chart.js - a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page 
    - documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

```<canvas>``` only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths. Luckily, we have an assortment of path drawing functions which make it possible to compose very complex shapes.

## Drawing paths
```path`` - is a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color
    - path, or even a subpath, can be closed. 
    
To make shapes using paths, we take some extra steps:

    1. First, you create the path.
    2. Then you use drawing commands to draw into the path.
    3. Once the path has been created, you can stroke or fill the path to render it.

Here are the functions used to perform these steps:

```beginPath()```
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.

```Path methods```
Methods to set different paths for objects.

```closePath()```
Adds a straight line to the path, going to the start of the current sub-path.

```stroke()```
Draws the shape by stroking its outline.

```fill()``
Draws a solid shape by filling the path's content area.

```closePath()```
This method tries to close the shape by drawing a straight line from the current point to the start. 
    - If the shape has already been closed or there's only one point in the list, this function does nothing.

**When you call fill(), any open shapes are closed automatically, so you don't have to call closePath(). This is not the case when you call stroke().**

### Moving the pen

```moveTo(x, y)```
Moves the pen to the coordinates specified by x and y

```lineTo(x, y)```
Draws a line from the current drawing position to the position specified by x and y.

### Arcs
To draw arcs or circles, we use the arc() or arcTo() methods.

```arc(x, y, radius, startAngle, endAngle, anticlockwise)```
Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).

```arcTo(x1, y1, x2, y2, radius)```
Draws an arc with the given control points and radius, connected to the previous point by a straight line.

### Drawing a Line 

```lineTo(x, y)```
Draws a line from the current drawing position to the position specified by x and y.

### Arcs
To draw arcs or circles, we use the arc() or arcTo() methods.

```arc(x, y, radius, startAngle, endAngle, anticlockwise)```
Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).

```arcTo(x1, y1, x2, y2, radius)```
Draws an arc with the given control points and radius, connected to the previous point by a straight line.

### Bezier and quadratic curves
Bézier curves - available in both cubic and quadratic varieties. 
    - These are generally used to draw complex organic shapes.

```quadraticCurveTo(cp1x, cp1y, x, y)``` 
Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.

```bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)```
Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).

- has just one control point 

### Rectangles
```rect(x, y, width, height)``` 
Draws a rectangle whose top-left corner is specified by (x, y) with the specified width and height.

### Making combinations

*there's no limitation to the number or types of paths you can use to create a shape*

### Path2D objects
- there can be a series of paths and drawing commands to draw objects onto your canvas. 
    - To simplify the code and to improve performance, the Path2D object, available in recent versions of browsers, lets you cache or record these drawing commands. You are able to play back your paths quickly.
Let's see how we can construct a Path2D object:

```Path2D()``` 
The Path2D() constructor returns a newly instantiated Path2D object, optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data.

All path methods like moveTo, rect, arc or quadraticCurveTo, etc., which we got to know above, are available on Path2D objects.

The Path2D API also adds a way to combine paths using the addPath method. This can be useful when you want to build objects from several components, for example.

```Path2D.addPath(path [, transform])```
Adds a path to the current path with an optional transformation matrix.

### Using SVG paths
Another powerful feature of the new canvas Path2D API is using SVG path data to initialize paths on your canvas. 
    - might allow to pass around path data and re-use them in both, SVG and canvas.

## Colors
```fillStyle = color``` 
Sets the style used when filling shapes.

```strokeStyle = color```
Sets the style for shapes' outlines.

### Transparency 
```globalAlpha = transparencyValue```
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.

### Line styles
```lineWidth = value```
Sets the width of lines drawn in the future.

```lineCap = type```
Sets the appearance of the ends of lines.

```lineJoin = type```
Sets the appearance of the "corners" where lines meet.

```miterLimit = value``` 
Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

```getLineDash()```
Returns the current line dash pattern array containing an even number of non-negative numbers.

```setLineDash(segments)```
Sets the current line dash pattern.

```lineDashOffset = value```
Specifies where to start a dash array on a line.

### lineCap
```butt```
The ends of lines are squared off at the endpoints.

```round```
The ends of lines are rounded.

```square```
The ends of lines are squared off by adding a box with an equal width and half the height of the line's thickness.

### lineJoin
The lineJoin property determines how two connecting segments (of lines, arcs or curves) with non-zero lengths in a shape are joined together (degenerate segments with zero lengths, whose specified endpoints and control points are exactly at the same position, are skipped)
- There are three possible values for this property: 
    - round, bevel and miter. By default this property is set to miter. 
    - lineJoin setting has no effect if the two connected segments have the same direction
        - no joining area will be added in this case.

```round```
Rounds off the corners of a shape by filling an additional sector of disc centered at the common endpoint of connected segments. The radius for these rounded corners is equal to half the line width.

```bevel```
Fills an additional triangular area between the common endpoint of connected segments, and the separate outside rectangular corners of each segment.

```miter```
Connected segments are joined by extending their outside edges to connect at a single point, with the effect of filling an additional lozenge-shaped area. This setting is effected by the miterLimit property which is explained below

**[🠴 RETURN](README.md)**