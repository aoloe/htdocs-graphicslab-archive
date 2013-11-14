
# copy paste and formatting

ale / 2012-12-01 18:17:21

When copy pasting a selection of text, the basic rule should be that character formatting are kept in the pasted text, but paragraph formatting are "lost".

In some "corner cases" the user may wish to keep the formatting:
- when the selection starts at the beginning of the paragraph
- when the selections ends and the end of the paragraph
- when the selections contains several paragraphs.
Those cases should be tested and a good behavior defined.

There may also be cases where the user may want to lose also the character formatting. We could check if some of those cases can be identified automatically and in a reliable way.
