
# Which formatting should be applied to the next character typed?

ale / 2012-11-27 09:46:13

Currently, the way Scribus applies the formatting to the next character typed is based on the way the formatting and the text are stored in the internal data structures.

We need a concept work, which describes from the user perspective which formatting should be applied in each possible case.

Some possible cases are:
- the first character typed in a new frame
- a character typed before the first character in a non empty frame
- a character typed after the last character in a non empty frame
- the first character typed after a frame has been emptied
- the first character typed after a change of formatting in the middle of the text
- the first character typed in front of a change of formatting in the middle of the text
- the first character type when a selection was highlighted and gets replaced by the character
- the first character type after deleting a selection with different formatting than it's surrounding text
- ...

## Foske / 2012-11-27 10:04:37

Copied from IRC:

what do you do if a user just higlighted a word and
starts typing just before the word...
in the end my solution was not to apply the new
formatting to the first and last character if it is a
space, and if you type at the "outside" of the space you
get the old formatting, and when you type on the
"inside", i.e. close to the new formatted word, you get
the new one

## ale / 2012-11-29 19:04:13

there should not be an empty text frame. every frame contains at least an end of line mark.
- the paragraph formatting is attached to it
- it is possible to attach effects to (bullets, ...) to it.
