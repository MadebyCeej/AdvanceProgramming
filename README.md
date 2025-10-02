# Python Input-Based Problems

This repository contains three Python programs that demonstrate fundamental concepts such as user input, string manipulation, and list operations.

---

## Problems Covered

### 1. Alphabet Soup

**Instruction:**  
Create a function that takes a string and returns a string with its letters in alphabetical order.  

**Example:**
```
Enter a word: hello
Alphabetical order: ehllo
```

---

### 2. Emoticon Converter

**Instruction:**  
Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words **smile, grin, sad,** and **mad** with their corresponding emoticon.  

**Example:**
```
Enter a sentence: I am Sad but I Smile
Converted sentence: I am :(( but I :)
```

---

### 3. Unpacking List

**Instruction:**  
Unpack the list into three variables: first, middle, and last. `first` is the first element, `last` is the last element, and `middle` is everything in between.  

**Example:**
```
Enter numbers separated by spaces: 1 2 3 4 5 6
First: 1
Middle: [2, 3, 4, 5]
Last: 6
```

---

## How to Run

1. Ensure you have Python installed on your system.  
2. Clone this repository or download the individual Python files.  
3. Open a terminal or command prompt.  
4. Run any of the Python files using:  
```bash
python filename.py
```

For example:  
```bash
python alphabet_soup.py
```

---

# Codes with Explanations

## Alphabet Soup Problem
```python
def alphabet_soup(word: str) -> str:
    # SORT THE WORD ALPHABETICALLY
    return ''.join(sorted(word)) 

# USER'S INPUT
user_word = input("Enter a word: ")
print("Alphabetical order:", alphabet_soup(user_word))
```
- The function sorts characters in a word alphabetically.  
- The user enters a word, and the program prints it in alphabetical order.  

---

## Emoticon Converter Problem
```python
def emotify(sentence: str) -> str:
    # REPLACE EACH WORD WITH EMOTICONS (CASE-SENSITIVE HANDLING)
    sentence = sentence.replace("Smile", ":)").replace("smile", ":)")
    sentence = sentence.replace("Grin", ":D").replace("grin", ":D")
    sentence = sentence.replace("Sad", ":((").replace("sad", ":((")
    sentence = sentence.replace("Mad", ">:(").replace("mad", ">:(")
    return sentence

# USER'S INPUT
user_sentence = input("Enter a sentence: ")
print("Converted sentence:", emotify(user_sentence))
```
- The function replaces certain words with matching emoticons.  
- Works for both uppercase and lowercase.  

---

## Unpacking List Problem
```python
# USER'S INPUT (SPACE-SEPARATED NUMBERS)
numbers = input("Enter numbers separated by spaces: ").split()
# CONVERT EACH INPUT STRING TO AN INTEGER
lst = [int(x) for x in numbers]

# PRINT FIRST, MIDDLE, LAST ELEMENTS
print("First:", lst[0])
print("Middle:", lst[1:-1])
print("Last:", lst[-1])
```
- The program splits the input into integers.  
- Prints the first element, all middle elements, and the last element separately.  
