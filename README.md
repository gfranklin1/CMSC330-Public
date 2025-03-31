# CMSC330 - Organization of Programming Languages

Welcome to my repository for ```CMSC330 - Organization of Programming Languages``` at the ```University of Maryland, College Park```. This repository includes a summary and the grade received for the projects that I completed throughout this course. Due to university policies, the code for these projects is not publicly available. If you are an employer or have a legitimate request to view the code, please contact me directly.

## Projects 

### Project 1: **Ocaml Warmup**
**Description:**  
- Implemented recursive and higher-order functions in OCaml.
- Designed list manipulation algorithms (`reverse`, `merge`, `zip`, `every_nth`).
- Created numeric functions (`fibonacci`, `power`, `logarithm`, `GCD`).
- Used fold to implement higher-order functions, including uniqueness filtering and element counting (`there_is`, `count_occ`, `uniq`, `every_xth`).
- Used functional programming principles (immutability, recursion, no imperative structures).

**Grade:** 100/100

---

### Project 2: **HOFs on Trees & Database Design**
**Description:**  
- Part 1 (Database Design)
  - Designed a functional database in OCaml to store `person` records with `name`, `age`, and `hobbies`.
  - Implemented core operations: `insert`, `remove`, `sort`, `query`, `update`, and `deleteAll`.
  - Used higher-order functions to evaluate complex conditions (`And`, `Or`, `Not`, `If`) for querying/updating entries.
  - Supported comparator-based sorting and conditional data transformations.
  - Leveraged OCaml's variant types and pattern matching for condition evaluation.
- Part 2 (Higher Order Functions on Trees)
  - Created a `tree_fold` function to abstract tree traversal logic.
  - Built `map`, `mirror`, `in_order`, `pre_order`, `depth`, and `trim` using `tree_fold`.
  - Implemented `compose` to generate function compositions from tree nodes.
  - Reconstructed binary trees from pre-order and in-order traversals (`from_pre_in`).
  - Used recursion and functional programming to handle tree operations without imperative features.

**Grade:** 100/100

---

### Project 3: **Regular Expression Engine**
**Description:**  
- Implemented a comprehensive **Regular Expression Engine** capable of simulating and manipulating **NFAs (Non-deterministic Finite Automata)** and **DFAs (Deterministic Finite Automata)**.
- Developed the `accept` function to determine whether a given string is accepted by an NFA.
- Applied the **subset construction algorithm** to convert NFAs to equivalent DFAs.
- Built the `regex_to_nfa` function to translate regular expressions into NFAs using state transitions.
- Leveraged functional programming principles to ensure clean, maintainable code with no side effects.
- Utilized OCaml modules, including `Stdlib`, `List`, `Char`, and `String`, adhering to strict coding guidelines.

**Grade:** 100/100 

---

### Project 4: **SmallC Lexer, Parser, and Evaluator**  
**Description:**  
- Implemented a **lexer**, **parser**, and **evaluator** for a simplified C language in OCaml.  
  - **Lexer**:  
    - Converted input strings into tokens using regular expressions (OCaml `Re` module).  
    - Covered **core C syntax** (though not exhaustive), including:  
      - **Keywords**: Control flow (`if`, `else`, `for`, `while`), types (`int`, `bool`), I/O (`printf`)  
      - **Operators**: Arithmetic (`+`, `-`, `*`, `/`, `^`), logical (`&&`, `||`, `!`), comparisons (`==`, `!=`, `<`, `<=`)  
      - **Literals/Identifiers**: Integers, booleans (`true`/`false`), variables  
      - **Syntax**: Braces, semicolons, parentheses  
    - Resolved ambiguities (e.g., `!=` vs `!`) via longest-match prioritization.  
  - **Parser**:  
    - Built a **recursive descent parser** to construct an **abstract syntax tree**.  
    - Handled **essential C constructs**: variable declarations, assignments, loops, conditionals, and expressions with precedence.  
  - **Evaluator**:  
    - Simulated runtime execution with type checking (`int`/`bool`), scoping, and error handling (e.g., division by zero).  
    - Supported **C-like semantics** for control flow (e.g., `for` loops with bounds, `while` conditions).  

**Grade**: 100/100  

---

### Project 5: ****
**Description:**  


**Grade:** 

---

### Project 6: ****
**Description:**  


**Grade:** 


---

## Disclaimer

**## CONTACT ME IF YOU WOULD LIKE TO SEE THE CODE, UNDER UNIVERSITY RULES I AM NOT ALLOWED TO POST PUBLICLY ON HERE**

If you are interested in reviewing the code or have any questions related to the projects, please reach out to me directly.
