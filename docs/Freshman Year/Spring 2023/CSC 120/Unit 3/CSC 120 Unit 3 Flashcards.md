---
cards-deck: docs::Spring 2023::CSC 120::Unit 3
---

---
cards-deck: docs: Spring 2023: CSC 120: Unit 3
---

[[2023-03-15]]
Ex of values::Numbers, Booleans, Lists, Strings, Function *names*; However, we don't have to name other types of values so in ISL, can avoid naming functions by using **lambda**
^1678908645641

Lambda::An anonymous (or nameless) function value; Keyword "lambda" comes from a mathematician, and it means "function"
^1678908645656

Ex of lambda::(lambda (a-cd) (not (zero? (cd-copies a-cd)))); First parenthesis encloses parameter(s) and second encloses body
^1678908645667

Lambda format::(lambda (x y) (... x ... y ...))
^1678908645677

Lambda represents a function that can be ---::simplified to a value
^1678908645685

If entered directly into terminal, any lambda function produces ---::(lambda (a1) ...); Doesn't bother spitting back the body of func or specific parameter(s)
^1678908645692

Function-Producing Functions::We already have functions that take functions as arguments (ex map); How about functions that produce functions?; Body of func can include lambda
^1678908645699

[[2023-03-24]]
Data def for a horse pedigree is an example of a ---::tree; More complicated than just a list; Individual horses at the top called leaves
^1679710390422

The data def for a horse pedigree (tree) must be ---::self-referential; Two references of horse-func bc it references itself twice within the DD
^1679710390433

[[2023-03-27]]
Non-binary trees::Possibility of more than two branches; Ex: A Horse is a (make-horse String Number String List-of-horses); This is a *mutually referential DD* for list-of-horses and horses bc they reference each other
^1679945444661

[[2023-03-29]]
The quote operator is shorthand for ---::list, which is shorthand for cons; quote is easier for making a list of lists
^1680128170704

Quote freezes everything within it so that no --- occurs::evaluation or simplification 
^1680128170715

Symbol is another --- data type::atomic; Like a string but cannot manipulate it 
^1680128170721

Quote is distributed to everything ---::inside it
^1680128170727

'"hello" or '14 simply returns ---::the data inside it ("hello" or 14)
^1680128170732

Quasiquote can "unfreeze" info by adding a ---::comma in front of desired expression; Allows you to simplify specific parts of your list
^1680128170739

With quote, you can turn functions into frozen pieces of ---::data; Made up of lists, symbols, strings, booleans, numbers, etc. but just one piece of data that can be manipulated as a whole (S-expressions)
^1680128170746

[[2023-03-31]]
Structurally recursive functions decomposed the data into ---::smaller pieces (ex list or loop functions)
^1680288604499

Structural Recursion::Code whose form parallels the data definition; Follows the design recipe; In a sense, always works, but may be more difficult than solving issue in direct way
^1680288604507

Generative Recursion::More general than structural; Recursive cases generated based on problem, not data; Does not follow data definitions
^1680288604512

Generative recursion requires deeper ---::analysis and domain-specific knowledge; Can follow intuition 
^1680288604518

Structural recursion is a special case of ---::generative recursion that is especially common
^1680288604523

[[2023-04-17]]
(set! <variable> <expression>) is an expression with no value (void). It evaluates<expression>, and then ---::changes the already defined variable <variable> to have that value. If <variable> isn’t already defined, it’s illegal.
^1681779817827

Mutable variables are variables that can change their value after they are ---::defined.
^1681779817840

IMPERATIVE STYLE PROGRAMMING::Traditional; Involves sequencing; Testing is difficult
^1681779817848

FUNCTIONAL STYLE PROGRAMMING = Racket (less dependency on sequences; Handles one thing at a time) - more mathematically based; Makes check-expects easy! (isolation and localization)

[[2023-04-19]]
for-each is like map in that it calls the function once with each item in the ---::list. Unlike map it discards whatever results the function might return. It is calling the function for effect only.
^1681947436266

