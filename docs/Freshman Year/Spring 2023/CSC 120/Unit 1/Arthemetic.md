[[2023-01-10]]

1. Computation = processing and manipulating information
	1. We describe computation as a *program*
	2. Info expressed in a program is called *data*
	3. Information comes in many types
		1. Ex: Numbers, letters, words, symbols, images
2. Arithmetic
	1. Evaluate:
		1. 1 + 2 = **3**
		2. 4 x 2 = **8** 
		3. sqrt(16) = **4**
		4. cos(0) = **1**
		5. 2^3 = **8**
		6. 4 x (2+3) = **20**
		7. 4 x 2 + 3 = **11**
		8. Takes complex expression and reduces it into a value
	2. Arithmetic is computing
		1. Fixed, pre-defined rules for *primitive operators*
		2. Rules for combining other rules
			1. Evaluate subexpressions first
			2. Precedence determines subexpressions
		3. Standard Math Notation
			1. Why do some primitive operators go in the middle, like "+" while others go at front, like cos, and yet others use subscript/superscript notation?
			2. What are the precedence rules?
			3. How do we know which arguments (operands) go with which operators?
			4. When are parentheses redundant?
			5. You're used to these questions bc you've been programmed :)
	3. Evaluate:
		1. (+ 2  3) = **5**
		2. (* 4  5) = **20**
		3. (sqrt  25) = **5
		4. (cos 0) = **1**
		5. (expt 2  4) = **16**
		6. (*  4 (+ 2  3)) = **20**
		7. (+ 4 (*  2  3*)) = **10**
		8. (+ 1  2  3  4) = **10**
		9. (* 2  4  5*) = **40**
	4. Simplified Expression Notation (Racket Notation)
		1. Start every operation w/ an open parenthesis
		2. Put the operator first, right after (
		3. List arguments (operands) for the operator
		4. Put a close parenthesis ) after the last argument
		5. Never add extra parenthesis
	5. The Language(s) of this Course
		1. Beginner/Intermediate Student Language (BSL+, ISL+)
		2. Based on a full-fledged language named Racket
	6. Arithmetic of Numbers
		1. "Arithmetic" to most people means "operations on numbers"
		2. We will add on to this definition