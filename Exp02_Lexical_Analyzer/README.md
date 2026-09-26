# Experiment 2: Implement a Lexical Analyzer using LEX Tool

## Aim
To create a program that reads a C source code file and identifies individual tokens such as identifiers, keywords, constants, operators, preprocessor directives, header files, and delimiters using FLEX.

## Files
- `lexer.l` — FLEX source file
- `iplex.c` — Sample C input file

## How to Compile and Run
```bash
flex lexer.l
gcc lex.yy.c -o lexer -lfl
./lexer iplex.c
```

## Expected Output
```
Preprocessor Directive : #include
Header File            : <stdio.h>
Keyword                : void
Identifier             : main
Delimiter              : (
Delimiter              : )
Delimiter              : {
Keyword                : int
Identifier             : x
Delimiter              : ;
Identifier             : x
Operator               : =
Number                 : 10
Delimiter              : ;
Delimiter              : }

End of file
```
