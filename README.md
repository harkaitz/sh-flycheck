SH FLYCHECK
===========

Flycheck mechanism for GNU Emacs that works with all build systems.

## Help

chk

    Usage: chk FILES...
    
    Check file correctness of source files. It applies the following
    inconsistencies:
    
      1. For "h" files it searches "c cpp cc cxx ..." LANGs.
      2. For "hh/hpp/hxx" files it searches "cpp cc cxx ... c".
    
    Files:
    
      1. ~/.commands.d/LANG   : File with "SRCDIR;WRKDIR;ENV;COMMAND".
      2. ~/.environment.d/ENV : File with export commands.
    
    You can create the files above with "make-h-tool(1)".

chk-h-emacs

    Usage: chk-h-emacs [-D EMACS_DIR] OPTS...
    
    Install "chk" in GNU Emacs's home directory and flycheck
    support.
    
      -V : Show configuration.
      -i : Install "chk".
      -u : Uninstall "chk".
    
    Environment variables: EMACS_DIR, HOME, USERPROFILE

make-h-tool

    Usage: make-h-tool { CMD ARGS... | MAKE-ARGS... }
    
    Perform a dry execution of the makefile.
    
    ... show                 : Show configuration.
    ... dry-run MAKE-ARGS... : Run "make -n" to create ".make.dryrun" and ".make.environment".
    ... dry-show             : Show compilation and cd commands.
    ... chk-update           : Create "~/.commands.d/LANG" and "~/.environment.d/CHKSUM".
    ... run COMMAND          : Execute COMMAND with "MAKE=make-h-tool".
    ... MAKE-ARGS...         : make(1), dry-run(2), chk-update(3).
    
    Examples:
    
    > make-h-tool run ./build.sh build

## Collaborating

For making bug reports, feature requests and donations visit
one of the following links:

1. [gemini://harkadev.com/oss/](gemini://harkadev.com/oss/)
2. [https://harkadev.com/oss/](https://harkadev.com/oss/)
