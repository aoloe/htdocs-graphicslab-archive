
# Add information about the revision and the branch in the about dialog

ale / 2012-11-21 07:58:40

Add information about the revision and the branch in the about dialog:
- [url]http://stackoverflow.com/questions/657850/cmake-how-to-use-bash-command-in-cmakelists-txt[/url]
- [url]http://stackoverflow.com/questions/9639449/cmake-how-to-pass-preprocessor-macros[/url]
- [url]http://stackoverflow.com/questions/3780667/use-cmake-to-get-build-time-svn-revision[/url]

## john / 2012-11-21 07:59:51

from the mailing list

Referencing 
[url]http://stackoverflow.com/questions/3780667/use-cmake-to-get-build-time-svn-revision[/url]

The above stackoverflow topic deals with calls to the cmake standard 
module "FindSubversion" which, in turn, takes the results of svn info 
and parses them into various variables.  I found a project for 
FindSubversion.cmake at 
[url]http://code.google.com/p/tombexcavator/source/browse/trunk/cmake/FindSubversion.cmake?r=81[/url]. 
   I'm not sure "svn info" is the way to go; instead the command 
"svnversion" seems appropriate.  So I'm playing around with adding a 
cmake MACRO to a modified version of FindSubversion that invokes svnversion.

Using the strategy of the stackoverflow topic above, I'm working on a 
method using cmake which invokes "svnversion" and creates a header file, 
svnversion.h, that may be used by about.h (I'm assuming in c++ headers 
may include other headers).  The header svnversion.h would create a 
variable SVNVERSION assigned the output from running the svnversion 
command.  The output of a svnversion command is terse, example:

    themis Scribus # svnversion
    17871M
    themis Scribus #

  And the additional benefit is that alphabetic characters will appear, 
such as the "M" above, if the Subversion tree has been modified or 
otherwise not complete.

I'm gated now because Gentoo copies the Subversion tree over to a 
temporary directory, i.e. /var/tmp/portage/app-office/scribus..., 
leaving behind the .svn directory.  In recent versions of Subversion, 
the top most .svn directory contains the database that manages the 
entire tree below.   So, in a Gentoo emerge, cmake invokes "svnversion" 
against its staged "tmp" tree and therefore fails since it cannot find 
the .svn subdirectory.  The part I'm focusing on now is to have Gentoo 
provide a reference back to its source of the Scribus Subversion tree, 
i.e. /usr/portage/distfiles/svn-src/scribus/Scribus, so the svnversion 
command is feed that path -- it should work then.  This should be 
helpful for other Gentoo builds based on Subversion pulls, e.g. those 
labeled version "9999".
