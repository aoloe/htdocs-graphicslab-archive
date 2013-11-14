
# Connect the text frames and their source

ale / 2012-10-02 18:34:46

The way the text frame can be connected with the file depends on the type of file:
- TXT
- formatted text (markdown)
- ODT
- HTML

The main issues seem to be:
- depending on the type of file, not all the Scribus formattings can be reproduced (and vice versa)
- if the layouter has already works on the typography (hyphenation, rivers, widows and orphans, ...) he must be warned that he has to check parts or all of the frame.

Some more issues:
- how to map inline frames?

Some random ideas:
- There should be a warning if a connected source has changed, but it's always the layouter who pulls the content and it's never done automatically.
- Saving to the text file can be done automatically or on demand

2.10.2012: Mariano Marini is interested in working on this.

## cezaryece / 2012-10-05 10:49:34

What about of possibility to insert into saved text file some formatting codes.
Similar approach was used by Ventura - user was able to insert into text some codes aka HTML tags which Ventura interprets as commands for layouting text.
In that way not only is possible to save some Scribus own properties with text. It will be possible even to prepare text file with Scribus properties already in text (for example from database and by scripts).

In fact, we already have all that codes defined - in SLA format. And we have interpreter for that ready. Only after importing text file all codes should be interpreted to proper para/char style properties.

## JLuc / 2012-12-18 12:41:06

markdown is a nice meant to be universal format

however, the translation mechanism should be overloadable so one could easily expand the list of possible format and implement ones own IN ou OUT format translations
