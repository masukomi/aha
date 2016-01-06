# aha - Ansi HTML Adapter

## Usage

```text
Ansi Html Adapter Version 0.4.7.1
aha takes SGR-colored Input and prints W3C conform HTML-Code
use: aha <options> [-f file]
     aha (--help|-h|-?)
aha reads the Input from a file or stdin and writes HTML-Code to stdout
options: --black,      -b: Black Background and White "standard color"
         --pink,       -p: Pink Background
         --stylesheet, -s: Use a stylesheet instead of inline styles
         --iso X,    -i X: Uses ISO 8859-X instead of utf-8. X must be 1..16
         --title X,  -t X: Gives the html output the title "X" instead of
                           "stdin" or the filename
         --line-fix,   -l: Uses a fix for inputs using control sequences to
                           change the cursor position like htop. It's a hot fix,
                           it may not work with any program like htop. Example:
                           echo q | htop | aha -l > htop.htm
         --word-wrap,  -w: Wrap long lines in the html file. This works with
                           CSS3 supporting browsers as well as many older ones.
         --no-header,  -n: Don't include header into generated HTML,
                           useful for inclusion in full HTML files.
Example: aha --help | aha --black > aha-help.htm
         Writes this help text to the file aha-help.htm
```

## Installation:

### OS X

	brew install aha

### Linux 

Your distro's package manager probably has it.

### From source
To compile just run make

	$ make

To "install" aha type (as root, or with sudo)

	$ make install


### License Note:

All files are subjects to the LGPL or the MPL. (Dual licensed).
