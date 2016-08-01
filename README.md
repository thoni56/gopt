# Gopt - Command line argument parsing in C

_NOTE: This software was created by [Tom Vajzovic](http://www.purposeful.co.uk/tom/),
but as [its site](http://www.purposeful.co.uk/software/gopt/)
seemed to be dying, I decided to copy it here for posterity.
All credit go to Tom._

Gopt is small set of C library functions for parsing POSIX and GNU
style command line arguments.

Gopt has a far more simple interface than any of the library functions
typically used to perform this task, such as Argp or getopt.

To see how simple Gopt is, look the sample program, gopt-usage.c.

Further documentation is provided in the form of comments in the
header file, gopt.h.

To start using Gopt, download the source code, gopt.c.

Gopt is written in pure C89 (ANSI C), but the header file has
convenience macros which use several of the more widely available
features of C99 (ISO 9899:99).  Gopt is free standing; it has no
dependencies on any libraries other than the C library.

There is no configure script.  The only thing you may want to change
is to define USE_SYSEXITS when gopt.c is compiled, if your system
provides <sysexits.h> (Most BSD and many Linux systems do).

Gopt is truly free software.

## Features

 - No loop required in main(), just a single function call.
 - Short (POSIX/Unix) style options, like mkdir -p
 - Long (GNU) style options, like cp --remove-destination
 - Automatic recognition of abbreviated long options, like cp --rem
 - Option arguments, like --suffix=.c, -S.c, --suffix .c or -S .c
 - Simple handling of repeatable options.
 - End of options delimiting with --
 - Automatic program termination on error.
 - Automatic error messages to stderr for illegal or ambiguous options.
 - Automatic error messages to stderr for missing or forbidden option arguments.
 - Options and option arguments are removed from the argument vector (argv), leaving only true operands.
 - Operand count corrected in argc.

## Deficiencies

 - Error messages in English only.
 - No automatic handling of --help or --version

## Versions

The files above are Gopt/8.1.  All previous versions have bugs in both
their design and in several cases, their implementation.  If you still
have a perverse desire for a copy of the older versions, please
contact [Tom Vajzovic](http://www.purposeful.co.uk/tom/).