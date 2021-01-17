# Contest One

## Contest One covers the following topics
  - Computer Number Systems
  - Recursive Functions
  - What Does this Program Do?
  - Programming Problems

## Computer Number Systems

### Problems inside this Section Includes:
  - Binary Conversion
  - Octal Conversion
  - Decimal Conversion
  - Hexadecimal Conversion
  - Binary Addition
  - Octal Addition
  - Decimal Addition
  - Hexadecimal Addition
  - Operations Including all systems
  
  
## Recursive Functions

### Problems inside this Section Includes:
  - Simple Recursion (One Input, Few Conditions)
  - Intermediate Recursion (One Input, Multiple Conditions)
  - Advanced Recursion (Few Inputs, Multiple Conditions)
  
## What Does this Program Do?

### Problems inside this Section Includes:
  - Finding the Outputed Value of Arbitrary Computer Programs
    - Easy
    - Intermediate
    - Hard
  
  
## Programming Problems

### Problems inside this Section Includes:
  - Depends on the Competition...
  
  
# Practice Problems
  
  ## Computer Number Systems
  
  ### Binary Conversion
  1) Binary to Octal
  ```
  101 -> 101 -> (4 + 1) -> 5
         421
  ```
  ```
  101111 -> 101 111 -> (4 + 1) + (4 + 2 + 1) -> 57
            421 421
  ```
  ```
  1010110111 -> 1 010 110 111 -> (1) + (2) + (4 + 2) + (4 + 2 + 1) -> 1267
                1 421 421 421
  ```
  
  2) Binary to Decimal
  ```
  110 -> 110 -> (1 * 4) + (1 * 2) + (0 * 0) -> 4 + 2 + 0 -> 6
         210
  ```
  ```
  1001 -> 1001 -> (1 * 8) + (0 * 4) + (0 * 2) + (1 * 1) -> 8 + 0 + 0 + 1 -> 9
          3210
  ```
  ```
  100101 -> 100101 -> (1 * 32) + (0 * 16) + (0 * 8) + (1 * 4) + (0 * 2) + (1 * 1) -> 32 + 4 + 1 -> 37
            543210
  ```
  ```
  110100101 -> 110100101 -> (1 * 256) + (1 * 128) + (0 * 64) + (1 * 32) + (0 * 16) + (0 * 8) + (1 * 4) + (0 * 2) + (1 * 1) -> 256 + 128 + 32 + 4 + 1 -> 421
               876543210
  ```
  3) Binary to Hexadecimal
  ```
  110 -> 110 -> (4 * 1) + (2 * 1) -> 6
         421
  
  ```
  ```
  101011 -> 10 1011 -> (2) (8 + 2 + 1 -> 11 -> B) -> 2B
            21 8421
  ```
  ```
  111011011 -> 1 1101 1011 -> (1) (8 + 4 + 1 -> 13 -> D) (8 + 2 + 1 -> B) -> 1DB
               1 8421 8421
  ```
   ```
  101101110101 -> 1011 0111 0101 -> (8 + 2 + 1 -> 11 -> B) (4 + 2 + 1 -> 7) (4 + 1 -> 5) -> B75
                  8421 8421 8421
  ```
  
  ### Octal Conversion
  1) Octal to Binary
   ```
  46 -> 4 6 -> (100) -> (110) -> 100110
               421       421
  ```
   ```
  6127 -> 6 1 2 7 -> (110) (001) (010) (111) -> 110001010111 
                      421   421   421   421
  ```
   ```
  1254323 -> 1 2 5 4 3 2 3 -> (001) (010) (101) (100) (011) (010) (011) -> 1010101100011010011 
                  
  ```
 2) Octal to Decimal
  ```
  10 -> 10 -> (8 * 1) + (0 * 1) -> 8
        10     
  ```
  ```
  4327 -> 4327 -> (4 * 512) + (3 * 64) + (2 * 8) + (7 * 1) -> 2263
          3210            
  ```
  ```
  156.52 -> 156.52 -> (1 * 64) + (5 * 8) + (6 * 1) + (5 * 1/8) + (2 * 1/64) -> 64 + 40 + 6 + 5/8 + 1/32 -> 110 + 21/32 -> 110 21/32
            210-1-2      
  ```
  3) Octal to Hexadecimal
 ```
  16 -> 1 6 -> 001 110 -> 00 1110 -> 1110 = 14 -> E
               421 421
  ```
   ```
  742 -> 7 4 2 -> 111 100 010 -> 1 1110 0010 -> 1 14 2 -> 1E2
                  421 421 421   
  ```
   ```
  26431 -> 2 6 4 3 1 -> 010 110 100 011 001 -> 010 1101 0001 1001 -> 2 13 1 9 -> 2D19 
                  
  ```
  
  ### Decimal Conversion
  1) Decimal to Binary
  ```
                            32 16 8 4 2 1 
  24 -> 24 - 16 - 8 = 0 ->  0  1 1 0 0 0 -> 11000
  ```
  ```
                                           128 64 32 16 8 4 2 1
  167 -> 167 - 128 - 32 - 4 - 2 - 1 = 0 ->  1  0  1  0  0 1 1 1 -> 10100111
  ```
  ```
                                                  512 256 128 64 32 16 8 4 2 1
  876 -> 876 - 512 - 256 - 64 - 32 - 8 - 4 = 0 ->  1  1 0  1  1  0  1 1 0 0 -> 1101101100
  ```
  2) Decimal to Octal
  ```
  78 -> 78 / 8 = 9.75 -> 9 R (.75 * 8 = 6) -> 9 / 8 = 1.125 -> 1 R (.125 * 8 = 1) -> 1 / 8 = (0.125 * 8 = 1) -> 116
  ```
  ```
  394 -> 394 / 8 = 49.25 -> 49 R 2 -> 49 / 8 = 6.125 -> 6 R 1 -> 6 / 8 -> .75 = 6 -> 612
  ```
  ```
  4157 -> 4157 / 8 = 519.625 -> 519 R 5 -> 519 / 8 = 64.875 -> 64 R 7 -> 64 / 8 = 8 R 0 -> 8 / 8 = 1 R 0 -> 1 / 8 = 0 R 1 -> 10075
  ```
  3) Decimal to Hexadecimal
  ```
  51 -> 51 / 16 -> 3.1875 = 3 R (.1875 * 16 = 3) -> 3 / 16 -> 0.1875 * 16 = 3 -> 33
  ```
  ```
  293 -> 293 / 16 -> 18.3125 -> 18 R 5 -> 18 / 16 -> 1 R 2 -> 2 / 16 = 1 -> 125
  ```
  ```
  8210 -> 8210 / 16 -> 512.125 -> 512 R 2 -> 512 / 16 = 32 R 1 -> 32 / 16 = 2 R 0 -> 2 / 16 = 2 -> 2012
  ```
  
  ### Hexadecimal Conversion
  1) Hexadecimal to Binary
  2) Hexadecimal to Octal
  3) Hexadecimal to Decimal
  
  ## Recursive Functions
  
  ### Examples
  
  ## What Does this Program Do?
  
  ### Examples
  
  ## Programming Problems
  
  ### Examples
