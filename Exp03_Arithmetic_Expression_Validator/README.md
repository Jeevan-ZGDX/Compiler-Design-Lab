# Experiment 3: Recognize a Valid Arithmetic Expression using LEX and YACC

## Aim
To write a program to recognize a valid arithmetic expression that uses operators `+`, `-`, `*`, and `/` using FLEX and BISON.

## Files
- `art_expr.l` — FLEX source file (tokenizer)
- `art_expr.y` — BISON source file (parser)

## How to Compile and Run
```bash
flex art_expr.l
bison -d art_expr.y
gcc lex.yy.c art_expr.tab.c -o art_expr -lfl
./art_expr
```

## Expected Output
```
Enter the Expression
a+b*c-d/e
Valid Expression

Enter the Expression
a=b
Invalid Expression
```
