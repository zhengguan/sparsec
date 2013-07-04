### S-Parsec: a simple parser combinator library

### Features

S-Parsec is modeled in a similar way as Haskell's Parsec library, but enhanced
with some friendly features. The concept of parser combinators is to contruct
parsers bottom-up - write parsers for small constructs first, then combine them
into bigger parsers, until you can parse the whole program.

For example, a parser for C++ function is defined as follows. Notice how similar
it is to the BNF grammar.


    (::= $function-definition 'function
         (@or (@... (@? $modifiers) $type
                    (@= 'name $identifier ) $formal-parameter-list)

              (@... (@= 'name $identifier ) $formal-parameter-list))
         (@? $initializer)
         $function-body)



### Parsers written

These experimental parsers are implemented using the library. They can parser
quite some input files, but they are not complete. My goal wasn't constructing
complete parsers for C++ or JavaScript, but just to demonstrate how parsers for
these complex syntax can be constructed in an easy way. The JavaScript parser
was written in just one day, and the C++ parser finished in two days.


* JavaScript
* C++
* Lisp family (Scheme, Clojure, Emacs Lisp, Common Lisp)

