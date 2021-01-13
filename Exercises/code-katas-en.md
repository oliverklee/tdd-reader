# Code katas

For these exercises, it is a requirement that you always use a test list and
that you work strictly test-first.

## Fun with words

### Character sorter
- level 1
- no dependencies

```
sort(string $text): string
"" => ""
"hello" => "ehllo"
It will also lowercase the text.
It does not matter where whitespace ends up after sorting.
UTF-8 umlauts need to not break.
```

### Word list reader
- level 1
- no dependencies

```
reads a list of words from a file and returns it as string[]
1 word per line
```

### Palindrome finder
- level 2
- requirements: Word list reader
- finds [palindromes](https://en.wikipedia.org/wiki/Palindrome)
- resource: [list of English words](https://github.com/dwyl/english-words)

```
1 script and (at least) 1 additional class
reads words from a file
from a list of words, finds all palindromes
examples: "anna", "noon", "reliefpfeiler"
ignores spaces
ignores the casing
echos all palindromes
```

### Anagram finder
- level 2
- requirements: Word list reader, Character sorter
- finds [anagrams](https://en.wikipedia.org/wiki/Anagram)
- resource: [list of English words](https://github.com/dwyl/english-words)

```
1 script and (at least) 1 additional class
reads words from a file
from a list of words, finds all anagram
examples: "neo"/"one", "tip"/"pit"
ignores spaces
ignores the casing
echos all anagrams
isAnagram(string $string1, string $string2): bool
run-time complexity must be better than O(n^2)
```

### PrefixFinder
- level 3 (extremely hard!)
- requirements: Word list reader
- data structure: [Prefix tree](https://en.wikipedia.org/wiki/Trie)
- resource: [list of English words](https://github.com/dwyl/english-words)

```
1 script and (at least) 1 additional class
reads words from a file
echos all words that are the prefix of another word, e.g., "pole(dance)"
run-time complexity must be better than O(n^2)
```

## Crunching numbers

### Duplicate finder
- level 1
- no dependencies

```
expects int[]
returns the numbers that occur at least two times
also test it with 1'000'000 random numbers
run-time complexity must be better than O(n^2)
```

### Prime finder
- level 1
- no dependencies
- algorithm: [the sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes)

```
returns whether an int is a prime
echos the first n prime numbers
manually test with n = 100
optional: use memoization
```

### Median
- level 1
- no dependencies
- resource: [definition of the median](https://en.wikipedia.org/wiki/Median)

```
returns the median of int[] (which also may include negative numbers)
needs to work both with an even and odd number of numbers
needs to deal correctly with duplicates
should also work with unsorted input
```

### One neighbour avoider
- level 2
- no dependencies

```
for a positive int n, returns as stringsall n-digit binary numbers that have no subsequent 1s
0 -> []
1 -> [0, 1]
2 -> [00, 01, 10]
3 -> [000, 001, 010, 100, 101]
4 -> …
```

### Roman numerals
- level 3 (extremely hard!)
- no dependencies
- resources:
  - [definition or roman numerals](https://en.wikipedia.org/wiki/Roman_numerals)
  - [explanation of the conversion](https://www.mathsisfun.com/roman-numerals.html)
  - [algorithm](http://blog.functionalfun.net/2009/01/project-euler-89-converting-to-and-from.html)

```
echos the numbers from 1 to 100 as roman numerals
can convert roman numerals to ints
```
