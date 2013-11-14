
# Extend "Arrange Pages" to become a Page management tool and flat plans

ale / 2012-10-04 08:59:24

- horizontal view
- preview of the page
- cleant up the dialog (remove the bin: DEL + context menu)

[h]Related tickets:[/h]
#10038 [url=http://bugs.scribus.net/view.php?id=10038]allow horizontal flatpans on canvas[/url]

## ale / 2012-10-04 09:04:44

i'm wondering what is the correct structure to show the page icons and previews.
currently it's done as a table, with empty colomns and rows inbetween the pages to be able to drag and drop the pages to sort them...
does anybody know of something better implemented in another application?

i'd really like to redo the palette by using a good .ui file...

## ale / 2012-10-04 09:12:33

the first obligatory step will be to show which master page is applied
to each page.
the easiest way would be to write the master page's name below each
page... but i don't really like it.
attaching a color, a letter or a number to each master pages doesn't
convince me either.
any brilliant idea?

then there are a few further things which i could to improve the dialog:

- using buttons instead of the context menu? (show / hide preview,
  horizontal / vertical layout, adding a page, removing a page, ...)

- the palette should work in both horizontal and vertical layout
  (depending on the width of the palette (or on the layout?) the master
  pages list should be on top or at the left of the list of pages). the
  biggest issue is: how to should the list of master pages be shown? is
  the current layout ok?

- do we really need a bin? (now you can drag master pages or pages to
  it... but i wonder if anybody gets it... reacting to the delete
  button and a context menu would imo be a much better choice!)

- should there be a button to launch the master page edit mode?

- should one be able to delete and create pages from this palette
  (currently one can drop a master page to the list of pages to create
  a new page... i wonder if anybody has ever used this function...).
  should there a button which starts the "insert page" dialog?

here is a preview of what i've been doing: [url]http://www.youtube.com/watch?v=W1UBGXALMws[/url]
