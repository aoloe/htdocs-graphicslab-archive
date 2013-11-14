
# Outlining fonts in exported PDFs

ale / 2012-10-02 20:43:49

Newer Scribus versions (starting with 1.3.4 or 1.3.5, I don't know for sure) do the "outlining" by converting the font to a PS Type 3 font, unlike the 1.3.3.x branch that (afaik) used XObjects. This is probably a good optimization, but some people some time really want outlined fonts.

[h]Related tickets[/h]
#7351 [url=http://bugs.scribus.net/view.php?id=7351]PDF export: fonts are always embedded[/url]
#8945 [url=http://bugs.scribus.net/view.php?id=8945]Confusing option name[/url]
