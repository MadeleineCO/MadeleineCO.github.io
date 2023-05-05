[[2023-02-23]]

1. Natural numbers can be 0, 1, 2 , 3, etc.
	1. Can be an arbitrary size
	2. The smallest natural number is 0
		1. Adding one gets the next natural number
2. Amenable to processing using recursive functions
3. Basis for number theory (which, in turn, is the basis for many other things)
4. An insight for defining the natural numbers is that zero is like 'empty' in that it's the simplest (or smallest) natural number
	1. Then, whenever you have a natural number, you can add one more to it to get another one
5. Data Definition		```
	```python
	;; A Nat (short for 'natural number') is either:
			;; 0, or
			;; (add1 nat)
				;; (add1 0) = 1
				;; (add1 1) = 2
				;; (add 1 (add 1 (add1 0))) = 3
	```
	1. add1 is like cons
		1. cons has two compartments, one w/ a value and the other w/ a list (or solid box for empty)
		2. add1 is like a box w/ one compartment. Then add one boxes the inner box (creates nested boxes)
			1. Number of nested boxes is the number you are trying to represent (assuming the first, innermost box contains zero)
				3. sub1 removes one nested box
					1. Sort of like rest for lists 
			2. zero? is a predicate that provides true if the number is 0
				1. Like empty?
			3. positive? determines if the number is greater than 0 
				1. Like cons?
7. Examples
	1. Basic Operations w/ Nats
		1. Constructor
			1. add1 : Nat -> Nat
		2. Predicates
			1. zero? : Any -> Boolean
			2. positive? : Any -> Boolean
		3. Selector
			1. sub1 : Nat -> Nat
		4. (zero? 0) = true
		5. (positive? (add1 n)) = true
		6. (sub1 (add1 n)) = n
	2. (define zero 0)
	3. (define one (add1 0))
	4. 
8. Template
```python
 (define (nat-func n)
	 (cond (zero? n) (...))
		(positive? n) (...n  (nat-func (sub1 n))))
```
8. Functions
	1. ! : Nat -> Nat
	2. produces n * n-1 * n-2 * ...* 1 (note: 01 = 1)
	3. (check-expect (! 0) 1)
	4. (define (! n)
		1. (cond ((zero? n) 1)
			1. (positive? n) ( * n
					(nat-func (sub1 n))))
	5. boxes : Nat -> Image
	6. produce n nested boxes with dot inside
	7. (check-expect (boxes 0) (square 1 "solid" "black")
	8. (define (nat-func n)
		1. (cond (zero? n) (square 1 "solid" "black"))
			1. (positive? n) (overlay (square (* n 10) "solid" "black") 
					n
					(boxes (sub1 n)))))
	