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

## Breakpoint Usage
```
(gdb) break *<memory address>
(gdb) break <function number>
(gdb) break <line number>
```

## List all Breakpoints
```
(gdb) info breakpoints
```

## Disable a breakpoint
```
(gdb) disable <breakpoint number to disable>
```

## Enable a breakpoint
```
(gdb) enable <breakpoint number to enable>
```

## Delete a breakpoint
```
(gdb) delete <breakpoint number to delete>
```

## Info Registers
```
* The program needs to be run first
(gdb) info registers
```

## Printing Registers
```
When using x/ or printing a register, it must have a $ prefix
Usage: (gdb) x/xs $eax

(gdb) info registers 
eax            0x4	4
ecx            0xbffff394	-1073745004
edx            0xbffff324	-1073745116
ebx            0xb7fc6ff4	-1208193036
esp            0xbffff2d0	0xbffff2d0
ebp            0xbffff2f8	0xbffff2f8
esi            0x0	0
edi            0x0	0
eip            0x8048579	0x8048579 <main+10>
eflags         0x282	[ SF IF ]
cs             0x73	115
ss             0x7b	123
ds             0x7b	123
es             0x7b	123
fs             0x0	0
gs             0x33	51
(gdb) x/xs ecx
No symbol "ecx" in current context.
(gdb) x/xs $ecx
0xbffff394:	 "\t\365\377\277C\365\377\277H\365\377\277K\365\377\277"
```

## Modifying Registers
```
* This is accomplished via the set command
Usage: (gdb) set $eip = 0x80484f4
```