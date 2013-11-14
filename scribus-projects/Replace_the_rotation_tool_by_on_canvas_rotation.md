
# Replace the rotation tool by on canvas rotation

ale / 2012-10-16 17:44:28

We should improve and use the mechanism in the content editing mode for the image frame.
Curently, when editing the content of an image frame the shift modifier key allows to rotate the image inside of the frame.

Alternative mechanisms would be:
- Like in Inkscape, clicking on the frame switches between move and rotate mode
- Like in SVGedit, a handle allows to rotate the frame.

Being compatible with Inkscape would be nice, but it seems that the rotation is not used as often in DTP as it is in vector drawing: is it justified to hijack the second click on the frame?

This proposal suggest to let the Shift modifier start the rotation mode when you click on a handle of the frame.
- when you hover a handle and press shift the cursor changes to the rotation one
- when your click on the handle while the shift modifier is down, the rotation mode starts
- you can release the shift modifier without exiting the rotation mode
- ESC exits the rotation mode and brings the shape back to its initial state
- pressing ctrl while in rotation mode constraints the rotation to multiple of 15°
- the base point is the opposite of the clicked handle
- if one of the middle handles are clicked, the base point is in the center of the frame

Once this is implemented, we suggest to remove the rotation button in the toolbar
- people who don't get the shortcut can rotate with the PP (with the single panel, context sensitive, PP it should not be a problem to find the rotation field)
