
# Improve the shape and contour line editing

ale / 2012-11-21 09:16:59

This is a meta request:
- Creating a margin around an image should be possible without going into the full fledged shape and contour line editor
- A better interface for switching between shape and contour line
- Make the use of the node editing tools snappier and more intuitive
- On canvas node editing

## jan / 2012-11-21 09:19:09

from the mailing list:

About "white space" around photos and graphics: I think an addition to the 'Shape' tab under 'Properties' would be great. Exactly as 'Rounded Corners' works to give you the "white space" between the text and the graphic.

## greg / 2012-11-21 09:20:12

from the mailing list:

I think it's important to think generically about the idea and consider what would be the most convenient way to implement. I would think that 
there might be a setting in Preferences > Tools where you might specify a displaced contour line a certain amount larger than the frame border. 
You also have to think about implementing this for more than just image frames, but also text and render frames (maybe even tables).

I don't know that it really makes sense to have the default for a contour line to be the same as the frame border. If you want to flow around the contour line, don't you want it to be different from the border?
