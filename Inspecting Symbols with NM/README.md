# Inspecting symbols with NM

## NM lists symbols from object files
```
gdb@ubuntu:~/gnu-debugger-course/video3$ nm video3_debug_symbols 
08048474 T AddNumbers
0804a02c B IamAGlobalVariable
0804a020 D IamInitializedGlobalVariable
08048491 T SubtractNumbers
08049f28 d _DYNAMIC
08049ff4 d _GLOBAL_OFFSET_TABLE_
0804863c R _IO_stdin_used
```

## NM Structure
```
08048474            T               AddNumbers
<virtual address>   <symbol type>   <symbol name>
```

## NM Symbol Types (for all symbols, use $man nm)
* Lowercase symbols denote Local Symbols
* Uppercase symbols denote external
|  Symbol Type  |  Symbol Meaning  |
|---------------|------------------|
|       A       | Absolute Symbol  |
|       B       | In the Uninitalized Data Section (BSS) |
|       D       | In the Initalized Data Section |
|       N       | Debugging symbol |
|       T       | In the text section |
|       U       | Symbol is undefined |