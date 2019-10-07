# LEXICAL Language Evaluator

Freya Mehta (20171184)

To run the parser:

(1) Open `ghci`, the Haskell interactive prompt.
(2) Load the file `AST.hs`
(3) Give any expression- belonging to the LEXICAL language- as a string to the function `run`.


```haskell
$ ghci
GHCi, version 7.10.3: http://www.haskell.org/ghc/  :? for help
Prelude> :l AST.hs 
[1 of 1] Compiling Main             ( AST.hs, interpreted )
Ok, modules loaded: Main.
*Main> run "( if ( assume ( ( a True ) ) ( ~ a ) ) ( + 4 5 ) ( * 4 5 ) ) )"
20
*Main> run "( assume ( ( a 2 ) ( b 4 ) ) ( assume ( ( c 6 ) ) ( assume ( ( d 18 ) ) ( - d ( + a ( + b c ) ) ) ) ) )"
6
*Main> run "( False )"
False
*Main> 
```