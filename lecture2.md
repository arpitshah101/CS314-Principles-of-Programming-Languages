# Lecture 2
## Scanners and Parsers
### Scanners
Used to map characters to tokens.

**Def**: tokens: basic unit of syntax.
Example: x = x + y --> <var x> <operator, assign> <var x> <operator +> <var y>  
Usually, tokens are numbers, variable names/IDs, operators (+, -, /, etc), and keywords (if, else, etc)

### Parsers
**Def**: Parse: determine grammatical structure of a token sequence  

**Def**: Grammar: Set of rules for a given sequence of tokens
Example: for x = x + y  
`assignment --> variable '=' expression ';' would be one rule`  

#### Syntax Trees
A tree of tokens representing a given sequence of characters  
Example:

```
For: x * 2 -y

                      <operation, ->
                        /       \
                       /         \
                <operation, *>   <variable, y>
                   /       \   
                  /         \
          <variable, x>   <number, 2>

```

## Language
### Defining a Language
2 things we need to focus on for defining computer languages
1. **Syntax** - what are the parts of the text and how they relate
2. **Semantics** - what are the behaviors specified by the program and how they relate

For example: a = b + c ;

Behavior:
```
calculate:
    add value of variable b
    to value of variable c
store result in variable a
```

For semantics, just use English to explain the behavior.

For syntax:
  - we use tokens defined by Regular Expressions or Finite State Automaton (Finite State Machines from Intro to Discrete 1...)
  - Context Free Grammar for larger scale structure.

#### Definitions
**Def**: Alphabet: a set of symbols  
Example: `{a, b}` or `{if, while, for,...}`

**Def**: String: sequence of symbols from the alphabet  
Example: `abbab`

**Def**: Language: set of strings  
Example: `{ab, abab, ababab, ...}`  

**Note**: each string is finite length BUT the set of strings can be infinite.  
Thus, a language can be an infinite set of strings.

## Specifying a Language

### Grammar

**Def**: Terminal Symbols: the alphabet of a language  
Terminal Symbols are the most basic unit. You can't simplify them further.  
Example: `a, b`

**Def**: Non-terminal Symbols: grammatical "categories" of the language - one of them is the "start" symbol  
Example: `MultiAB, AB`

There are also *Rules* with the following structure:  
`Non-terminal => sequence of Symbols`
Example:  
```
MultiAB => MultiAB AB
MultiAB => AB
AB => a b
```

#### Summary so far ...
* Grammars are essentially a set of rules
* Terminal symbols are the most basic symbols
* Non-terminal symbols are actually "categories" which need to be *simplified* into terminal symbols (like how you simplify or substitute math formulas when there are variables, etc)
* Each rule in a Grammar has a single Non-terminal on the left, and then a sequence of terminal AND non-terminal symbols on the right

### Regular Expressions

### Automata (Finite State Machines...)
