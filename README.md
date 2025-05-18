# ProyectoLenguajes
# LL(1) and SLR(1) Parser Generator

## Group Members
- Emily Cardona Casteñeda
- Hellen Yanes Doria

## Environment and Tools
- **Operating System**: Ubuntu 22.04 LTS (compatible with any OS supporting Python)
- **Programming Language**: Python 3.11
- **Libraries Used**: None (only Python Standard Library)

## Description
This project implements a parser generator that supports both **LL(1)** (top-down) and **SLR(1)** (bottom-up) parsing strategies for context-free grammars.

It allows:
- Computing **First** and **Follow** sets.
- Building LL(1) parsing tables.
- Constructing the LR(0) automaton and SLR(1) tables.
- Parsing strings using the selected parsing method.
- Displaying the parsing tables for LL(1) and SLR(1).

The program automatically detects whether the input grammar is LL(1), SLR(1), both, or neither.

## Usage Instructions

### 1. Run the Program

### 2. Input Format
You will first be prompted to enter the number of nonterminals (n), followed by n grammar rules.
Each rule must be in the format:

No terminal -> productions  alternative

The empty string is represented by the letter e.
The end-of-input marker is $.
example:
3
S -> S+T T
T -> T*F F
F -> (S) i

### 3. Output Behavior

The program will automatically determine the type of the grammar.
If applicable, it will print the LL(1) and/or SLR(1) parsing tables.
It will then prompt you:
Select a parser (T: for LL(1), B: for SLR(1), Q: quit):

You may then enter strings one by one to be parsed.
Type an empty line to return to the main prompt.
like:
Select a parser (T: for LL(1), B: for SLR(1), Q: quit): B
i+i
yes
(i)
yes
(i+i)*i)
no

after done select Q for exit of program.
