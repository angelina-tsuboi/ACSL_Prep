# Contest Two

## Contest One covers the following topics
  - Infix, Postfix, Prefix
  - Bit Flickering
  - LISP
  - Programming Problems

## Infix, Postfix, Prefix

### Problems inside this Section Includes:
  - Infix to Postfix
  - Infix to Prefix 
  - Postfix to Infix
  - Prefix to Infix
  
  
## Bit Flickering

### Problems inside this Section Includes:
  - Bitwise Operators
  - Shift Operators
  - Order of Precedence
  
## LISP

### Problems inside this Section Includes:
  - 
  - 
  
  
## Programming Problems

### Problems inside this Section Includes:
  - Depends on the Competition...
  
  
# Practice Problems
  
  ## Infix, Postfix, Prefix
  Normally we see mathematical expressions written with the operator acting between the operands (ie. 2 + 2, 15 / 3, 3 * (x - 4), etc). This convention is called infix notation where a operator(p) acts between the surrounding operands (d) -> d p d. Prefix notation is when the operator comes before its two operands p d d (ie. / 4 2, * 8 6, - 9 (+ x 4), etc). Lastly a postfix expression occurs when the operator comes after the two operands d d p (ie. 4 2 /, 8 6 *, 9 (x 4 +) -, etc). Below are examples on how to convert between the notations...
  
  ### Evaluating Expressions
  1) Evaluate the prefix expression 
  ```
 GIVEN: / / * 2 + 4 6 5 - ^ 3 2 5
 1. / / * 2 (10) 5 - ^ 3 2 5
 2. / / (20) 5 - ^ 3 2 5
 3. / / (20) 5 - 9 5
 4. / 4 4
 5.  1
 ANSWER: 1
  ```
  2) Evaluate the postfix expression 
  ```
 GIVEN: 8 4 / 6 2 ^ + 2 + 2 3 ^ /
 1. 2 (36) + 2 + 23 ^ / 
 2. 2 (36) + 2 + 8 /
 3. (38) 2 + 8 /
 4. 40 8 /
 5. 5
 ANSWER: 5
  ```
  3) Evaluate the prefix expression
  A = 3 and B = 2 
  ```
 GIVEN: / - ^ ^ A 2 2 ^ ^ B 2 2 * - ^ A 2 ^ B 2 + ^ A 2 ^ B 2
 1. / - ^ ^ 3 2 2 ^ ^ 2 2 2 * - ^ 3 2 ^ 2 2 + ^ 3 2 ^ 2 2
 2. / - ^ 9 2 ^ 4 2 * - 9 4 + 9 4
 3. / - (81) (16) * 5 (13)
 4. / 65 65
 5. 1
 ANSWER: 1
  ```
  4) Evaluate the postfix expression 
 The new binary operation @ is defined as follows: A @ B = sqrt ((A ^ 2) + (B ^ 2))
 Note that all numbers are single digit
  ```
 GIVEN: 3 2 ^ 2 3 * - 2 2 ^ @ 8 2 – 6 3 / * @
 1. 9 2 3 * - 2 2 ^ @ 8 2 - 6 3 / * @
 2. 9 6 - 4 @ 8 2 - 2 * @
 3. 3 4 @ 6 2 * @
 4. 5 6 2 * @
 5. 5 (12) @
 6. 13
 ANSWER: 13
  ```
 
  
  ### Conversion between Expressions (ie. Infix -> Prefix, Postfix -> Prefix)
  1) Infix to Prefix
   ```
   GIVEN: AX2 + BX + C = 0
   1: ((AX2 + BX + C) = 0)
   2: (((A * (X ^ 2)) + (B * X) + C) = 0)
   3: (((A * (^ X 2)) + (* B X) + C) = 0)
   4: (((* A (^ X 2)) + (* B X) + C) = 0)
   5: ((+ (* A (^ X 2)) (* B X) + C) = 0)
   6: ((+ + (* A (^ X 2)) (* B X) C) = 0)
   7: (= (+ + (* A (^ X 2)) (* B X) C) 0)
   8: = + + * A ^ X 2 * B X C 0
   ANSWER: = + + * A ^ X 2 * B X C 0
  ```
  2) Postfix to Prefix
   ```
  GIVEN: A A B + C A B / - / * 
  1. A (+ A B) C (/ A B) - / *
  2. A (+ A B) (- C (/ A B)) / *
  3. A (/ (+ A B) (- C (/ A B))) *
  4. (* A (/ (+ A B) (- C (/ A B))))
  5. * A / + A B - C / A B
  ANSWER: * A / + A B - C / A B
  ```
  3) Infix to Postfix
  ```
  GIVEN: (A + B) ^ (2/3) + (A / 2 – B) / 3
  
  ```
  4) Infix to Prefix
  ```
  GIVEN: (s * (s – a) * (s – b) * (s – c)) ^ (1/2)
  
  ```
  
  ## Bit Flickering
  
  
  ### Examples
  
  ## LISP
  
  ### Examples
  
  ## Programming Problems
  
  ### Examples
