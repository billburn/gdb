# Modifying Memory

## Viewing Memory Recap
```
* We can use x/s (string) to view memory (gdb) x/s argv[1]
* Alternatively we can use (gdb) print argv[1]
```

## Modifying Memory using set
```
* Usage: set {int || char || other type} <memory location> = <value>

(gdb) set {int} 0xbffff543 = 1
(gdb) x/5c argv[1]
0xbffff543:	1 '\001'	0 '\000'	0 '\000'	0 '\000'	0 '\000'
(gdb) set {char} 0xbffff543 = 'B'
(gdb) set {char} (0xbffff543 + 1) = 'B'
(gdb) set {char} (0xbffff543 + 2) = 'B'
(gdb) set {char} (0xbffff543 + 3) = 'B'
(gdb) x/5c argv[1]
0xbffff543:	66 'B'	66 'B'	66 'B'	66 'B'	0 '\000'
(gdb) x/s argv[1]
0xbffff543:	 "BBBB"
```

## Modifying Registers
```
* This is accomplished via the set command
Usage: (gdb) set $eip = 0x80484f4
```