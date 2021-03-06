
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
Trash                |  Clear             | _(N/A)_       | Clear all vertices.
Brushes              |  Color             | _(N/A)_       | Set a color
Copy                 |  Copy              | _(N/A)_       | Open a new web page with the current vertices specified in the URL.  NOTE: Bookmarking that URL will bookmark a link which can be used to reopen the polygon again for editing.
Clipboard            |  Clipboard         | _(N/A)_       |  Select the array syntax (for copying/pasting into your code).

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

You can Find Max's work on his [youtube channel](https://www.youtube.com/channel/UCZXyfVkPTnv-Z0xY9hA9Pyw), on his [github page](https://github.com/maxwihlborg), and at [http://www.maxwihlborg.com](http://www.maxwihlborg.com)

This content is released under the ([http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)) MIT License.