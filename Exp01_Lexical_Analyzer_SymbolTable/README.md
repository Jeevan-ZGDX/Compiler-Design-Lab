# Experiment 1: Lexical Analyzer with Symbol Table using LEX

## Aim
To develop a lexical analyzer using FLEX to recognize tokens such as identifiers, constants, comments, and operators in a C program and to create a symbol table while recognizing identifiers.

## Files
- `symtab.l` — FLEX source file
- `input.c` — Sample C input file

## How to Compile and Run
```bash
flex symtab.l
gcc lex.yy.c -o symtab -lfl
./symtab input.c
```

## Expected Output
```
Comment    : // sum variable
Identifier : int
Identifier : a
Constant   : 10
Operator   : =
Identifier : b
Identifier : a
Operator   : +
Constant   : 5

SYMBOL TABLE
S.No	Name
1	int
2	a
3	b
```
