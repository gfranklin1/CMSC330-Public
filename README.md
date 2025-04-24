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

### Project 5: **SmallC Optimizer & Type System**  
**Description:**  
- Continuation of Project 4, with the addition of an **optimizer**, **type checker**, and **type inferencer** for a simplified C language in OCaml.
  - **Optimizer:**
    - **Constant folding** (e.g. `(3+4)*6 → 42`), **constant propagation**, and **branch folding** (`if true then s1 else s2 → s1`).  
    - **Loop simplifications**: remove dead `while(false)` loops, simplify `for` when bounds are known, preserve the initial binding on empty loops.  
    - Raises `DivByZeroError` on compile‑time division by zero and `DeclareError` on unbound variables.  
  - **Type checker:**
    - Syntax‑directed check over the same SmallC AST, with support for `Int_Type`, `Bool_Type`, and `Unknown_Type _`.  
    - Environment threading through sequenced statements, proper merge of branch environments in `if`.  
    - Raises `TypeError` for mismatches and `DeclareError` for uses of undeclared identifiers.  
  - **Type inferencer:**
    - Constraint‑solving type inference for `read()` (“`Value`”) unknowns: generates constraints, unifies (with occurs‑check), and rebuilds the AST with all `Unknown_Type _` resolved to either `Int_Type` or `Bool_Type`.  
    - Correctly threads environments through `while` and `for` so that loop‑body bindings aren’t lost.  
    - Verifies the final, annotated AST with the same `typecheck` to guarantee soundness.  

**Grade:** 94/100
- Passed 35/37 tests.

---

### Project 6: **Rust Intro**
**Description:**
- Implemented **6 core functions** in Rust to familiarize with syntax, safety, and standard library features.  
- **Key Functions:**  
  - **Gauss Sum**:  
    - Computed the sum of integers from 1 to `n` using the formula `(n*(n+1))/2`.  
    - Returned `None` for non-positive inputs.  
  - **Double Up and Dance**:  
    - Doubled elements in a slice to create a new `Vec`.  
    - Modified the fifth element of the new vector by multiplying it with the second element of the original slice (if length ≥5).  
  - **Binary String Conversion**:  
    - Converted unsigned integers to binary strings without leading zeros (e.g., `9` → `"1001"`).  
  - **Range Counting**:  
    - Counted elements in an iterator within a given `Range<i32>` (start inclusive, end exclusive).  
  - **In-Place Capitalization**:  
    - Capitalized the first letter of each string in a mutable iterator (e.g., `"hello"` → `"Hello"`).  
  - **Vending Machine Parser**:  
    - Parsed a file into a `HashMap` of item-price pairs using regex validation.  
    - Enforced rules: prices 1-50 cents, no duplicates, and strict line formatting (e.g., `item; 50c`).  
    - Returned `None` for invalid lines, duplicates, or prices outside bounds.  

**Rust Features Used:**  
- **Iterators**: Leveraged `impl IntoIterator` for flexible input handling.  
- **Regex Crate**: Validated file lines with patterns like `^[A-Za-z][A-Za-z ]*;\s*([1-9]|50|[1-4][0-9])\s*(c|cents)$`.  
- **Error Handling**: Used `Option` types and early returns for invalid inputs.  
- **Memory Safety**: Modified strings in-place via mutable references (`&mut String`).  

**Grade:** 100/100 

---

### Project 7: ****
**Description:**  


**Grade:** 

---

## Disclaimer

**## CONTACT ME IF YOU WOULD LIKE TO SEE THE CODE, UNDER UNIVERSITY RULES I AM NOT ALLOWED TO POST PUBLICLY ON HERE**

If you are interested in reviewing the code or have any questions related to the projects, please reach out to me directly.
