# Expression-Calculator
📘 Expression Calculator – Reading Overview
🔹 Concept

We are building a calculator that can understand and solve mathematical expressions like:

3 + (4 * 2)


But computers don’t directly understand infix expressions (the normal way we write math).
Instead, they work better with postfix expressions (also called Reverse Polish Notation).

Example:

Infix: 3 + 4 * 2

Postfix: 3 4 2 * +

Postfix is easier for computers because it removes parentheses and precedence confusion.

🔹 Tech Requirements

Stack – A data structure where we can push and pop items (Last-In, First-Out).

Used to hold operators (+, -, *, /, %).

Also helps with parentheses.

Infix to Postfix Conversion

Convert human-readable expressions into postfix.

Rules:

Numbers (operands) → go straight to output.

Operators → pushed into stack, but follow precedence (* before +).

Parentheses () → handled specially.

Postfix Evaluation

Take postfix expression and calculate the result using another stack.

🔹 Functions Used
1. precedence(op)

Returns priority of operators.

*, /, % → higher precedence.

+, - → lower precedence.

2. infix_to_postfix(expression)

Converts infix expression (normal math) → postfix (machine-friendly).

Uses a stack to store operators.

3. evaluate_postfix(expression)

Solves postfix expression.

Uses a stack for numbers:

Push numbers.

When an operator appears, pop last two numbers, apply operator, push result back.
