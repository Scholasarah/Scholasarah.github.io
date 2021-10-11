---
Title: Beginner Python Project (5/12)
categories:
  - python
tags:
  - python
  - computer science
  - Hangman
---



# Beginner Python Projects (5/12)

**5. Hangman**

First, choose a random English word.

https://stackoverflow.com/questions/594273/how-to-pick-a-random-english-word-from-a-list 

![image-20211011141524111](/images/2021-10-11-pythonproject5/image-20211011141524111.png)



\# from **words**(words.py) import **words**(variables in words.py)



**Code 작성법**:

```python
import random
from words import words
import string

def get_valid_word(words):
    word = random.choice(words) # randomly chooses sth from the list
    while '-' in word or ' ' in word:
        word = random.choice(words)
    return word.upper()  # we're going to uppercase all the letters
# print(get_valid_word(words))

def hangman():
    word = get_valid_word(words)
    word_letters = set(word)  # letters in the word
    alphabet = set(string.ascii_uppercase)
    used_letters = set()      # what the user has guessed

    # getting user input
    while len(word_letters) > 0:
        # letters used
        # ' '.join(['a', 'b', 'cd']) --> 'a b cd'
        print('You have used these letters: ', ' '.join(used_letters))

        # what current word is (ie. W - R D)
        word_list = [letter if letter in used_letters else '-' for letter in word]
        print('Current word: ', ' '.join(word_list))

        user_letter = input('Guess a letter: ').upper()
        if user_letter in alphabet - used_letters:
            used_letters.add(user_letter)
            if user_letter in word_letters:
                word_letters.remove(user_letter)
        elif user_letter in used_letters:
            print('You have already used that character. Please try again.')
        else:
            print('Invalid character. Please try again.')
    # gets here when len(words_letters) == 0
    print('You guessed the word', word, '!!')

hangman()
```



![image-20211011141536744](/images/2021-10-11-pythonproject5/image-20211011141536744.png)





----------------------------------------------------------------------


**5-1. Hangman (with lives)**

Using the concept of **LIVES** in **Hangman**:



**Code 작성법**:

```python
import random
from words import words
import string

def get_valid_word(words):
    word = random.choice(words) # randomly chooses sth from the list
    while '-' in word or ' ' in word:
        word = random.choice(words)
    return word.upper()  # we're going to uppercase all the letters, so ths should be return word.upper()
# print(get_valid_word(words))

def hangman():
    word = get_valid_word(words)
    word_letters = set(word)  # letters in the word
    alphabet = set(string.ascii_uppercase)
    used_letters = set()      # what the user has guessed

    lives = 6
    # getting user input
    while len(word_letters) > 0 and lives > 0:
        # letters used
        # ' '.join(['a', 'b', 'cd']) --> 'a b cd'
        print('You have', lives, 'lives left and you have used these letters: ', ' '.join(used_letters))

        # what current word is (ie. W - R D)
        word_list = [letter if letter in used_letters else '-' for letter in word]
        print('Current word: ', ' '.join(word_list))

        user_letter = input('Guess a letter: ').upper()
        if user_letter in alphabet - used_letters:
            used_letters.add(user_letter)
            if user_letter in word_letters:
                word_letters.remove(user_letter)

            else:
                lives = lives - 1 # takes away a life if wrong
                print('Letter is not in word.')

        elif user_letter in used_letters:
            print('You have already used that character. Please try again.')
        else:
            print('Invalid character. Please try again.')
    # gets here when len(words_letters) == 0 OR when lives == 0
    if lives == 0:
        print('You died, sorry. The word was', word)
    else:
        print('You guessed the word', word, '!!')

hangman()
```



![image-20211011141557666](/images/2021-10-11-pythonproject5/image-20211011141557666.png)












* [12 Beginner Python Project - Coding Course](https://youtu.be/8ext9G7xspg)
  * 초급 Python 프로젝트-코딩 과정

-끝-

