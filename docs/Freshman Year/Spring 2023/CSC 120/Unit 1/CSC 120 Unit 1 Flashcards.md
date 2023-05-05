---
cards-deck: docs::Spring 2022::CSC 120::Unit 1
---

[[2023-01-11]]

Computation::Processing and manipulating info; We describe computation as a *program*; Info expressed in a program is called *data*
^1673480287077

Examples of data::Numbers, characters, strings, strings, booleans; Data also called operands while functions are operators
^1673480287092

Arithmetic is a form of ---::computing; Fixed, pre-defined rules for *primitive operators*, such as evaluate subexpressions first in order of precedence
^1673480287099

Simplified Expression Notation::Racket Notation; Start every operation w/ an open parenthesis; Put the operator first, right after (; List arguments (operands) for the operator; Put a close parenthesis ) after the last argument; Never add extra parenthesis
^1673480287106

Text info is represented as a sequence of keyboard characters enclosed in ---::double-quotes "..."; Called a *string*
^1673480287115

(string-append s1 s2)::string-append is to strings as + is to numbers; Adds the two strings together
^1673480287123

(string-length s)::Consumes a string and produces its length
^1673480287131

(string-ith s i)::Extracts a one-character substring located at the i'th position in string s (counting from 0)
^1673480287139

(substring s i j)::Extracts a substring of characters from string s, located at position i (inclusive) up to position j (exclusive)
^1673480287147

(number->string n)::Converts a numeric value to a string
^1673480287158

When evaluating operations on strings, follow ---::similar rules to arithmetic of numbers
^1673480287166

To use primitive operations to create new images, you must first ---::enter (require 2htdp/image) and run on DrRacket; Ex of primitive operation:: (circle d "style" "color")
^1673480287175

Operations relating to the properties of images::(image-width i); (image-height i)
^1673480287183

Operations that combine images::(overlay i1 i2); (above i1 i2); (below i1 i2)
^1673480287191

Booleans::Represent truth values (true or false); Numbers, strings, and images can all be compared for equality
^1673480287198

Boolean operations::Numbers - (= n1 n2); Strings - (string=? s1 s2); Images - (image=? i2 i2)
^1673480287206

If statements::if (...test...) / (...true-answer...) / (...false-answer...); Useful for making decisions based off booleans
^1673480287213

Operations on booleans are useful for expressing ---::compound conditions; (or...) checks whether any of booleans is true; (and...) checks whether all of booleans are true; (not...) produces the opposite boolean
^1673480287220

To create variables, we use ---::define operation; Ex: (define x 2) creates a *named constant*
^1673480287226

[[2023-01-13]]
Functions, like arithmetic expressions, compute ---::values; Output depends on the value of its *input*
^1673635721939

Evaluating application of a function proceeds by ---::copying its body, substituting the value of arguments (operands) for parameter (input) names, then simplifying (evaluating) the expression; Evaluation happens by *substitution*
^1673635721948

Functions eliminate ---::redundancy; Functions are a mechanism to reduce redundancy in expressions
^1673635721955

Pattern of a *function definition*::(define (function-name  parameter-name  body-expression))
^1673635721962

To create animations, you can make a scene using ---::(empty-scene w h); Must first do (require 2htdp/image); Then use (place-image), which takes four operands; Then add (require htdp-2/universe) and call the (animate) operator
^1673635721969

Named constants::Giving a name to an expression or value (define name expression)
^1673635721977

Functions::(define (function-name param-name param-name ...) body)
^1673635721983

If expression::(if question true-result false-result); When evaluating, first reduce question, then determine true or false, then replace expression w/ true or false result
^1673635721990

Programming is a creative activity but ---::design rules can guide and focus creativity; We should have an initial version of a recipe to guide design of simple programs (HtDf)
^1674084067345

HtDf Recipe::1 - Signature, purpose, and stub; 2 - Define examples using (check-expect); 3 - Template; 4 - Code the function body; 5 - Test and debug
^1674084067353

