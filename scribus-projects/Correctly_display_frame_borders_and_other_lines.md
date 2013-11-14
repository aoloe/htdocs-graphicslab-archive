
# Correctly display frame borders and other lines

ale / 2012-10-04 09:57:22

Frames are not being displayed pixel-perfect, not more then that. It's always a bit antialiased due to 
document/screen coordinate conversion.

Thickness should be exactly 1 screen pixel thin. This is wrong in scribus right now, it both 1.4 and 1.5.
