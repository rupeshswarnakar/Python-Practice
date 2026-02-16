# Python-Practice

Q.1 
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

Answer 1:
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

Q.2
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

Answer 2:
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

Q.3
```
Write a Python function that takes a list of integers and returns a new list containing elements that appear exactly once.
Example:
Input: [4, 5, 4, 6, 7, 5, 8]
Output: [6, 7, 8]
```

Answer 3:
```
List = []

for num in numbers:
    if num not in List:
        List.append(num)
    elif num in List:
        List.remove(num)

print(List)
```






