# Name
YIDL Is Declarative Language

Inspired by the name of YAML, since it has the same syntax

# Idea
Create a declarative programming language that has the same syntax as YAML. It can either be made as a transpiled language that would generate code in other languages, or as a language with it's own runtime and everything.

# Example
```yaml
module: main

import:
  - stdlib:
    - math:
      - plus
      - minus
      - times
      - div
    - object:
      - propOf

types:
  - person:
    - name: string
    - age: int

functions:
  main:
    params: []
    returns: void
    description: "The main function"
    body:
      - const:
        - person:
          - name: "John"
          - age: 30
      # print person's name
      - print: 
        propOf: [person, name]

  add:
    params:
      - first: int
      - second: int
    returns:
      - int
    description: "Adds two numbers"
    body:
      - plus : [first, second]
  
  sub:
    params:
      - first: int
      - second: int
    returns:
      - int
    description: "Subtracts two numbers"
    body:
      - minus : [first, second]
  
  mul:
    params:
      - first: int
      - second: int
    returns:
      - int
    description: "Multiplies two numbers"
    body:
      - times : [first, second]
  
  div:
    params:
      - first: int
      - second: int
    returns:
      - int
    description: "Divides two numbers"
    body:
      - div : [first, second]

export:
  - add
  - sub
  - mul
  - div
```

# Contribution
I don't have a clue how to write programming language. If you like the idea and would like to try it out, please help me!
