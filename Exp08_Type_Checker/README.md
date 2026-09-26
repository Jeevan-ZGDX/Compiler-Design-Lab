# Experiment 8: Type Checking using LEX and YACC

## Aim
To write a program using FLEX and BISON to implement type checking of variables in simple declarations and expressions, using a symbol table built during parsing.

## Files
- `typecheck.l` — FLEX source file (tokenizer)
- `typecheck.y` — BISON source file (parser & type checker)

## How to Compile and Run
```bash
flex typecheck.l
bison -d typecheck.y
gcc lex.yy.c typecheck.tab.c -o typecheck -lfl
./typecheck
```

## Expected Output

### Case 1: Valid Type Matching
```
Enter declarations and expressions:
int a;
int b;
int c;
a = b * c;
No type mismatch in expression: a = ...
```

### Case 2: Type Mismatch
```
Enter declarations and expressions:
int a;
float b;
int c;
a = b + c;
Type mismatch in assignment to a
```
