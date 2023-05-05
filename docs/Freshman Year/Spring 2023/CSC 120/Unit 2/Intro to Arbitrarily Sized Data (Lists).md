[[2023-02-12]], [[2023-02-14]]

1. The *form* of the data plays in determined much of the structure of the program
	1. Determines template, number of examples, and final function definition
2. Several forms of *fixed size* data
	1. Atomic: Number, Boolean, String Image
	2. Compound: Posn, Boa
	3. One-of (mixed)
		1. Enumerations
		2. Itemizations
3. Arbitrary-sized lists of data refers to data where the size is unknown
	1. Doesn't mean infinite data, just not yet a set number
4. Aquarium Example
	1. (define-struct aq (first second))
		1. Takes in first and second fish
		2. aq-weight finds the weight of all the fish in the aquarium
		3. But then a fish dies so now aq needs to just have one fish in it
		4. Must go back and rewrite functions, structure, template, etc.
		5. But then we get two more fish, so three total. Must rewrite everything again.
		6. The choice of data doesn't work bc number of fish is not always fixed
	2. To represent an aquarium, we need a *list* of numbers
		1. (define-struct) lets us define a new kind of box w/ as many compartments as we want, but we have to pick how many boxes
			1. The boxes stretch to fit one thing in each slot
			2. Still, the number of slots is fixed after define-struct
			3. How can you create a single package?
				1. You have four things to pack as one
				2. Nested boxes to fit everything inside
			4. But what if we have 0 fish?
		2. General strategy (for any num of fish)
			1. For 0 fish, use blackbox
			2. If you have a blackbox and a new fish, put them together
			3. To combine many fish, start w/ backbox and add one fish at a time
			4. Creates nested boxes w/ fish 
				1. Innermost box contains a fish and a blackbox
		3. General Strategy for a List of Numbers
			1. To represent an aq as a list of numbers, use an **empty** list for 0 fish
			2. If you have a list and a num, put them together w/ make-bigger-list
				1. (make-empty-list)
				2. (make-bigger-list 10 (make-empty-list))
				3. (make-bigger-list 5 (make-bigger-list 10 (make-empty-list))) and so on. . .
			3. (define-struct empty-list ())
			4. (define EMPTY (make-empty-list))
			5. (define-struct bigger-list (first rest))
				1. ; A List-of-numbers is either: - EMPTY, or  - (make-bigger-list Number List-of-numbers)
					1. Self-referential
				2. ;interp. a list of weights in our aquarium is either empty or adds a weight to an existing list of weights
			6. Examples
				1. (define LON-1 (make-bigger-list 10 EMPTY)
				2. (define LON-2 (make-bigger-list 5 LON-1)
				3. (define LON-3 (make-bigger-list 7 LON-2))
			7. Template
				1. (define (lon-func a-lon)
				      (cond ((empty-list? a-lon) (...))
				            ((bigger-list? a-lon) (...(bigger-list-first a-lon) (lon-func (bigger-list-rest a-lon))...)))
			8. Function
				1. ;aq-weight : List-of-numbers -> Number
				2. ;produces the sum of all weights in the given list
				3. (c-e (aq-weight MT-LON) 0)
				4. (c-e (aq-weight LON-1) 10)
				5. (c-e (aq-weight) (make-bigger-list 12 LON-2) (+ 12 15))
				6. ((define (lon-func a-lon)
				      (cond ((empty-list? a-lon) 0)
				            ((bigger-list? a-lon) (...(bigger-list-first a-lon) (+ (aq-weight (bigger-list-rest a-lon)))))
				7. Self-referential template rule = If your template contains a self-reference, then remember to rename that to the name of the actual function you are working on when you copy the template down to create the function
5. Built-in operators for lists in BSL
	1. make-empty-list = empty
	2. empty-list? = empty?
	3. make-bigger-list = cons 
	4. bigger-list-first = first
	5. bigger-list-rest = rest
	6. bigger-list? = cons?
	7. Ex: (cons 5 (cons 10 (cons 7 empty)))
	8. CONS-truct a list from the empty list or from an existing list by adding one more item
6. DNA Base Ex
	1. Enumeration
	2. ;;A DNA base one of the strings:
	    ;; - "A"
	    ;; - "T"
	    ;; - "G", or
	    ;; - "C"
	    ;;interp. represents a nucleobase found within DNA
	3. (define (dnabase-func base . . .)
	    (cond (string=? base "A") . . .)
	              (string=? base "T") . . .)
	              (string=? base "G") . . .)
	              (string=? base "C") . . .)))
	4. ;;A List-of-dnabases is either:
	    ;; - empty, or
	    ;; - (cons DNABase List-of-dnabases)
	    ;; interp. represents a squence of nucleobases
	5. (define SEQ-1 (cons "T" (cons "A"  (cons "T" (cons "G" (cons "C" empty))))
	6. (define lodb-func a-lodb)
	    (cond ((empty? a-lodb) (. . .))
	              ((cons? a-lodb) (. . .(dna-base-func (first a-lodb)) (lodb-func (rest a-lodb)) . . .))))
		1. This is a *recursive* function
	7. ;;complementary-strand/list : List-of-dnabases -> List-of-dnabases
	   ;;produce a list of complements of the DNA bases in the given list
		1. (c-e (complementary-strand/list empty) empty)
		2. (c-e (complementary-strand/list SEQ-1) SEQ-2)
		3. (c-e (complementary-strand/list SEQ-2) SEQ-1)
		4. (c-e (complementary-strand/list (cons "G" SEQ-1)) (cons "C" SEQ-2))
		5. (define complementary-strand/list a-lodb) "B")
		6. (define complementary-strand/list a-lodb)
			(cond ((empty? a-lodb) (. . .))
				  ((cons? a-lodb) (. . .(dna-base-func (first a-lodb)) (complementary-strand/list (rest a-lodb)) . . .))))
		  7. (define complementary-strand/list a-lodb)
			    (cond ((empty? a-lodb) (empty)
				  ((cons? a-lodb) (cons (complementary-base (first a-lodb)) (complementary-strand/list (rest a-lodb))))))
		8. ;;complementary-strand : String -> String
		   ;;given a string that represents a strand of DNA, produces the complementary base
		   (c-e (complementary-strand "ATCGCCTAG") "TAGCGGATC")
			1. (explode "Hello")
				1. (cons "H" (cons "e" (cons "l" (cons "l" (cons "o" empty)))))
				2. (implode s) reverses this
			2. (define (complementary-strand dnaseq)
			        (implode (complementary-strand/list (explode dnaseq))))