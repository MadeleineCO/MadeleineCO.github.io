[[2023-01-12]]

1. Example of a function in DrRacket:
	; f(w) = w/6
    (define (f w)
         (/ w 6))
	1. In the function above, f is the name of the function and w is the parameter of the function
	2. This function f takes a given weight w and divides it by 6
	3. To run this function, use the arithmetic rules:
	    (f 120)
		1. In this example, w = 120, so the end result is 20 (120/6 = 20)
2. Functions, like arithmetic expressions, compute values
	1. Depends on the value of its *input(s)*
	2. The value it produces is its output
	3. An expression like (wgt-on-moon 120) is called a function application
		1. Evaluating application of a function proceeds by copying its body, substituting the value of arguments (operands) for parameter (input) names, then simplifying (evaluating) the expression
	4. Functions eliminate redundancy
		1. Functions are a mechanism to reduce redundancy in expressions
	5. A function generalizes similar expressions (ie captures a pattern or formula)
	6. The pattern of a *function definition*:
		1. (define (function-name parameter-name body-expression))
	7. Syntax for *function application* is uniform (just like built-in operators)
		1. (function-name argument-value(s))
	8. Evaluation of function application happens by *substitution*
		1. Copy the function body, replace parameter names w/ argument values, and simplify
3. Creating animations
	1. To create animations you can make an scene using (empty scene w h)
		1. Must first do (require 2htdp/image)
	2. Then you can use (place-image), which takes four operands
		1. 1st - copy/paste your image
		2. 2nd - x location
		3. 3rd - y location
		4. 4th - (empty-scene w h)
		5. For the x and y coordinates, the top-left corner of a scene has (x,y) coordinate of (0,0)
	3. Adjust the pixels each time you place the image to create the animation
		1. Can create a function for pixel change
	4. Then add (require-htdp2/universe)
	5. Then you can call the (animate) operator