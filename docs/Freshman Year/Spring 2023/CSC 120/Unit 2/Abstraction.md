[[2023-02-26]], [[2023-02-28]], [[2023-03-02]]

1. Abstraction = Making and using more generalized (more abstract) functions
	1. Goal: Eliminate redundancy, repetition, and similarity
	3. May look simple but actually involves a lot of thought
2. A lot of functions involve repeated parts
	1. Ex: to find weight on moon, divided weight by six
		1. Redundant to write the weight divided by six every time you want to find the weight on the moon
		2. Better to right a function
	2. Parameters give us *variability*
		1. The parameter stands for the varying value
		2. Creates functions that are more general purpose than specific expressions
	3. Ex: got-milk? vs got-eggs?
		1. Both take a-los and determine if the item is in the list
		2. We can systematically follow a process to generalize these functions using a parameter
		3. We can write the function contains?
			1. (define (contains? s a-los))
				1. (cond ((empty? a-los) false)
					1. ((cons? a-los) (or (string=? s (first a-los) (contains? s (rest a-los)))))
	4. Allows us to use fewer lines of code
	5. Ex: count-items, count-grades, count-collection
		1. All very similar
		2. Can create a more abstract function called count-elements
		3. (define (count-elements a-lothings)
			1. (cond ((empty? a-lothings) 0)
				1. (cons? a-lothings) (+ 1 (count-elements (rest a-lothings)))))
		4. Can then replace count-items, count-grades, and count-collection to just use count-elements
		5. Signature for count-elements
			1. ;;count-elements : (Listof X) -> Number
				1. Where X is a *type variable*
	6. When similarities occur in functions, we can *parameterize* in order to abstract, or generalize, our function definitions
3. Abstraction and Data Definitions
	1. Ex: List-of-numbers, List-of-strings, List-of-colors, etc. involves a lot of repitition
		1. Can create Listof X
			```python
			;;A (Listof X) is one of:
			;; - empty
			;; - (cons X (Listof X))
			```
		2. Here, X is a *type variable* (a special kind of parameter) which stands for some **type** (not a **value**) 
			1. By convention, type variables are a single upper-case letter
			2. The DD above is called *parametric*, and "Listof" is a *parametric type* (a type that has a parameter)
			3. A parametric DD abstracts from a reference to a particular collection of data in the same manner as a function abstracts from a particular value
		3. We can now talk about. . .
			1. (Listof Number)
			2. (Listof String)
			3. (Listof Color)
			4. (Listof Grade)
			5. Etc.
			6. We no longer have to do separate data definitions for Listof types
4. Designing Abstractions
	1. Systematic recipe for designing abstract function
		1. Do this when you recognize similar functions
		2. Note: This process reverses the order of some steps of the core HtDf recipe bc the easiest thing to produce is the function definition for the abstract function
			1. Tests are the next easiest thing to produce
			2. The signature and purpose can be harder (sometimes they aren't)
		3. Step 1 = Gather signatures, tests, and definitions of two or more functions
		4. Step 2 = Identify points of variation between functions
		5. Step 3 = Copy one function to make new one, w/ extra parameters
			1. Update recursive calls
			2. Use parameters at points of variability
			3. Rename list parameter to a-lox, if appropriate
		6. Step 4 = Rewrite original functions as "one-liners"
			1. One-liners can usually have fewer tests
		7. Step 5 = Adapt tests to new abstract function
			1. Be sure to test variability
			2. Write more generic examples for the function
		8. Step 6 = Study example signatures to produce the abstract signature
			1. As general as possible but not too general
5. Benefits of abstraction
	1. Shorter definitions overall
		1. Fewer lines
	2. Reduces duplication
		1. Improvements only have to happen once
			1. *Point of control* on the code
		2. Bugs only happen once
		3. Greater efficiency overall
		4. May generally improve performance bc reducing the amount of code can improve overall performance
	3. More perspicuous
		1. Shared behavior appears once
	4. Easier to understand overall
	5. Can be applied in contexts that you didn't first think of when building the function
6. Using Abstraction
	1. Abstraction = process of finding similarities or common aspects and forgetting unimportant differences
		1. Captures similarity
		2. Parameterize over differences 
		3. Functions are values in ISL
	2. Abstraction enables us to solve increasingly complex problems
	3. Functional abstraction in a programming language is the process of creating abstract functions such as 'map' or 'filter'
		1. Reduces code size
		2. Avoids copy-paste
		3. Bugs fixed/improvements in one place affect many uses
			1. Point-of-control
		4. Eases understanding by making the use of a common pattern recognizable
		5. Tackles complexity
			1. Grader and grander functions
		6. Functions like 'map' and 'filter' are called *higher-order functions* bc they take other functions as arguments (inputs)
			1. Many programming languages provide this 
			2. ISL makes it particularly easy
	4. Built-in functions
		1. map and filter
			1. These abstracted functions consume a function as well as a list and use the function to do something w/ every element in the list
			2. In other words, these "loop" over the elements in a list, performing the same operation
			3. Once you have such abstractions or looping constructs, you should use them whenever passible
		2. ISL provides a number of built-in abstract functions for processing natural numbers and lists
			1. See notes for list of some useful ones
			2. See documentation for complete list
	5. The key idea is that when you are designing a function that operates on a list, try to identify whether it has map, foldr, filter or some other abstract list function behavior.
		1. If so, build it up around a call to that function instead of thelistof template.
