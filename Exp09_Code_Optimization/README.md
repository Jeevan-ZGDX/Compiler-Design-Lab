# Experiment 9: Code Optimization Techniques using LEX and YACC

## Aim
To write a program using FLEX and BISON to implement simple code optimization techniques such as constant folding, strength reduction, and algebraic simplification applied while parsing three-address code style assignment statements.

## Files
- `optimize.l` — FLEX source file (tokenizer)
- `optimize.y` — BISON source file (parser & code optimizer)

## How to Compile and Run
```bash
flex optimize.l
bison -d optimize.y
gcc lex.yy.c optimize.tab.c -o optimize -lfl
./optimize
```

## Expected Output
```
Enter Three Address Code statements (end with Ctrl+D):
a = 2 + 4;
// Constant Folding: 2 + 4 -> 6
a = 6

b = d * 1;
// Algebraic Simplification: x * 1 -> x
b = d

c = s * 2;
// Strength Reduction: x * 2 -> x + x
c = s + s
```
