---
cards-deck: docs::Spring 2023::CSC 120::Unit 2
---

[[2023-02-13]]

The *form* of the data plays in determined much of the --- of the program::structure; Determines template, number of examples, and final function definition
^1676323335579

Several forms of *fixed size* data::Atomic: Number, Boolean, String Image; Compound: Posn, Boa; One-of (mixed) (Enumerations, Itemizations)
^1676323335593

Arbitrary-sized lists of data refers to data where the size is ---::unknown; Doesn't mean infinite data, just not yet a set number
^1676323335600

General Strategy for a List of Numbers::To represent an aq as a list of numbers, use an **empty** list for 0 fish; If you have a list and a num, put them together w/ make-bigger-list; (make-empty-list); (make-bigger-list 10 (make-empty-list)); (make-bigger-list 5 (make-bigger-list 10 (make-empty-list))) and so on.
^1676323335606

List DD::(define-struct bigger-list (first rest)) ;; A List-of-numbers is either: - EMPTY, or  - (make-bigger-list Number List-of-numbers) - *Self-referential* - ;;interp. a list of weights in our aquarium is either empty or adds a weight to an existing list of weights
^1676323335614

List Examples::(define LON-1 (make-bigger-list 10 EMPTY); (define LON-2 (make-bigger-list 5 LON-1); (define LON-3 (make-bigger-list 7 LON-2))
^1676323335621

List Template::(define (lon-func a-lon) (cond ((empty-list? a-lon) (...)) ((bigger-list? a-lon) (...(bigger-list-first a-lon) (lon-func (bigger-list-rest a-lon))...)))
^1676323335630

Self-referential template rule::If your template contains a self-reference, then remember to rename that to the name of the actual function you are working on when you copy the template down to create the function
^1676323335637

make-empty-list BSL Equivalent::empty
^1676323335644

empty-list? BSL Equivalent::empty?
^1676323335652

make-bigger-list BSL Equivalent::cons 
^1676323335659

bigger-list-first BSL Equivalent::first
^1676323335666

bigger-list-rest BSL Equivalent::rest
^1676323335674

bigger-list? BSL Equivalent::cons?
^1676323335681

Creating a list Ex::(cons 5 (cons 10 (cons 7 empty))); CONS-truct a list from the empty list or from an existing list by adding one more item
^1676323335688

[[2023-02-14]]
Enumeration DNAbase DD template::(define (dnabase-func base . . .) (cond (string=? base "A") . . .) (string=? base "T") . . .) (string=? base "G") . . .) (string=? base "C") . . .)))
^1676509049207

List-of-DNAbases DD template::(define lodb-func a-lodb) (cond ((empty? a-lodb) (. . .)) ((cons? a-lodb) (. . .(dna-base-func (first a-lodb)) (lodb-func (rest a-lodb)) . . .)))); This is a *recursive* function bc it calls itself
^1676509049225

[[2023-02-20]]
Abbreviated notation for CONS-tructing a list::Use the (list ... ... ...) operator; Does not change our data def for lists; Does not change shape of list; Just a shorthand form
^1676924164130

When using the list operator, do not write ---::empty at the end (unless you explicitly want another empty list); Do not write function definitions using list (just use for c-e or examples); When you are adding one thing onto a list, use cons instead
^1676924164143

Templates for lists (ex list-of-strings) involves --- recursion::structural (or natural); The template calls the template func itself
^1676924164151

[[2023-02-24]]
Natural numbers can be an --- size::arbitrary; 0, 1, 2, 3, etc; Adding one gets the next natural number
^1677276440876

Using natural numbers as amenable to processing using recursive functions

Natural numbers for the basis of --- theory::number; Number theory, in turn, is the basis for many other things
^1677276440882

An insight for defining the natural numbers is that zero is like ---::empty in that it's the simplest (or smallest) natural number
^1677276440886

DD for Nat::A Nat (short for 'natural number') is either: - 0, or  - (add1 nat)
^1677276440893

