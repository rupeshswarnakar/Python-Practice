# Python-Practice

## Q.1 
```
String Cleaning & Transformation
Write a Python function that takes a sentence and performs the following:
●	Removes all vowels (a, e, i, o, u)

●	Replaces spaces with underscores _

●	Converts it to title case (first letter of each word capitalized)

Example:
Input:  "data engineering rocks"
Output: "Dt_Engnrng_Rcks"
```

## Answer 1:
```
words = "data engineering rocks"
vowels = ["a", "e", "i", "o", "u"]

# replacing spaces with "_"
words = words.replace(" ", "_")

# filtering vowels from given words
new = []
for ch in words:
    if ch not in vowels:
       new.append(ch)

result = " ".join(new)

# Capitalizing first letter of each word
split_words = result.split("_")

new_list = []
for ch in split_words:
    first = ch[0].upper()
    rest = ch[1:]
    new_ch = first + rest
    new_list.append(new_ch)

final = "_".join(new_list)
print(final)
```

## Q.2
```
Dictionary Aggregation
Given a list of dictionaries representing sales transactions:
sales = [
  {"product": "Pen", "amount": 10},
  {"product": "Book", "amount": 20},
  {"product": "Pen", "amount": 15},
  {"product": "Pencil", "amount": 5}
]

Write a Python program to calculate total sales per product and print the result as:
Pen: 25
Book: 20
Pencil: 5
```

## Answer 2:
```
total = {}

for sale in sales:
    product = sale["product"]
    amount = sale["amount"]
    if product not in total:
        total[product] = amount
    else:
        total[product] += amount

print(total)
```

## Q.3
```
Write a Python function that takes a list of integers and returns a new list containing elements that appear exactly once.
Example:
Input: [4, 5, 4, 6, 7, 5, 8]
Output: [6, 7, 8]
```

## Answer 3:
```
List = []

for num in numbers:
    if num not in List:
        List.append(num)
    elif num in List:
        List.remove(num)

print(List)
```
## Q.4:
```
Write a Python function to reverse a given string.
Input: "hello"
Output: "olleh"
```

## Answer 4:
```
list = []

for i in range(len(Input)-1, -1, -1):
    list.append(Input[i])

result = ''.join(list)
print(result)
```
## Q.5:
```
Write a Python function to check if two given strings are anagrams of each other.
Input: "listen", "silent"
Output: True
```

## Solution 5:
```
word1 = sorted(word[0]
word2 = sorted(word[1]
if word1 == word2:
    print("True")
else:
    print("False")
```

## Q.6:
```
Write a Python function to remove all duplicate characters in a given string while preserving the order of the remaining characters.
Input: "programming"
Output: "progamin"
```

## Solution 6:
```
bucket= []
for ch in Input:
    if ch not in bucket:
        bucket.append(ch)

result = ''.join(bucket)
print(result)
```
## Q.7:
```
Hospital system logs patient visits. You are given a list of patient IDs.

a. Return the top 2 most frequent patients
b. Sorted by frequency (highest first)
c. If tie → sort by patient_id alphabetically

Example
visits = [
    "P101", "P102", "P101",
    "P103", "P102", "P102",
    "P104", "P101"
]

Expected Output:
[("P101", 3), ("P102", 3)]
```

## Solution 7:
```
freq = {}

for visit in visits:
	if visit not in freq:
		freq[visit] = 1
	else:
		freq[visit] += 1

result = sorted(freq.items(), key=lambda x:(-x[1], x[0]))
print(result[0:2])
```
## Q.8:
```
Find the First Non-Repeating Character
Write a Python function to find the first non-repeating character in a given string and return its index.
Input: "swiss"
Output: 1 (for 'w' in "swiss")
```

## Solution 8:
```
s = "swiss"
freq = {}

for ch in s:
    if ch not in freq:
        freq[ch] = 1
    elif ch in freq:
        freq[ch] += 1

for i, ch in enumerate(s):
    if freq[ch] == 1:
        print(i)
        break
```










































