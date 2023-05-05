[[2023-01-10]]

1. Equality of Booleans
	1. Booleans represent truth values
		1. Yes or no. True or false.
	2. Evaluate:
		1. (= (+ 1 1)  2) = **true**
		2. (= (* 2 6)  7) = **false**
	3. Strings and images can be compared for equality too...
		1. (string=? s1 s2)
		2. (image=? i1 i2)
		3. ? = "huh"
2. Boolean Data
	1. Useful for making decisions
	2. if (...test...)
		 (...true-answer...)
		 (...false-answer...)
	 3. Operations on booleans are useful for expressing compound conditions
	 4. (or...) checks whether any of the given booleans is true
	 5. (and...) checks whether all of the given booleans are true
	 6. (not __) produces the opposite boolean
 3. Using define
	 1. If we want to define a variable, we use define
	 2. Ex: (define x 2)
		 1. Creates a *named constant*
	 3. Evaluate:
		 1. (define X 2)
			 (define Y 3)
			 (+ X Y)
			 = **5**
	 4. When evaluating, we *substitute* values for names
		 1. For the previous example...
			 (+ X Y)
			 (+ 2 3)
                       = **5**
