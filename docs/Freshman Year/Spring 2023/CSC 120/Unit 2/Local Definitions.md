[[2023-03-12]]

1. General syntax of the local construct is:
```python
(local [...<definitions>...]
	<body>)
```
2. Definition only exists within the function
	1. Outside of the local, they do not exist
3. Closure = Function that accesses a variable that's defined in an outer scope
	1. Can create a local function that is nested inside the outer function and can use its variables
4. There are three principal ways to use local. They are, in order of simplest to most complex, . . .
	1. Giving names to intermediate values
		1. As in "random-choice"
	2. Avoiding recomputation of values
		1. As in "max-nums"
	3. Encapsulation (grouping)
		1. As in "sort-list"