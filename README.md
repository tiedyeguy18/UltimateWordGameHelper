# UltimateWordGameHelper
A program that allows the user to specify a constraint string. The program generates words that abide by the specified constraints.

## Constraints:

### Constant Constraints:
- Words consist of only lowercase characters from a to z.
- The only words are those in english_wordlist.txt.

### Specifiable Constraints:
- Specifying any lowercase character from a to z specifies that the letter at that position must be the given letter.
- Specifying a positive integer makes a new wildcard that could be any lowercase letter. You must use square brackets to specify a number greater than 9. Wildcards that use the same number must correspond to the same letter.
- Specifying a "\*" means there can be zero or more letters a through z filling that space.
- Outside of the constraint string, you may also specify the letters available to make a word out of. They must be a subset of the lowercase English alphabet. An empty alphabet assumes the entire lowercase English alphabet

## Examples:

- alphabet: ""; constraints: "q\*d\*p\*"
  - quadruped
  - quadrupled
  - etc.
- alphabet: ""; constraints: "[1]end"
  - rend
  - mend
  - tend
  - send
  - etc.
- alphabet: ""; constraints: "h[1][2][2]o"
  - hello
  - hippo
  - etc.
- alphabet: "gnaroexuz"; constraints: "o\*"
  - orange
  - or
  - oar
  - ox
  - etc.
