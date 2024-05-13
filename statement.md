# PYTHON: Pig Latin Program

I am going to show the solution code for my clash of code: "Igpay Latin". It is suitable for use in any Pig Latin case.

## Program: Pig Latin
In this program we will:
1. Get an input sentence from the user and create a variable string.
2. Define a function that implements "Pig-Latin" on a string.
3. Parse through the sentence and add each word to an array.
4. Iterate through each word in the array and use the function on that word.
5. Output the resulting string, now in pig-latin and in lowercase, and end the program.

Let's do this:
```python runnable

def PigLatin(string):
    vowels = ['a', 'e', 'i', 'o', 'u']
    if string[0].lower() in vowels:
        return string + "yay"
    else:
        for i in range(len(string)):
            if string[i].lower() in vowels:
                return string[i:].lower() + string[:i].lower() + "ay"


sentence = str(input("Enter a string: ")).split(" ")
answer = ""

for word in sentence:
    answer+=PigLatin(word)+" "

print(answer.strip().lower())
```

This program will work for single-word strings or mulitple-word strings.

Please feel free to use it or to modify it to suit your needs.

Here are two links for those who'd want to read about Pig Latin:

https://www.dictionary.com/e/pig-latin

https://en.wikipedia.org/wiki/Pig_Latin

Happy Coding,
@Code-Parser