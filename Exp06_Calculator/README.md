# Experiment 6: Implementation of Calculator using LEX and YACC

## Aim
To write a program to implement a Calculator using FLEX and BISON.

## Files
- `cal.l` — FLEX source file (tokenizer)
- `cal.y` — BISON source file (parser with evaluation)

## How to Compile and Run
```bash
flex cal.l
bison -d cal.y
gcc lex.yy.c cal.tab.c -o calc -lfl
./calc
```

## Expected Output
```
Enter the expression:
2+2
Answer: 4

10*5+3
Answer: 53

100/4-5
Answer: 20
```
