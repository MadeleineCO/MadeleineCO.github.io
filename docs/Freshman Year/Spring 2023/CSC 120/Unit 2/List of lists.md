[[2023-02-19]]

1. Templates for lists (ex list-of-strings) involve structural (or natural) recursion
	1. The template calls the template func itself 
2. A List-of-list-of-strings (or LOLOS) is either
	- empty, or
	- (cons LOS LOLOS)
3. (define D-VOTES) (cons VOTES1 (cons VOTES2 (cons VOTES 3 empty)))
	1. Each votes variable is a LOS
4. (define (lolos-func a-lolos)
           (cond ((empty? a-lolos) (...)
                  (cons? a-lolos) 
                           (...(los-func (first a-lolos))... 
                               (lolos-func (rest a-lolos)...)))))
9. IO Functions allow us to read text files
	1. Ex: (read-words/line "file-name")
10. ;;total-votes : LOLOS -> Number
11. ;;computes the total number of votes over all days
12. (define (total-votes a-lolos)
          (cond ((empty? a-lolos) 0)
                     (cons? a-lolos) 
                           (+ (votes-in-day (first a-lolos)) 
                               (total-votes (rest a-lolos))))))
14. ;;votes-in-day : LOS -> Number
15. ;;computes the number of votes in a given list of votes
16. (define (votes-in-day a-los)
	    (cond ((empty? a-los) 0)
	               (cons? (+1 (votes-in-day (rest a-los)))))
17. ;;total-votes-for : String LOLOS -> Number
18. ;;produces the total number of votes for the given animal
19. (define (total-votes-for str a-lolos)
          (cond ((empty? a-lolos) 0)
                     (cons? a-lolos) 
                           (+ (daily-votes-for str (first a-lolos)) 
                               (total-votes-for str (rest a-lolos))))))
20. ;;daily-votes-for : String LOS -> Number
21. ;;produces the number of votes for the given animal in the given list of votes
22. (define (daily-votes-for str a-los)
            (cond ((empty? a-los) 0)
	               (cons? (if (strong=? str (first a-los))
	                            (+1 (daily-votes-for (rest a-los)))
	                            (daily-votes-for - (rest a-los)))))
23. ;;animals-with-votes : LOS LOLOS Number -> LOS
24. ;;produces a list of those animals in the set of votes who have exactly n total votes
25. (define (animals-with-votes animals votes num)
          (cond ((empty? animals) empty)
                     (cons? animals)
                           (if (= n (total-votes-for (first animals) votes)
                                 (cons (first animals) (animals-with-votes (rest animals) votes n)))
                                 (animals-with-votes (rest animals) votes num)))))