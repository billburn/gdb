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

## info variables (only shows global and static variables)
```
Usage: (gdb) info variables
This will tell you the variables that are part of the compiled binary
* does not print local variables, only global and static
```

## info scope <variable name> (tab complete to see list)
```
Usage: (gdb) info scope <var_name>
This will allow you to see local variables
```

## adding symbols to runtime with gdb
```
Usage: (gdb) symbol-file <name_of_symbol_file>
Confirm with: (gdb) info variables
Alternative: you may use objcopy to add symbols too, check Google (objcopy --add-gnu-debug-link=<name_of_symbol_file>)
```