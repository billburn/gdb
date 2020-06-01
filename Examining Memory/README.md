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
```