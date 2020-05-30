# Common Commands

## list
```
Usage: (gdb) list OR list 5
* Have to have the orginal source file to be used
This will list the next 10 lines depneding on how its used.  The first time it will list the first 10 lines of the file.
(gdb) list 10 will list starting at the 10th row
```

## info functions
```
Usage: (gdb) info functions
info functions will provide you with a list of compiled functions
```

## info sources
```
Usage: (gdb) info sources
This will tell you what sources are used for the compiled binary
```

## info variables
```
Usage: (gdb) info variables
This will tell you the variables that are part of the compiled binary
* does not print local variables, only global and static
```