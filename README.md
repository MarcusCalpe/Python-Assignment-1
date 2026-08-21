# ECE-2112-PA-1
Made by Marcus Nathan J. Calpe | 2ECE-D

This repository contains the source code for ECE2112 Practical Activity 1 (AY 2026–2027) with solutions to three introductory Python programming problems.

### 1. Word Rotation Problem: Create a function named rotate word() that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the capitalization of every character. 

The following method was used:
```python
def rotate_word(text):
    result = ""
```
The function `rotate_word(text)` starts initializing an empty variable named `result`. This acts as a storage for the text as the user inputs a string.
```python
for i in range(len(text)):
        result = text[i] + result
    return result
```
A `for loop` combined with `range()` and `len()` is used to iterate each character of the given input by its index `i`. Inside the loop, `text[i] + result` adds characters to the front of the stored result string. This approach reverses the sequence of characters without using built-in reversing functions.

### 2. Username Builder Problem Create a function named make username() that accepts two strings: first name and last name. The function must:
1. convert all letters to lowercase;
2. remove all spaces from the first name;
3. remove all spaces from the last name; and
4. join the processed first and last names using one period (.).

```python
def make_username(f, l):
    first_name = f.lower().replace(" ", "")
    last_name = l.lower().replace(" ", "")
```
The function above is accepting two arguments. Following the format, all letters must be lowercase, `.lower()` is applied to both instances to convert all characters to lowercase. It is followed by `.replace(" ". "")` to find and replace whitespaces, ensuring names are concatenated properly.
```python
result = first_name + "." + last_name
    return result
```
Once the inputs are prim, string concatenation `(+)` is used to join the `first_name` and `last_name` variables. A period is added in between them as per the instruction.

### 3. Bookend Swap Problem: Create a function named swap bookends() that accepts a list containing at least two elements. Unpack the list into three variables.
```python
def swap_bookends(items):
    first, *middle, last = items
```
In accordance with the requirement, `first`, `*middle`, and `last` was used iterate the items into their respective position; first item of the list into the `first` variable and the last item of the list into the `last` variable. The remaining items were stored in the `*middle` sub-list.
```python
return [last] + middle + [first]
```
To achieve the swapping of positions, the lists is constructed using concatenation. The `last` and `first` variables were enclosed in a bracket to form a list. 

Thank you for reading!

To see the main Python program for Programming Assignment 1, click this link: [https://github.com/MarcusCalpe/Python-Assignment-1/blob/main/Python%20Assignment.ipynb](https://github.com/MarcusCalpe/Python-Assignment-1/blob/main/Python%20Assignment.ipynb) and download it, open it in Jupyter Notebook, then run all cells.

#### README file Version History:
August 20, 2026 - Initial README output created

August 21, 2026 - Format in README content was updated
