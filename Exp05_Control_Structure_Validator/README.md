# Experiment 5: Recognize Valid Control Structure Syntax using LEX and YACC

## Aim
To write a program to recognize a valid control structure syntax of C language (for loop, while loop, if-else, if-else-if, switch-case, etc.) using FLEX and BISON.

## Files
- `control.l` — FLEX source file (tokenizer)
- `control.y` — BISON source file (parser)

## How to Compile and Run
```bash
flex control.l
bison -d control.y
gcc lex.yy.c control.tab.c -o control -lfl
./control
```

## Expected Output
```
Enter a C control structure syntax:
if (x < 5) { y = 10; }
(Press Ctrl+D)
Valid control structure syntax.
```

### More Test Cases
```
while (x > 0) { y = 10; }
→ Valid control structure syntax.

for (i = 0; i < 10; i = i) { x = 5; }
→ Valid control structure syntax.

switch (x) { case 1: y = 10; default: z = 20; }
→ Valid control structure syntax.

if (x < 5) { y = 10; } else { z = 20; }
→ Valid control structure syntax.
```

**Note:** Input is read from stdin. Press `Ctrl+D` (EOF) after entering the control structure to see the result.