A program's signature tells the ---::function name and input and output (Ex: ;;add-numbers : Number -> Number))
^1674084067360

Purpose statements tell *what* the function ---::does/produces, not *how* it achieves that purpose; Should be about one sentence
^1674084067367

A stub lays out a valid ---::skeleton of our function definition; Makes sure you have a valid name, parameter, and parenthesis
^1674084067375

(check-expect (function param(s)) expected-result)::Used to define examples, check your stab (which will probably fail) and your function body (which should pass); AKA test cases; Compares the actual result to the expected result
^1674084067382

A template reminds us of ---::all the parts our function must work with; Ex: (define (function param) (. . .param. . .))
^1674084067389

When coding the function body, just ---::fill in the dots from the template then test and debug to make sure your (check-expect) tests pass
^1674084067396

[[2023-01-19]]
When writing a function, consider whether ---::existing functions may help; Look for functions that you wish you'd written and make a wish list
^1674183162474

Wish list::Functions we wish we could use to make life easier; Fulfill wishes by applying HtDf; Can create functions that you want to use in other functions; Increases  simplicity by breaking large problems into smaller problems
^1674183162484

Cond expressions can be used instead of ---::nested if-statements to handle multiple decisions; (cond (Q A) (Q A). . .); Each question must evaluate to a boolean; Last question can be else; One or more question-answer pairs
^1674183162496

[[2023-01-23]]
The purpose of any program is to describe a ---::computation, which transforms some collection of info into another
^1674504383917

Programmers must decide how to --- the info as data in a program and how to --- data s info::represent; interpret; Must choose a representation suitable for the program's input and output
^1674504383927

Info in a program's domain is represented by ---::data; Data must be interpreted as info in a program's domain
^1674504383934

A data definition tells us how to --- info as data and how to --- data as info::represent; interpret
^1674504383941

Parts of a data definition::1 - structure definition (define-struct); 2 - types comment (describes how info is represented as data); 3 - interpretation (describes how data of that form should be interpreted as info); 4 - examples of the data; 5 - template (designed for a function operating on an input parameter of the data)
^1674504383948

The form of info in the problem determines the ---::form of the data definition (which in turn determines the form of the examples and templates and therefore shapes and guides much of the final program design)
^1674504383955

Non-primitive data::Designed w/ HtDD; Ex: atomic data, intervals, enumerations, itemization, distinct; Compound data uses HtDW; The formulas for such data are orthogonal to the form of data so you can cross-product easily
^1674504383962

Ex of types comment (HtDD)::A ScovilleRating is a number: - between 0 and 100 - between 2500 and 8000 
^1674504744122

Ex of interpretation (HtDD)::interp. the Scoville rating of a pepper where 0-100 represents a bell pepper, 101-200 represents a serrano, ---
^1674504744133

Ex of examples (HtDD)::(define RIPE-BELL 55)
^1674504744140

