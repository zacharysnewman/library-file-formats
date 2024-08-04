# File Format Specifications

## 1. Unstructured Word List (.uwl) Specification

- **Extension:** `.uwl`
- **Description:** This file format contains a list of words, each separated by a newline character. Each line represents a single word.
- **Format:**
  - Each word is placed on a new line.
  - No additional characters or delimiters are used.
- **Example:**
  ```
  apple
  banana
  cherry
  ```

## 2. Whitespace and Punctuation List (.wpl) Specification

- **Extension:** `.wpl`
- **Description:** This file format contains combinations of punctuation and whitespace characters. Each combination is terminated by a "0" character and separated by a newline character.
- **Format:**
  - Each combination is a sequence of characters followed by "0".
  - Each combination is placed on a new line.
- **Example:**
  ```
  .0
  ,0
   0
  !0
  ```

## 3. Permutation Index List (.pil) Specification

- **Extension:** `.pil`
- **Description:** This file format contains hexadecimal numbers, each separated by a newline character.
- **Format:**
  - Each hexadecimal number is placed on a new line.
  - Hexadecimal numbers are in uppercase.
- **Example:**
  ```
  1A
  2B
  3C
  ```

## 4. Words Whitespace and Punctuation File (.wwp) Specification

- **Extension:** `.wwp`
- **Description:** This file format combines the contents of a `.uwl` file and a `.wpl` file. The word list and the whitespace/punctuation list are separated by a semicolon (`;`) with a newline before and after the semicolon.
- **Format:**
  - The file starts with the word list, following the `.uwl` format.
  - After the word list, a newline, a semicolon (`;`), and another newline are added.
  - The file then contains the whitespace and punctuation list, following the `.wpl` format.
- **Example:**
  ```
  apple
  banana
  cherry

  ; 

  .0
  ,0
   0
  !0
  ```

## 5. Complete Indexed Word List (.cil) Specification

- **Extension:** `.cil`
- **Description:** This file format combines the contents of `.pil`, `.uwl`, and `.wpl` files in that order. Each section is separated by a semicolon (`;`) with a newline before and after the semicolon.
- **Format:**
  - The file starts with the permutation index list, following the `.pil` format.
  - After the permutation index list, a newline, a semicolon (`;`), and another newline are added.
  - The file then contains the word list, following the `.uwl` format.
  - After the word list, a newline, a semicolon (`;`), and another newline are added.
  - The file ends with the whitespace and punctuation list, following the `.wpl` format.
- **Example:**
  ```
  1A
  2B
  3C

  ; 

  apple
  banana
  cherry

  ; 

  .0
  ,0
   0
  !0
  ```
