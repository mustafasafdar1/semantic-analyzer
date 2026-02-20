Semantic Analyzer for Type Checking and Scope Resolution
Overview

This project implements a Semantic Analyzer for a simple programming language. The analyzer is designed to perform two critical tasks during compilation:

Type Checking – Ensures that operations are performed on compatible data types and reports type errors.

Scope Resolution – Handles variable and function scopes, ensuring that identifiers are declared before use and follow proper scope rules.

Semantic analysis is a key phase in a compiler that validates the correctness of a program beyond syntax. This project demonstrates core compiler concepts such as symbol tables, type inference, and scope management.

Features

Detects type mismatches in expressions and assignments.

Supports nested scopes and block-level scope resolution.

Generates meaningful semantic error messages.

Maintains a symbol table with variable names, types, and scope levels.

Handles function declarations and variable shadowing correctly.

How It Works

Lexical Analysis & Parsing:
The program assumes that a parser has already generated a parse tree from the source code.

Symbol Table Creation:

For each new scope (function, block), a new symbol table is created.

Identifiers are stored with attributes such as type, scope level, and value (if initialized).

Type Checking:

Binary and unary operations are checked for compatible types.

Assignments are validated to ensure the assigned value matches the variable’s type.

Scope Resolution:

Identifier lookups start from the innermost scope and move outward.

Undeclared variables trigger semantic errors.

Supports variable shadowing in nested scopes.

Example
Input Code:
int a;
float b;
a = 5;
b = a + 2.5;
c = a + b; // Semantic Error: 'c' not declared
Output:
Type Checking:
Line 4: Error - Variable 'c' is undeclared
Line 3: OK
Line 4: OK
