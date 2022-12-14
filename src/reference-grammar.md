# Grammar

The Pax language comprises three grammars:
 1. [Template grammar](https://www.github.com/pax-lang/pax/blob/master/pax-compiler/src/pax.pest#L05)
 2. [Settings grammar](https://www.github.com/pax-lang/pax/blob/master/pax-compiler/src/pax.pest#L69)
 3. [Expressions grammar](https://www.github.com/pax-lang/pax/blob/master/pax-compiler/src/pax.pest#L101)

Each grammar serves a specific function:
 - `templates` declare content & dynamic branching (`if`,`for`)
 - `settings` assign values to properties, optionally with CSS-like syntax
 - `expressions` allows binding properties to spreadsheet-like functions of state

Pax's parser is powered by a Parsing Expression Grammar (PEG), using [Pest](https://pest.rs/)

Rather than maintaining a separate rendition of the grammar here in the docs, refer to the [grammar in the source code](https://www.github.com/pax-lang/pax/blob/master/pax-compiler/src/pax.pest).