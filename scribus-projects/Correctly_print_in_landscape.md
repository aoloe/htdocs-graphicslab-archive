
# Correctly print in landscape

ale / 2012-11-01 13:18:00

Currently, on most platforms, Scribus can't correctly print in landscape.

## Greg / 2012-11-01 13:18:54

(taken from the mailing list)


Here are some observations about printing landscape orientation directly 
from Scribus.

If you have a page oriented in a landscape fashion in Scribus, when you 
print in a normal (i.e., portrait) manner, it will print in a landscape 
way. In other words, the right hand side of the page as displayed comes 
out the printer first. If you set for a landscape mode of printing, it 
comes out the printer as a portrait printing, i.e., the top of your 
landscape-oriented page comes out the printer first. This seems to be 
true for whatever OS you are using.

On Fedora, for the most part I have to use an alternative printer 
command (I use lpr), and in this case you see a similar phenomenon, 
using either the default option (equivalent to '-o portrait'), or use 
'-o landscape'. A landscape-oriented page comes out in a landscape way 
(right side of the page first) if you use '-o portrait', but a 
portrait-oriented page requires you to specify '-o landscape' for the 
page to come out in a landscape way (right side of the page first).

So although it's quirky, it is possible to control the printing 
orientation. You just have to experiment.

Greg

Addendum - more weirdness

If you have a page already in a portrait orientation, and you go to File 
 > Document Setup and switch to landscape, this will only apply to new   
pages you create, and does not affect the existing page(s).
So I just now started with a one-page document in portrait orientation, 
switched to landscape in Document Settings, then added a page. Then I 
printed the entire document with 'lpr -o landscape' from Scribus. The 
first page came out right side of the page first, the second page came 
out bottom side first!
