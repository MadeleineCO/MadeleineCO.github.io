[[2023-01-17]], [[2023-01-19]]

1. Programming and Creativity
	1. The examples of functions/programs we've seen so far may seem to have been written in a creative leap
		1. In some cases, maybe it's not clear how you would have written them on your own
	2. Programming is a creative activity but. . .
		1. Design rules can guide and focus creativity
		2. We should have a initial version of a recipe to guide design of simple programs
2. Benefits of the Design Recipe
	1. A proven, step by step process of organizing programs around problem data
	2. Saves you from staring at a blank screen (writer's block)
	3. One of the most important elements of this course!
	4. A device for diagnosing difficulties while learning to program
		1. We use it to help yourself (and as a rubric for grading)
	5. Applicable to problem-solving across disciplines
		1. Medicine, journalism, engineering, etc.
3. HtDf Recipe
	1. Signature, purpose, and stub
		1. Signature tells function name and input and output
		2. Purpose statements tell *what* the function does/produces, *not how* it achieves that purpose
			1. Should be one sentence
		3. Stub lays out a valid skeleton of our function definition 
			1. Makes sure you have a valid name, parameter, and parenthesis
	2. Define examples, wrap them in check-expect
		1. Checks the stub and later the function body
			1. The stub will probably fail whereas the function should pass
		2. AKA test cases
		3. check-expect compares the result to the expected result
	3. Template
		1. Reminds us of all the parts our function must work with
		2. Ex:
			(define (wgt-on-moon earth-wgt)
				(. . .earth-wgt. . .))
	1. Code the function body
		1. Fill in the dots from the template
	2. Test and debug until working
		1. Make sure all the tests pass
			1. If they don't, debug
4. Helper functions and reuse
	1. When writing a function, consider whether existing functions help
	2. Look for functions that you wish you had written
	3. Ex: Write (bigger-image?), which checks whether one image has more pixels than a second image
		1. We could use image-width and image-height but we could also use the simpler function (image-size)
	4. Wish list = functions we wish we could use to make life easier
		1. Fulfill wishes by applying HtDf
		2. Can create functions that you want to use in other functions
			1. Simplicity
	5. Break large problems into smaller problems
		1. Large functions can be broken down into smaller functions