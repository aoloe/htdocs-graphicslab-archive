
# Improve the preflight verifier

ale / 2012-10-22 13:21:13

This is a meta project, listing various ideas for improvements to the preflight verifier:

- warn if double pages don't have the same size/orientation ([url=http://bugs.scribus.net/view.php?id=8214]#8214[/url])
- make it dockable
- allow a real time update
- it could be integrated into the "Outline" palette (the pop up could then be a special view of the outline palette)

## ale / 2012-11-09 09:25:05

What happens if the Exporter is invoked and the Preflight verifier is already docked?
We could put a warning in the exporting dialog instead: "11 errors and 3 warnings are waiting for your action in the Preflight verifier"

The popup is probably the best solution for "beginners".
