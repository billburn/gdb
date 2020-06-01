# Examining Memory Usage

## Format Letters

|   Format Symbol   |  Symbol Meaning  |
|-------------------|------------------|
|       o           | Octal            |
|       x           | Hex              |
|       d           | Decimal          |
|       u           | Unsigned Decimal | 
|       t           | Binary           |
|       f           | Float            |
|       a           | Address          |
|       i           | Instruction      |
|       c           | Char             |
|       s           | String           |

## Size Letters

|   Size Letter Symbol   |  Symbol Meaning  |
|------------------------|------------------|
|       b                | Byte             |
|       h                | Halfword         |
|       w                | Word             |
|       g                | Giant Word       |

## x/Usage
```
FMT is a repeat count followed by a format letter and a size letter
Usage: (gdb) x/FMT address
Example: (gdb) x/s 0xbffff54a => prints the string located at this memory address
Example: (gdb) x/4x 0xbffff54a => prints the next (4) hex addresses
Example: (gdb) x/i 0xbffff54a => prints the assembly instruction for the address
Example: (gdb) x/10xw $esp => prints the next (10) assembly instructions after the pointer for $ESP register

(gdb) x/s 0xbffff54a
0xbffff54a:	 "test"

(gdb) x/4x 0xbffff54a
0xbffff54a:	0x74	0x65	0x73	0x74

(gdb) x/i 0xbffff54a
0xbffff54a:	je     0xbffff5b1

(gdb) x/10xw $esp
0xbffff2f0:	0xb7fed230	0x00000000	0x080484e9	0xb7fc6ff4
0xbffff300:	0x080484e0	0x00000000	0x00000000	0xb7e38533
0xbffff310:	0x00000002	0xbffff3a4
```