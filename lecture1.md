# Lecture 1

## Athropomorphism
Consider the similarities and the differences between human languages and programming languages.

Similarities:
* There is a syntax
  * structure to a languages
* Semantics
  * meaning to the language
* Can be used to express an algorithm

The difference? Computer languages are:
* Rigid & simple syntax
* Unambiguous
* Only for algorithms

## Considering Programming Languages
Fact: Through various methods, one program in any language can be created using *any* other language.

Question: So does it really matter which language you use for a project?

Answer: **Yes!**
Which computer language you use can influence how you think of the problem (i.e. recursive solutions) and how easily (or often) you make mistakes.

### Goals for Programming Languages
* Readable
* Simple to learn
* Portable (i.e. is it dependent on a specific OS like Mac?)
* Abstraction
  * control and data structures to hide details and organize
* Easy to catch errors early on through reading or simple debugging
* Can be compiled into efficient code

## Paradigms
**Paradigm** - how you look at the problem

Example: Print a large X pattern
```
X   X
 X X
  X
 X X
X   X
```
You can do this recursively or you can perhaps just iterate line by line.


### Imperative Paradigm
In the imperative paradigm, a program is just a sequence of instructions manipulating memory data directly.
* This fits the Von Neumann architecture closely.
* When you pass parameters, they are passed by reference.
I.e. Think of this as Assembly.

### Functional Paradigm
In the functional pradigm, a program is a collection of functions manipulating the data.
* Variables are names which may or may not map to a memory location at any given time.
* You work with the variable names rather than the memory locations directly.
* When passing parameters, you may pass by value.
* You can have recursion here rather than iteration.
I.e. Scheme/Lisp

### Logic Paradigm
Programs are rules (like in proofs from Discrete 1) with the left side representing the current conditions and the right representing the implications.
Solutions in these programs are determined by *"proving"* the theorems.

Example language: Prolog

code:
```prolog
sum(0, 0).
sum(N, S) :- N>0, X is N-1, sum(X, XX), S is N + XX.
```

### Object Oriented Paradigm
Program is oriented around communication between *objects*.
Objects can hold both data and operations/methods.
Key Operations are passing messages and invoking methods.
Example language: Java.