Ex of a template (HtDD)::(define (scoville-rating-func a-rating) (cond ((<= 0 a-rating 100) (...a-rating...)) ((<= 2500 a-rating 8000) (...a-rating...)) ((<= 10000 a-rating 23000) (...a-rating...) (else (...a-rating...))))
^1674504817611

[[2023-01-25]]
An *enumeration* specifies ---::distinct, individual elements from an existing class of data ("A" "B" "C" "D")
^1674658751438

Predicates::Functions that return true or false (a boolean value); Used to distinguish the classes of data that we know so far (ex string? number?)
^1674658751446

An *itemization* generalizes ---::intervals and enumerations; Used when info consists of two or more subcategories, at least one of which is not a distinct data item
^1674658751453

Interval::A data definition that distinguishes different subclasses or ranges of numbers
^1674658751461

Enumeration::A data definition that specifies distinct individual elements from some existing class of data (ex strings)
^1674658751467

Itemization::A data definition that allows us to combine existing types of data; AKA mixed data; Often uses comparison, equality operators, or type predicates in the function
^1674658751475

[[2023-01-27]]
Rendering::The process of generating an image from a model, by means of a computer program
^1674847647800

(big-bang) operator::Uses (require 2htdp/universe); Takes an initial piece of data and several arguments (ex (on-tick ...) (to-draw ...) (on-key ...) (on-mouse ...) (stop-when ...))
^1674847647816

Cat example of (big-bang) operator::(big-bang 10 (on-tick advance-cat) (to-draw render)); 10 = initial position of the cat image
^1674847647824

TL example of (big-bang) operator::(big-bang "red" (on-tick next-color 1) (to-draw make-traffic-light)); "red" = initial color; 1 = one second pause before switching colors
^1674847647832

Key presses example::(handle-key 120 " "); 120 = initial position, if " " is pressed, an image moves to position 0
^1674847647839

Key presses update the ---::state of the world based on the key pressed
^1674847647847

User Interface Framework::Integrates pieces of functionality; Similar to real world frameworks
^1674847647855

Designing World Programs::Domain analysis (pencil + paper) - Sketch program scenarios, Identify constant info, Identify changing info, Identify big-bang options; Build the actual program - Constants, Data definitions, Functions, Work through wish list until done
^1674847647863

!!! indicates functions that are ---::apart of the wish list
^1674847647870

[[2023-01-30]]
Posn::Short for position; Used for (x, y) coordinates; Create posns by using (make posn x y); Ex: (make-posn 14 5) -> (14, 5)
^1675110743233

Posn is an example of --- data::compound; Has a single name (ex P1 or ORIGIN) but two values associated w/ it; Ex: (define ORIGIN (make-posn 0 0))
^1675110743246

How to extract from compound posn data::Used (posn-x posn) and (posn-y posn)
^1675110743254

When writing posn functions, the data def template looks like ---::(define (posn-func a-posn)  (... (posn-x a-posn) (posn-y a posn)))
^1675110743261

[[2023-02-01]]
Problem Domain::The area of expertise or application that needs to be examined to solve a problem
^1675263416745

When defining structures, use ---::(define-struct structure-name (parameters)); Ex: (define-struct Boa (name length food))
^1675263416756

DrRacket automatically introduces new --- when you run structure definitions::operators; One constructor (make-name), One selector per field (name-fieldname), One structure predicate (name?)
^1675263416764

Types comment indicates how we expect structures to ---::be used; What type of data each field contains; Ex: A Boa is a (make-boa String Number String) and interp. a Boa w/ a given name, length in feet, and favorite food
^1675263416874

Must provide a --- for structure definitions::template; Ex: (define (boa-func a-boa) (...(boa-name a-boa) (boa-length a-boa) (boa-food a-boa)...)); Template contains expressions that apply all the selector functions to the parameter
^1675263416880

For additional clarity when writing structure definitions, one may also occasionally include a --- for each selector expression::type comment; Reminder of what type of data the field is
^1675263416889

[[2023-02-03]]
Nested Structures (Structures in Structures)::When a structure references another structure; Ex: An Ant is a (make-ant Number Posn)
^1675470754818

When created templates for data definitions of nested structures, you must apply the --- rule::reference; Must reference the other template function within the nested structure template body; Ex: An Ant is a (make-ant Number Post) so the template would be: (define (ant-func an-ant) (ant-age an-ant) *(posn-func (ant-location an-ant))*)
^1675470754829

[[2023-02-06]]
Mixed data (itemization) example: Animal::An Animal is either. . . - A Boa  - A Dillo  - An Ant, or  - A Tiger; interp. a particular animal in the zoo
^1675712625439

Animal ex template for mixed data (itemization)::(define (animal-func an-animal)(cond ((boa? an-animal) (...(boa-func an-animal)...))  ((dillo? an-animal) (... (dillo-func an-animal)...))  ((ant? an-animal) (...(ant-func an-animal)...))  ((tiger? an-animal) (...(tiger-func an-animal)...)))
^1675712625451

When creating templates for mixed data (itemizations), you must apply the ---::reference rules and use predicates for each type of data within the cond expression; Don't need to create examples later bc previous examples in previous data definitions
^1675712625460
