# Strace

## What is strace
* The man page states, "Strace is a useful diagnostic, instructional, and debugging tool"
* Traces all calls made by the program
* Allows us to look at low-level system calls by investigating the flow of the program

## Strace common flags
```
-o output file
-t timestamp
-r relative timestamp (relative timestamp provides total run time in ms)
-e qualifying expression (eg: open, socket, connect, recv)
-p process id (should be run as sudo)
```

## Usage
```
$strace -o output.txt <name of binary>
$strace -o output.txt -t <name of binary>
$strace -o output.txt -r <name of binary>
$strace -e access,write,close (if a list, no space between expressions)
$sudo strace -p <process id>
```