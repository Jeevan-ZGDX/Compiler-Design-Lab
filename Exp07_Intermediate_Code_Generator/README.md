# Experiment 7: Three Address Code Generation using LEX and YACC

## Aim
To write a program using FLEX and BISON to generate three-address code (TAC) for a simple arithmetic expression.

## Files
- `tac.l` — FLEX source file (tokenizer)
- `tac.y` — BISON source file (parser with intermediate code generation)

## How to Compile and Run
```bash
flex tac.l
bison -d tac.y
gcc lex.yy.c tac.tab.c -o tac -lfl
./tac
```

## Expected Output
```
Enter the expression:
a = b + c * d
t1 = c * d
t2 = b + t1
a = t2
```
