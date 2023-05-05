
[[2023-03-23]], [[2023-03-26]]

1. Horse Pedigrees
	1. Data def for a horse pedigree is an example of a *tree*
		1. More complicated than just a list
		2. If each has at most two branches, called a binary tree
	~~~python
	(define-struct horse (name yob color sire dam))
;; A Horse is one of:
;;   - empty, or
;;   - (make-horse String Number String Horse Horse)
;; interp. represents a horse with pedigree information
;;         where 'empty' represents an unknown horse~~~

	2. Individual horses are called *leaves*
	3. Two occurrences of Horse
		1. Self-referential data definition 
		2. References itself twice
		3. Important for the creating the template of the data definition
~~~python
(define (horse-func a-horse)
  (cond
    [(empty? a-horse)  ...]
    [(horse? a-horse) (... (horse-name a-horse)
                           (horse-yob a-horse)
                           (horse-color a-horse)
                           (horse-func (horse-sire a-horse))
                           (horse-func (horse-dam a-horse)))])~~~
2. Non-binary trees (possibility of more than two branches)
	1. A Horse is (make-horse String Number String List-of-horses)
	2. Mutually referential data definitions for list-of-horses and horses bc they reference each other
```python
;;templates
(define (horse2-func a-horse)
  (...(horse-name a-horse)
     (horse-pob a-horse)
     (horse-color a-horse)
     (loh-func (horse-offspring a-  
      horse))))

(define (loh-func a-loh)
  (cond
    [(empty? a-loh) ...]
    [(cons? a-loh) (...(horse2-func  
                   (first a-loh)
                    (loh-func (rest a-
                     loh))))]))

```