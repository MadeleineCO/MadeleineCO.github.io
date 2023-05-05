[[2023-03-30]]

1. Before, we have used structurally recursive functions
	1. Decompose the data into smaller pieces
	2. Lists functions
	3. Loop functions 
		1. Map, filter, etc.
	4. Structural Recursion = code whose form parallels the data definition
		1. Following the design recipe
		2. In a sense, it always works
			1. But making structural recursion work sometimes requires more creativity than solving the problem in a different, more direct way
	5. Generative Recursion = more general
		1. Recursive cases are generated based on the problem that we are solving, not based on the data
		2. Do not follow data definitions
		3. Ex: odd-items function does not strictly follow the list data def template
		4. Can be harder to come up with solutions to problems 
			1. Requires deeper analysis and domain-specific knowledge
			2. Can follow intuition
		5. Structural recursion is a special case of generative recursion that is especially common
		6. Expands our choices for designing functions
		7. Does have a template
```python
(define (func v)
	(cond [(trivial-case-1? v) ...]
		  [(trivial-case-2? v) ...]
		  [else (...
			  v
			  (func (next-problem-
			  1 v)) ...
			  (func (next-problem-2
			  v))
			  ...)]))
```
2. Trivial = function does not involve recursion
3. Next problem = a smaller problem 