[[2023-01-29]], [[2023-02-02]]

1. POSN (short for "position")
	1. Used for (x, y) coordinates
	2. Create posns by using (make-posn x y)
		1. Ex: (make-posn 14 5)
			1. (14, 5)
	3. Compound data because it has a single name (ex P1 or ORIGIN) but two values associated w/ it
		1. Ex: (define ORIGIN (make-posn 0 0))
	4. How to extract from compound data
		1. (posn-x posn) and (posn-y posn)
			1. Extracts x-coordinate or y-coordinate from a posn
			2. (Ex: (posn-x ORIGIN) = 0)
	5. When writing POSN functions, data def template looks like:
		1. (define (posn-func a-posn) 
			  (... (posn-x a-posn)
			  (posn-y a posn)))
  2. Problem Domain = the area of expertise or application that needs to be examined to solve a problem
  3. Structures
	  1. Use (define-struct)
	  2. Structure definition precedes the types comment
		  1. Ex: (define-struct boa (name length food))
		  2. DrRacket automatically introduces new operators when you run structure definition
			  1. Ex: for a Boa, (make-boa "Slinky" 10 rats)
				  1. (boa-name BOA1) -> "Slinkey"
				  2. (boa-length BOA1) -> 10
				  3. (boa-food BOA1) -> "rats"
				  4. (boa? BOA1) -> true
		  3. In general, define-struct creates 3 kinds of new operations:
			  1. One CONSTRUCTOR
				  1. make-name
				  2. Creates INSTANCES of the structures from as many values as there are fields
			  2. One SELECTOR per field
				  1. name-fieldname
				  2. Extracts the value of the field from an appropriate structure
			  3. One STRUCTURE PREDICATE
				  1. name?
				  2. Distinguishes instances of the structure from all other values
	  3. Types comment indicates how we expect structure to be used
		  1. What type of data each field contains
		  2. Ex: A Boa is (make-boa String Number String)
			  interp. a boa w/ a given name, length in feet, and favorite food
	  4. Then provide examples and a template
		  1. Template ex:
			1. (define (boa-func a-boa)
			      (...(boa-name a-boa)
			          (boa-length a-boa)
			          (boa-food a-boa) ...))
			  2. The template for a function that processes a simple structure will contain expressions that apply all the SELECTOR functions to the parameter that is the structure type
				  1. Apply the selector functions to the parameter
			  3. For additional clarity, one may also occasionally include a type comment for each selector expression to remind what type of data the field is 
			  4. Keep the template name generic by appending a-func
		2. Can write out types of pieces on the side (ex comment String or Number)
	5. Nested Structures (Structures in Structures)
		1. When a structure references another structure
			1. Ex: An Ant is (make-ant Number Posn)
				1. (posn-func (ant-loc an-ant)) to get a Posn 
					1. Must reference the other template and types comment in the nested structure template
					2. Called the "reference rule for templates"