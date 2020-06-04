# Calling Functions

* (1) In addition to setting convenience functions, and calling with print
* (2) You may also call functions directly from GDB

```
(gdb) set $i = 10
(gdb) print $i
(gdb) print argv[1]
```

```
(gdb) info functions
(gdb) call <name of function> <argument 1> <argument n>
```
