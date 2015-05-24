
# polygondraw


Polygondraw is a browser based polygon editor originally written by Max Wihlborg to support his excellent Javascript Asteroids tutorial. I started using it extensively to develop my own vector games, so I ended up fleshing out the feature set.

Button | Mode [Hotkey] : Description
------ | --------
Arrows | **Move** [M or <escape>]: Click on (or near) a vertex to pick it up. Click again to drop it.
Pencil | **Line** [L]: Click to add a vertcies (i.e. draw a new line segment).
Plus   | **Add** [A]:  Click along (or near) an existing line segment to add a new verted along it.
Scissors | **Cut** [C]: Click on (or near) verticies to remove them.
Crosshair | **Change Origin** [O]: Click to specify a new origin. 
Circular Left Arrow | **Undo** [U]
Circular Right Arrow | **Redo** [R]
Trash | **Clear**: Clear all verticies.
Copy | **Copy**: Open a new web page with the current verticies specified in the URL.  NOTE: Bookmarking that URL will bookmark a link which can be used to reopen the polygon again for editing.
Clipboard | **Clipboard**: Select the array syntax (for copying/pasting into your code).
Code | **Code Mode**: Cycle through the various array syntax options (ARRAY, ONE_ARRAY, NORMALISED, ONE_NORMALIZED).

You can Find Max's work on his [youtube channel](https://www.youtube.com/channel/UCZXyfVkPTnv-Z0xY9hA9Pyw), on his [github page](https://github.com/maxwihlborg), and at [http://www.maxwihlborg.com](http://www.maxwihlborg.com)

This content is released under the ([http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)) MIT License.