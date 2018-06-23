# Code katas

## Fun with words

### Character sorter
- level 1
- no dependencies

```
sort(string $text): string
"hello" => "ehllo"
hello world" => "dehllloorw "
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
