[[2023-01-22]], [[2023-02-05]]

1. Sometimes need to define the data that we are working with
2. Data Definitions are made up of several parts
	1. Types comment
		1. A parameter can be a, b, or c
			1. Ex: 0, 1, or 2
	2. Interpretation
		1. Like the purpose statement
		2. Says what the data represents
	3. Template
	4. Update the statement to have specific data type
3. Information and Data
	1. The purpose of any program is to describe a computation, which transforms some collection of info into another
	2. After analyzing the problem statment to understand what info there is, . . .
		1. You must decide how to *represent* the info as data in your programming language and how to *interpret* data as info
		2. That is, choose a representation suitable for the program's input and output
		3. Info in program's domain represented by data
			1. Data interpreted as info in program's domain
4. Examples
	1. Suppose you were writing a program that involved processing the following type of info. What data representation would you use?
		1. Fahrenheit degrees 
			1. Numbers or strings
		2. Grocery items on a shopping list
		3. People's faces
		4. Wages
		5. Your grade in a course
	2. Going the other way: suppose you have a piece of data - "red"
		1. Could be many things
		2. We can't know without being told how to *interpret* it
			1. Similarly we can't represent something, like the weight of a cat, without being told how to *represent* it
			2. This is what a *data definition* does for us
				1. Tells us how to represent info as data and how to interpret data as info
5. A *Data Definition* is made up of four or five parts
	1. Possibly a *structure definition* (define-struct)
	2. A *types comment* that describes how info is represented as data
	3. An *interpretation* that describes how data of that form should be interpreted as info
	4. One or more *examples* of the data
	5. A *template* for a function operating on an input parameter of the data
6. One of the most important points of this course is that. . .
	1. The form of info in the problem determines the form of the data definition
	2. Which in turn determines the form of the examples and templates
	3. And therefore shapes and guides much of the final program design
7. Atomic Data
	1. Writing a program involving the names of cities
		1. Ex: Boston, Rome
		3. Names of cities should probably be strings
			1. Ex: "Boston" or "Rome"
		4. Simple atomic data
			1. Won't be taken apart
			2. Baselevel
		5. ;;Data Definitions
			;;CityName is String
			;;interp. the name of a city
			(define CN1 "Boston")
			(define CN2 "Rome")

			#;template
			(define (cityname-func a-cn)
				(. . .a-cn. . .))

		6. ;;Functions
			;;best-city? : CityName -> Boolean
			;;produces true if the city of the given name is the best in the world

			(check-expect (best-city? "Boston") false)
			(check-expect (best-city? "Rivendell") true)
		
			;(define (best-city? a-cn) "") ;stub
			
			;use template from CityName
			;(define (best-city? a-cn)
			;	(string=? a-cn "Rivendell"))		
8. Primitive data
	1. Ex: string, number, image
	2. HtDf
9. Non-primitive data
	1. Designed w/ HtDD
	2. Ex: atomic, intervals, enumerations, itemization, distinct
	3. HtDF, HtDD, and HtDW recipes work w/ all forms of data
		1. The recipe is mostly orthogonal to the form of data so you can cross-product easily
	4. Compound data uses HtDW
	5. List and trees can use similar recipe so easier to learn
10. Mixed data
	1. [[Compound Data]] & [[HtDD - Enumerations, Predicates, and Itemizations]]
	2. Ex: Animal
		1. An Animal is either. . .
			1. A Boa
			2. A Dillo
			3. An Ant, or
			4. A Tiger
		2. interp. a particular animal in the zoo
		3. Template
			1. (define (animal-func an-animal)
				(cond ((boa? an-animal) (...(boa-func an-animal)...))
		               	   ((dillo? an-animal) (... (dillo-func an-animal)...))
					   ((ant? an-animal) (...(ant-func an-animal)...))
					   ((tiger? an-animal) (...(tiger-func an-animal)...)))
				2. Must apply reference rules and use predicates for each type of data
	1. Forms of itemization
	2. Don't need to create examples bc previous examples in previous data definitions