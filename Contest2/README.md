# Contest Two

## Contest Two covers the following topics
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
  - Basic Functions (SET, SETQ, EVAL, ATOM)
  - List Functions (CAR, CDR, CONS, REVERSE)
  - Arithmetic Functions (ADD, MULT, ...)
  
  
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
  1. (((A + B) ^ (2/3)) + (((A / 2) – B) / 3))
  2. ((^ (+ A B) (/ 2 3)) + (((A / 2) – B) / 3))
  3. (((A B +) (2 3 /) ^) + (((A 2 /) B –) 3 /))
  4. (((A B +) (2 3 /) ^) (((A 2 /) B –) 3 /) +)
  5. A B + 2 3 / ^ A 2 / B - 3 / +
  6. ANSWER: A B + 2 3 / ^ A 2 / B - 3 / +
  
  ```
  4) Infix to Prefix
  ```
  GIVEN: (s * (s – a) * (s – b) * (s – c)) ^ (1/2)
  1. (^ (s * (s – a) * (s – b) * (s – c)) (1/2))
  2. (^ (s * (– s a) * (– s b) * (– s c)) (/ 1 2))
  3. (^ ((* s (– s a)) * (– s b) * (– s c)) (/ 1 2))
  4. (^ (* (* ((* s (– s a)) (– s b)) (– s c))) (/ 1 2))
  5. ^ * * * s - s a - s b - s c / 1 2
  ANSWER: ^ * * * s - s a - s b - s c / 1 2
  ```
  
  ## Bit Flickering
  Bit Strings (strings of binary digits) can be modified by logical operators such as NOT, AND, OR, and XOR. Furthermore, they can be manipulated by as a unit using SHIFT and circulate operators. The bit furthest to the left is called the most significant bit and the bit furthest to the right is called least significant bit.
  
  ### Evaluate 
  1) A2716 XOR 4E216
  The two arguments are hexadecimal numbers representing bit strings that are 12 bits long.
Express your answer as a 3-digit hexadecimal string.
  ```
  GIVEN: A27 XOR 4E2
  1. 1010 0010 0111 XOR 0100 1110 0010
  2. 1110 1100 0101 
  3. E C 5
  ANSWER: EC5
  ```
  2) (RSHIFT-2 (RCIRC-8 (RSHIFT-2 10011)))
  ```
  GIVEN: (RSHIFT-2 (RCIRC-8 (RSHIFT-2 10011)))
  1. (RSHIFT-2 (RCIRC-8 (00100)))
  2. (RSHIFT-2 (RCIRC-8 (00100)))
  3. (RSHIFT-2 (10000))
  4. 00100
  ANSWER: 00100
  ```
  3) (LCIRC-2 (RSHIFT-1 01101)) OR (NOT (RCIRC-2 (LSHIFT-1 01010)))
  ```
  GIVEN: (LCIRC-2 (RSHIFT-1 01101)) OR (NOT (RCIRC-2 (LSHIFT-1 01010)))
  1.  (LCIRC-2 (00110)) OR (NOT (RCIRC-2 (10100)))
  2.  (11000) OR (NOT (00101))
  3.  (11000) OR (11010)
  4.  11010
  ```
  
  ### List all Possible Values 
  1) How many values of X (5 bits long) satisfy the following equation?
  ```
  GIVEN: (RSHIFT-1 X ) OR 10110 AND 00101 = 00101
  1. (RSHIFT-1 abcde) OR 10110 AND 00101 = 00101
  2. 0abcd OR 10110 AND 00101 = 00101
  3. 0abcd OR 00100 = 00101
  4. 0a1cd = 00101
  5. a = 0, c = 0, d = 1
  6. 0*01* (back to abcde format)
  ANSWER: 0*01* 
  ```
  2) List all the values of X ( a 5-bit string) that make the following expression TRUE
  ```
  GIVEN: (LSHIFT-2 (RCIRC-1 (NOT X))) = 10000 
  1. (LSHIFT-2 (RCIRC-1 (NOT abcde))) = 10000 
  2. (LSHIFT-2 (RCIRC-1 (ABCDE))) = 10000 
  3. (LSHIFT-2 (EABCD)) = 10000 
  4. (BCD00) = 10000 
  5. B = 1, C = 0, D = 0
  6. b = 0, c = 1, d = 1
  7. *011* (back to abcde format)
  ANSWER: *011*
  ```
  3) List all possible values of X (5 bits long) that solve the following equation
  ```
  GIVEN: (LCIRC-3 (RSHIFT-2 01110)) OR (RCIRC-2 X) = 11011
  1. (LCIRC-3 (00011)) OR (RCIRC-2 abcde) = 11011
  2. (11000) OR (edabc) = 11011
  3. 11abc = 11011
  4. a = 0, b = 1, c = 1
  5. 011** (back to abcde format)
  ANSWER: 011**
  ```
  
  ## LISP
  During the mid 1950s a programming language called LISP ("LISt Processing language") was developed by John McCarthy at MIT. LISP provides simple structure and semantics that allow it to be one of the most powerful and simplest programming language. Its unconventional structure and simplicity allow programmers to take a break from commonly used algorithmic langauges (Java, C, C++, etc).
  
  ### Basic Functions
  1) Problem 1
  ```
  GIVEN: 
  (SETQ X '(RI VA FL CA TX))
  (CAR (CDR (REVERSE X)))
  What is the value of X?
  ```
  2) Overview 1
  ```
  (SETQ p '(ADD 1 2 3 4))	(ADD 1 2 3 4)	p is a list with 5 elements
  (ATOM 'p)	true	The argument to ATOM is the atom p
  (ATOM p)	NIL	Because p is not quoted, it is evaluated to the 5-element list.
  (EVAL p)	10	The argument to EVAL is the value of p; the value of p is 10.
  ```
  3) Overview 2
  ```
  (SET 'a (MULT 2 3))	6	a is an atom with a value of 6
  (SET 'a '(MULT 2 3))	(MULT 2 3)	a is a list with 3 elements
  (SET 'b 'a)	a	b is an atom with a value of the character a
  (SET 'c a)	(MULT 2 3)	c is a list with 3 elements
  (SETQ EX (ADD 3 (MULT 2 5)))	13	The variable EX has a value of 13
  (SETQ VOWELS '(A E I O U))	(A E I O U)	VOWELS is a list of 5 elements
  ```
  
  ### List Functions
  1) (CDR (CAR (CDR ‘((b c) (a d f) (d)))))
  ```
  ```
  2) (CAR (CAR (CDR (CDR ‘(a (b c) (a (b c))))))
  ```
  ```
  3) (CAR (CAR (CDR (CDR (CDR ‘(1 (2 3) 4 ((5 6) (7 8) 9))))))) 
  ```
  ```
  4)(CDR (CAR (CDR (CAR ‘((b (c d) (e f g)) (h (j k)))))))
  ```
  ```
  ### Arithmetic Functions
  1) (ADD (SUB 4 5) (ADD 6 3) (MULT 4 8))
  ```
  GIVEN: (ADD (SUB 4 5) (ADD 6 3) (MULT 4 8))
  ```
  2) (DIV (MULT (ADD 1 4 5) (SUB 7 2)) (EXP 5 2)) 
  ```
  GIVEN: (DIV (MULT (ADD 1 4 5) (SUB 7 2)) (EXP 5 2)) 
  ```
  3) (MULT (ADD 2 3 1 (EXP 3 2)) (SUB (MULT 4 2) (DIV 10 2)))
  ```
  GIVEN: (MULT (ADD 2 3 1 (EXP 3 2)) (SUB (MULT 4 2) (DIV 10 2)))
  ```
  
  ## Programming Problems
  
  ### Examples
