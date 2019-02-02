
# Polygondraw

Polygondraw is a browser based polygon editor originally written by Max Wihlborg to support his excellent Javascript Asteroids tutorial. I started using it extensively to develop my own vector games (see [vectoralchemy.com](http://www.vectoralchemy.com)), so I ended up fleshing out the feature set.

Button               | Mode               | Hotkey        | Description
------               | ------------------ | ------------- | -------------------------------------
Arrows               |  Move              | M or <escape> | Click on (or near) a vertex to pick it up. Click again to drop it.
Pencil               |  Line              | L             | Click to add a vertices (i.e. draw a new line segment).
Plus                 |  Add               | A             | Click along (or near) an existing line segment to add a new vertex along it.
Scissors             |  Cut               | C             | Click on (or near) vertices to remove them.
Crosshair            |  Change Origin     | O             | Click to specify a new origin.
Eye                  |  Toggle Visibility | V             | Toggle the visibility of a line segment.
Anchor               |  Toggle Grid Snap  | S             | Toggle snapping to the grid.
Circular Left Arrow  |  Undo              | U             | Undo
Circular Right Arrow |  Redo              | R             | Redo
Hand                 |  Pan               | H             | Pan canvas
Scale                |  Scale             | X             | Apply a scale factor to polygon (can be a number or math expression i.e. 2, 0.5, or 1/3)
Trash                |  Clear             | _(N/A)_       | Clear all vertices.
Brushes              |  Color             | _(N/A)_       | Set a color

# Grid Controls
* The bottom slider controls the grid subdivision level. There are four levels of subdivision. Changing the subdivision results in the all points on all frames being dynamically altered so that they stay in the same location.
* The slider second from the bottom controls the current magnification level (this does not alter the points).

# Animation Controls
Above the magnification slider is a small slider for the animation speed.

Button         | Hotkey      | Description
-------------- | ----------  | -----------------------------------------------------------------------------
Plus           |             | adds a new frame and copys all existing points from the previous frame
Minus          |             | deletes the current frame you are viewing (unless you are on the first frame)
Previous frame | Left arrow  | move to the previous frame
Next frame     | Right arrow | move to the next frame
Play           |             | play animation
Stop           |             | stop animation
Export         |             | Export all frames to clipboard copy buffer

NOTE:
* shift + left arrow skips to beginning frame
* shift + right arrow skips to end frame

## Rotoscoping
Checkbox location           | Description
--------------------------- | ------------------------------------
Above previous frame button | Rotoscope previous frame (neon red)
Above next frame button     | Rotoscope next frame (neon blue)

Note:
* the sliders beside the above mentioned checkboxes control the opacity for the rotoscoping

# Data format
Vector data has the form [x1, y1, x2, y2, x3, y3, ...., xN, yN]
Special "escape" sequences mark color and pen-up transitions:

X | Y | Function
------ | -------- | -----
9000 | 7000 | Pen Up (next line segment is invisible)
9000 | 80nn | Switch to color #nn

# Color Codes
Value | Color
------ | --------
01 | BLUE
02 | WHITE
03 | GREEN
04 | YELLOW
05 | RED
06 | CYAN
07 | MAGENTA
08 | CYAN_DK
09 | ORANGE
10 | BROWN
11 | YELLOW_DK
12 | GRAY
13 | GRAY_DK
14 | LIGHTSKYBLUE
15 | DODGERBLUE
16 | LIGHTBLUE

Note: You can load any pre-existing vector from your code into polygondraw by specifying it in the URL; just add a "?" followed by the array data.  For example:
```
http://www.website.com/polygondraw.html?[1,1,4,4]
```

Or for loading in multiple frames for animations:
http://www.website.com/polygondraw.html?[[0,0,0,-2],[0,0,1,-2],[0,0,2,-2],[0,0,2,-1],[0,0,2,0],[0,0,2,1],[0,0,2,2],[0,0,1,2],[0,0,0,2],[0,0,-1,2],[0,0,-2,2],[0,0,-2,1],[0,0,-2,0],[0,0,-2,-1],[0,0,-2,-2],[0,0,-1,-2]]

You can Find Max's work on his [youtube channel](https://www.youtube.com/channel/UCZXyfVkPTnv-Z0xY9hA9Pyw), on his [github page](https://github.com/maxwihlborg), and at [http://www.maxwihlborg.com](http://www.maxwihlborg.com)

This content is released under the ([http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)) MIT License.
