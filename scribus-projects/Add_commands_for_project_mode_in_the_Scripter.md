
# Add commands for "project mode" in the Scripter

ale / 2012-12-14 17:21:44

"Project mode" is about using several .SLA files in one project.

Since both GSoC 2012 projects on that topic have failed, we could first implement some of the features needed for a "project mode"  in the Scripter, before trying again to implement the whole feature. The part that is easier to implement is the one related to the output (PDF, EPUB).

That way:
- we can avoid the specification of a new file format for the project
- we don't have to work on a GUI
- the changes we will make can be used for a full featured "project mode"

The first try can be done with the EPUB export plugin:
- create a new command for exporting to epub and document it
- change the export code to handle multiple sources
