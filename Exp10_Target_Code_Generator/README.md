# Experiment 10: Compiler Back-End (8086 Assembly Generation)

## Aim
To write a program using FLEX and BISON to implement the back-end of a compiler which takes three-address code (TAC) as input and generates equivalent 8086 assembly language code.

## Files
- `backend.l` — FLEX source file (tokenizer)
- `backend.y` — BISON source file (parser & 8086 assembly code generator)

## How to Compile and Run
```bash
flex backend.l
bison -d backend.y
gcc lex.yy.c backend.tab.c -o backend -lfl
./backend
```

## Expected Output
```
Enter TAC statements (end with Ctrl+D):
t1 = a + b;
t2 = t1 - c;
t3 = t2 * d;
t4 = t3 / e;
x = t4;

MOV AX, a
ADD AX, b
MOV t1, AX

MOV AX, t1
SUB AX, c
MOV t2, AX

MOV AX, t2
MUL d
MOV t3, AX

MOV AX, t3
MOV DX, 0
MOV BX, e
DIV BX
MOV t4, AX

MOV AX, t4
MOV x, AX
```
