# Breakpoints

* Technique to freeze the program's execution
* Allows you to inspect / modify CPU, Registers, Memorts, and more

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

