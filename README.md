##  Today-Scripts (custom scripts in your notification bar. This fork has a fix for Mac OS X Sierra, tested on **macOS 10.12.3**)
A widget for running scripts in the Today View in OS X Sierra`s Notification Center.

Changed original script to fit new light transparent style introduced in OSX Sierra.

##Features

* [Colorized Output](http://i.imgur.com/Yvj2ePG.png). Today Scripts supports colorized terminal output from your scripts, as well as bold and underline.
* [Custom Labels](http://i.imgur.com/LL4s6Ao.png). Today Scripts has a form for setting up scripts, which gives you the option of picking a label to display instead of the script itself.
* Custom Interpreters: When setting up a script, you may specify any program to run in place of your shell. This means you can directly run scripts in Python, Perl, AppleScript, etcetera, simply by specifying their associated interpreter.
* Manually Run Scripts: Scripts may be run on command by clicking on their label. You may also specify that scripts not be run automatically when Notification Center is opened.
* Output text selection: You may highlight the output of your scripts, allowing you to copy it to the clipboard or drag it where you please.

##Usage

After building, simply copy "Today Scripts.app" wherever you'd like to store it, then open it. In Notification Center, you will see "1 New" appear on the edit button, and you may use that to add Today Scripts to your Today View in order to begin using it.

To begin editing your list of scripts, click the "Info" symbol in the title of the widget.

To start or stop a given script on demand, click its label in your list.

To edit an existing script, click the "action" button to the right of its label.

##Technical Details

* An interpreter can be speficied using a path to any valid executable (it need not be an "interpreter" at all). The provided script is piped to the interpreter via its standard input.
* Today Scripts emulates a 40-column terminal. When running a script, a pseudo-TTY is opened for it, and the standard output and standard error of it is set to that. The `COLUMNS` environment variable for scripts is set to `40`, and `PAGER` is set to `/bin/cat`.
* Today Scripts supports all ANSI color sequences; both standard and bright, as well as both foreground and background. The `TERM` environment variable for scripts is set to `ansi`.

##Special Thanks

Support for ANSI escape sequences made possible thanks to [Ali Rantakari's ANSIEscapeHelper](http://hasseg.org/ansiEscapeHelper/).

Special credit to [lsd](https://github.com/lsd/Today-Scripts/) for previous fixes regarding OSX El Capitan

Icon designed by [Friedrich Preuß](http://phriedrich.de).
