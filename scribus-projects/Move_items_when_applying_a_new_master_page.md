
# Move items when applying a new master page

ale / 2012-10-13 17:59:50

When you have facing pages, when moving one or multiple pages from the left to the right "side", you need to move the elements to match the margins.

For simple changes, Scribus should optionally be able to propose to automatically shift all the items on each page concerned.

- Create a simple .ui file
- Go and find where the master pages gets applied (might be multiple places)
- check if the two MP have different margins and if there are items on the page; if it's the case start the dialog
- if the user choses to move the items, go through all the items on the pages and change their Y coordinate by the difference between the old and the new margins.

This project is a good introductory project for somebody want to start contributing to Scribus
