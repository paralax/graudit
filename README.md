graudit
===============================================================================
graudit is a simple script and signature sets that allows you to find potential 
security flaws in source code using the GNU utility grep. It's comparable to 
other static analysis applications like RATS, SWAAT and flaw-finder while 
keeping the technical requirements to a minimum and being very flexible.

Usage
===============================================================================
graudit supports several options and tries to follow good shell practices. For
a list of the options you can run graudit -h or see below. The simplest way to 
use graudit is;

```
graudit [opts] /path/to/scan

OPTIONS
  -d <dbname> database to use or /path/to/file.db (uses default if not specified)
  -A scan ALL files
  -x exclude these files (comma separated list: -x *.js,*.sql)
  -i case in-sensitive scan
  -c <num> number of lines of context to display, default is 2

  -B supress banner
  -L vim friendly lines
  -b colour blind friendly template
  -z supress colors
  -Z high contrast colors
  
  -l lists databases available
  -v prints version number
  -h prints this help screen
```

Databases
===============================================================================
graudit uses extended regular expressions (POSIX) as it's signatures and comes 
with several databases ready for use. You can extend the existing databases or 
make your own if you require additional signatures.

* All is a combined database of all the databases listed below

* Asp offers basic auditing support for the Active Server Pages languages

* C offers support for the C programming language

* Default is aimed at finding low hanging fruit. It cointains generic rules that 
  should match common vulnerabilites in several languages. However, in order to 
  find additional vulnerabilities for a specific language you should use the 
  language specific databases.

* Dotnet offers basic dot net support

* Jsp basic JSP support.

* Other looks for source comments that could indicate problems

* Perl basic support for perl

* PHP tracks user input and function calls

* Python basic python support

Contributing
===============================================================================
If you would like to contribute to graudit, please fork the repository at 
https://github.com/wireghoul/graudit and use that. If you wish to get in contact 
with me, shoot me a line on github or twitter (@wireghoul).

Credits
===============================================================================
Wireghoul - http://www.justanotherhacker.com
Various others - see Changelog
