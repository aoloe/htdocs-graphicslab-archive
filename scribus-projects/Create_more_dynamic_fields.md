
# Create more "dynamic" fields

ale / 2012-10-03 16:29:36

In 1.5.0svn two dynamic fields exist: the page number and the number of pages.
Cezary's work for the footnotes brings also variable fields and cross references.

On top of this further fields are needed:
- real mathematical formulas

## ale / 2012-10-03 16:32:27

On September 29 2011, Peter Nermander,  wrote to the mailing list:
[quote]
I think we should look a bit further.

What Scribus needs is different kinds of automatic fields. They may be
references to objects or they may be other document of object data.

I also think a good approach would be to make it a bit object oriented.

Some examples (just brainstorming):

me.PageNumber (would correspond to todays #)

Frame("Frame name").Content (would work as a "live copy" of the frame content

me.Name (would give the name of the frame)

Document.FileName or maybe give it some options like Document.FileName(FullPath)


I think many of these would be easy to implement, at least if they are
already available in the Scripter (they could probably be made into
code snippets that are executed on preview or print of the document).


Another important feature would be fo be able to find the latest or
the next occurance of a certain style or frame name (to be able to get
automatic running headers). Somthing like:

Previous.Style("ChapterName").Content (where ChapterName is a style name)


MS Word has a lot of these features and I use the often.They save a
lot of work when rearranging documents.


I am not sure if the above ideas cover things like "See picture X"
where X is a dynamic reference.
[/quote]
