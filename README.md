# Lexer and Interpreter for a Simple Functional Language in Python

## Overview
This project implements a **Lexer and Interpreter** for a **minimalistic Lisp-inspired functional language** using **finite state automata** and **recursive evaluation**. The lexer tokenizes input based on **regular expressions**, while the interpreter evaluates **lambda expressions, function applications, and list-based arithmetic operations**.

## Features
✅ **Custom Lexer** – Converts input into tokens using **regular expressions and finite automata**  
✅ **Regex to NFA to DFA Conversion** – Implements **Thompson's construction** and **subset construction algorithms**  
✅ **Functional Programming Language** – Supports **lambda expressions, function calls, and list manipulation**  
✅ **Recursive Evaluation** – Processes nested expressions until fully reduced  
✅ **Standard Library Functions** – Includes `+` (sum of elements) and `++` (list concatenation)  

## How It Works
1. **Lexical Analysis** – The lexer processes the input based on token definitions.  
2. **Parsing & Evaluation** – Expressions are parsed and recursively evaluated.  
3. **Execution** – The interpreter runs the processed input and produces an output.  

### Example Usage

#### Lexing Example
```python
spec = [("TOKEN1", "abbc*"), ("TOKEN2", "ab+"), ("TOKEN3", "a*d")]
lexer = Lexer(spec)
tokens = lexer.lex("abbd")
print(tokens)  # Output: [('TOKEN1', 'abb'), ('TOKEN3', 'd')]
