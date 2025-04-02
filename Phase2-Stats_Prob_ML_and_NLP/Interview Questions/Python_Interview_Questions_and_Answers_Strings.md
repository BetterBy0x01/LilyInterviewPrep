# Python Interview Questions and Answers - Strings 2025

## 1. Python program to remove characters from a string


<details><summary><b>Hint</b></summary>
<p>

> **Input** - Python
>
> **Input Character** - o
>
> **Output** - Pythn

</p>
</details>

```python
str = "Python"
ch = "o"
print(str.replace(ch," ")) 

>> Pyth n

```

---

## 2. Python Program to count occurrence of characters in string

<details><summary><b>Hint</b></summary>
<p>

> **Input** - Python
>
> **Input Character** - o
>
> **Output** - 1

</p>
</details>

```python
string = "Python"
char = "y"
count = 0
for i in range(len(string)):
    if(string[i] == char):
        count = count + 1
print(count)

>> 1

```
---

## 3. Python program in to check string is anagrams or not

<details><summary><b>Hint</b></summary>
<p>

> Input - Python
>
> Input Character - onypth
>
> Output - Anagrams
    
</p>
</details>

```python
str1 = "python"
str2 = "yonthp"
if (sorted(str1) == sorted(str2)):
    print("Anagram")
else:
    print("Not an anagram")
    
> Anagram

```

---

## 4. Python program to check string is palindrome or not

<details><summary><b>Hint</b></summary>
<p>

> Input - madam
>
> Output - Palindrome
    
</p>
</details>

```python
string = "madam"
if(string == string[:: - 1]):
   print("Palindrome")
else:
   print("Not a Palindrome") 

> Palindrome

```
---

## 5. Python code to check given character is digit or not

<details><summary><b>Hint</b></summary>
<p>

> Input - a
>
> Output - Not a Digit
    
</p>
</details>

```python
ch = 'a'
if ch >= '0' and ch <= '9': 
    	print("Digit")
else: 
    print("Not a Digit")
    
> Not a Digit


```
---

## 6. Program to replace the string space with any given character

<details><summary><b>Hint</b></summary>
<p>

> Input - m m
>    
> Input charcter - a
>
> Output - mam
    
</p>
</details>

```python
string = "m d m"
result = '' 
ch = "a"
for i in string:  
        if i == ' ':  
            i = ch   
        result += i  
print(result)
    
> madam

```

---

## 7. Check if Two Strings are Permutations of Each Other

```python
def are_permutations(s1: str, s2: str) -> bool:
    if len(s1) != len(s2):
        return False
    return sorted(s1) == sorted(s2)

# Example usage:
print(are_permutations("abc", "cab")) 

> True

```

---

## 8. Find All Permutations of a Given String

```python
from itertools import permutations

def string_permutations(s: str) -> list:
    return [''.join(p) for p in permutations(s)]

# Example usage:
print(string_permutations("ABC"))

> ['abc', 'acb', 'bac', 'bca', 'cab', 'cba']

```
---

## 9. Find the Longest Palindromic Substring

```python
def longest_palindromic_substring(s: str) -> str:
    def expand_around_center(left: int, right: int) -> str:
        while left >= 0 and right < len(s) and s[left] == s[right]:
            left -= 1
            right += 1
        return s[left+1:right]
    
    longest = ""
    for i in range(len(s)):
        # Odd length palindrome
        substr1 = expand_around_center(i, i)
        # Even length palindrome
        substr2 = expand_around_center(i, i + 1)
        longest = max(longest, substr1, substr2, key=len)
    return longest

# Example usage:
print(longest_palindromic_substring("babad"))

> "bab" or "aba"

```
---

## 10. Count and Group Anagrams from a List of Strings

```python

from collections import defaultdict

def group_anagrams(words: list) -> dict:
    anagrams = defaultdict(list)
    for word in words:
        sorted_word = ''.join(sorted(word))
        anagrams[sorted_word].append(word)
    return dict(anagrams)

# Example usage:
print(group_anagrams(["eat", "tea", "tan", "ate", "nat", "bat"]))

> {'aet': ['eat', 'tea', 'ate'], 'ant': ['tan', 'nat'], 'abt': ['bat']}

```

