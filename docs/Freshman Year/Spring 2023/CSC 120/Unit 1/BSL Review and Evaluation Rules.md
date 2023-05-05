[[2023-01-12]]

1. Beginning Student Language
	1. Definitions
		1. Named constants = giving a name to an expression or value
			1. (define name expression)
		2. Functions
			1. (define (function-name param-name param-name ...) body)
		3. Expressions
			1. Simple values = 3, true, "hello", image, etc.
			2. Constant name = "rock"
			3. Call to a primitive = (+ 3 (+ 1 4))
			4. Call to a defined function = (rock-at (+ 1 2))
			5. If expression = (if question true result false result)
				1. Ex: (if (> (string-length "hi") 3)
				              "long"
				              "short")
	2. Evaluation Rules
		1. Named constant --> evaluates to whatever they've been defined as
		2. (+ 3 (+ 1 4)) --> (+ 3 5) --> 8
		3. Calls to a defined function --> first arguments reduce to simplified values --> function call is then replaced w/ body of function as arguments are substituted for parameters in the body --> function result
		4. Work from the inside out then left to right
		5. Evaluating if expressions
			1. First reduce question to simplified values
			2. Then determine if question evaluates to true or false
			3. Then determine true or false results
				1. Replace entire expression w/ true or false result
2. Stepper tool
	1. Instead of normal run, use the step tool
	2. It highlights current expression that it is evaluating in green and result of that evaluation in purple
	3. Stepping forward shows the next evaluation in green and next result in purple
	4. And so on until the program is finished running
	5. Useful for understanding how expressions are evaluated by the computer