For natural numbers, add 1 is like ---::cons, which has two compartments, one w/ value and other w/ a list (or solid box for empty); add1 is like a box w/ one compartment, and adding one boxes the inner box (number of nested boxes is number you are trying to represent assuming the innermost box contains zero
^1677276440898

sub1 removes ---::one nested box for natural numbers; similar to (rest ...) for lists
^1677276440903

zero?::predicate that provides true if the number is 0; Like empty? but for natural numbers
^1677276440909

positive?::determines if the number is greater than 0; Like cons? but for natural numbers
^1677276440915

Nat Constructor::add1 : Nat -> Nat; (define one (add1 0))
^1677276440921

Nat Predicates::zero? : Any -> Boolean *and* positive? : Any -> Boolean; (zero? 0) = true; (positive? (add1 n)) = true
^1677276440927

Nat Selector::sub1 : Nat -> Nat; (sub1 (add1 n)) = n
^1677276440933

Template for Nat functions::(define (nat-func n) (cond (zero? n) (...)) (positive? n) (...n...(nat-func (sub1 n)))); Very similar to list template function
^1677276440939
[[2023-02-27]]
Abstraction::Making and using more generalized (more abstract) functions; Goal is to eliminate redundancy, repetition, and similarity
^1677527211875

A lot of functions involve repeated parts, but using parameters gives us ---::variability; the parameter stands for the varying value; Creates functions that are more general purpose than specific expressions
^1677527211884

Both got-milk? and got-eggs? take a-los and determine if item s is in the list. We can systematically follow a process to ---::generalize these functions using a parameter; We can write the function contains? (ex of abstraction)
^1677527211889

Abstraction allows us to use --- lines of code::fewer; When similarities occur in functions, we can *parameterize* in order to abstract, or generalize, our function definitions
^1677527211896

In Listof X, X i- a ---::type variable (a special kind of parameter), which stands for some *type* (not a *value*); By convention, type variables are a single upper-case letter
^1677527211901

The DD for Listof X is called ---::parametric, and "Listof" is a *parametric type* (a type that has a parameter)
^1677527211907

A parametric DD abstracts from a reference to a particular collection of data in the same manner as ---::a function abstracts from a particular value
^1677527211914

Listof X allows us to no longer write separate DD for ---::Listof types; (Listof Numbers), (Listof String), (Listof Color), etc. can all be created using Listof X
^1677527211920

[[2023-03-01]]
There is a systematic recipe for designing abstract  ---::functions; Follow when you recognize similar functions; Note: reverses order of some steps in HtDf recipe bc easiest thing to produce is the function definition for the abstract function (then tests then signature and purpose, which are hardest)
^1677723142601

Abstract function recipe::1 - Gather signatures, tests, and definitions of two or more functions; 2 - identify points of variation between functions; 3 - copy one function to make new one w/ extra parameters; 4 - rewrite original functions as "one-liners"; 5 - adapt tests to new abstract function; 6 - study example signatures to produce the abstract signature
^1677723142611

Benefits of abstraction::Shorter definitions and fewer lines; Reduces duplication (creates a single *point of control*); More perspicuous (shared behavior appears once); Easier to understand; Can be applied in contexts that you didn't first think of when building the func
^1677723142619

[[2023-03-03]]
Abstraction is the process of ---::finding similarities or common aspects and forgetting unimportant differences; Captures similarity; Parameterize over differences; Functions can be values in ISL
^1677871762304

Abstraction enables us to solve increasingly ---::complex problems
^1677871762317

Functional abstraction in a programming language is the ---::process of creating abstract functions such as 'map' or 'filter'
^1677871762323

More Benefits of Abstractions::Reduces code size; Avoids copy-paste; Bugs fixed/improvements in one place affect many uses (point of control); Eases understanding by making the use of a common pattern recognizable; Tackles complexity
^1677871762327

Functions like 'map' and 'filter are called --- bc they take other functions as arguments (inputs)::higher-order functions; Many programming languages provide this
^1677871762333

map and filter are built in abstracted functions that consume a function as well as a list and use the function to ---::do something w/ every element in the list; Loop over elements in list while performing same op
^1677871762339

Once you have abstractions or looping constructs, you should use them ---::whenever possible
^1677871762346

The key idea of using looping constructs is that when you are designing a func that operates on a list, try to identify whether it has ---::map, foldr, filter, or some other abstract list func behavior; If so, build it up around a call to that func instead of the list-of template
^1677871762352

[[2023-03-13]]
General syntax of local construct::(local (. . .definitions. . .)  . . .body. . .)
^1678734876778

In local constructs, the definition only exists within the ---::function; Outside of local, they do not exist
^1678734876786

Closure::A function that accesses a variable that's defined in an outer scope; Can create a local function that is nested inside the outer function and can use its variables
^1678734876794

Three principal ways to use local (from simplest to most complex)::1 - Giving names to intermediate values; 2 - Avoiding recomputation of values; 3 - Encapsulation (grouping)
^1678734876803

