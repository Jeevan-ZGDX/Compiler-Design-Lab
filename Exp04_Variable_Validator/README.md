# Experiment 4: Recognize a Valid Variable using LEX and YACC

## Aim
To write a program to recognize a valid variable which starts with a letter followed by any number of letters or digits using FLEX and BISON.

## Files
- `valvar.l` — FLEX source file (tokenizer)
- `valvar.y` — BISON source file (parser)

## How to Compile and Run
```bash
flex valvar.l
bison -d valvar.y
gcc lex.yy.c valvar.tab.c -o valvar -lfl
./valvar
```

## Expected Output
```
Enter the variable:
add
Valid variable

Enter the variable:
add1
Valid variable

Enter the variable:
1add
Invalid variable
```
