[[2023-02-19]]

1. Abbreviated notation for CONS-tructing a list
	1. Does not change our data def for lists
	2. Does not change shape of list
	3. Just a shorthand form
2. Use (list ... ... ...) operator
	1. Ex: (list "dillo" "boa" "elephant")
		1. Will create (cons "dillo" (cons "boa" (cons "elephant" empty))) for you
	2. Can be expressions that will be simplified before the list is created 
	3. Do not write empty inside the list operator (unless you explicitly want another empty list)
3. Use Beginning Student with List Abbreviations language
4. Do not write function definitions with list in them
	1. Use for check-expects or examples
5. When you are adding one thing onto a list, use cons