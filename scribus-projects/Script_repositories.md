
# Script repositories

ale / 2012-10-12 22:48:46

- create a script that can download and run scripts
- one can add new repositories
- there could be an official repository on services.scribus.net (what's the use? official script could be distributed with scribus...)


implementation:
- create it as a script or a plugin?
- how to update the installed script? (version with date? or just uninstall and reinstall?)

- add a repository
  - there are different types of repository (an example would be git download directory)? really needed? or simply a http(s) download?
- cache and update the list of scripts on the server
- one tab to download the scripts from the defined repositories
- one tab to run one of the downloaded scripts
- with scripter 2 there will be a way to defined where the script goes in the menus and which shortcut it uses

- add a ~/.scribus/scripter/repository/ directory
  - ~/.scribus/scripter/repository/sources.xml list of repositories
  - ~/.scribus/scripter/repository/cache.xml list of scripts found in the repositories
  <sources>
    <repository>
      <url>https://github.com/aoloe/scribus-planet/downloads</url>
      <status>ok|failed</status>
      <script>
         <file>
            <filename>exportguides.py</filename>
         </file>
         <file>
         ...
         </file>
      </script>
    </repository>
    <repository>
    ...
    </repository>
  </sources>
  - ~/.scribus/scripter/repository/script/ contains *.py files that are automatically listed in "Scribus > Scribus Scripts", too

In the list of scripts you have an alphatbetical list of all Scripts from
