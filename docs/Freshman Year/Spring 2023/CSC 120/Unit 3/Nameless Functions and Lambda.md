
[[2023-03-14]]

1. Some values. . .
	1. Numbers 
	2. Booleans
	3. Lists
	4. Strings
	5. Functions *names*
		1. However, we don't have to name other types of values
		2. But, we can also avoid naming functions using **lambda**
2. Lambda
	1. An anonymous (or nameless) function value 
	2. Keyword "lambda" comes from mathematician that means "function"
	3. Ex: (lambda (a-cd) (not (zero? (cd-copies a-cd))))
		1. First parenthesis encloses parameter(s) and second encloses the body
	4. (lambda (x y ...) (... x ... y ...))
	5. Lambda represents a function that can be simplified to a value
	6. (lambda (x) (not (zero? (cd-copies x)))) returns (lambda (a1) ...)
		1. If entered directly in terminal
		2. (lambda (dht) (not (zero? (cd-copies dht)))) returns (lambda (a1) ...)
		4. Never produces a different result
		5. DrRacket doesn't bother spitting back the body of the function
	7. (lambda (x) (+ x 10)) returns (lambda (a1) ...)
		1. ( (lambda (x) (+ x 10)) 17 ) returns 27
			1. Function calls doesn't need an identifier (concrete name of function or variable)
3. Function-Producing Functions
	1. We already have functions that take function arguments
		1. Ex: map
	2. How about functions that produce functions?
4. Lambda in Math
	1. (define (derivative f) 
		 ...)
		 1. ;derivative : (Number -> Number) -> (Number -> Number)
		 2. Takes a function and produces the derivative of that function
5. Lambda in Real Life Programming
	1. GUIs often use functions as values, including anonymous functions
		1. Java equivalent = inner "function object" classes
	2. Button click -> update bottom text
	3. gui.ss : Simple Graphical User Interfaces teachpack