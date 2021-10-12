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

Link: [[How to pick a random english word from a list]](https://stackoverflow.com/questions/594273/how-to-pick-a-random-english-word-from-a-list)

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



​	alphabet = 알파벳.대문자

​	used_letters = set()  #user가 guess한 letter

​	user_letter = user가 작성한 letter

![image-20211012185246532](/images/2021-10-11-pythonproject5/image-20211012185246532.png)

**if user_letter in alphabet - used_letters:**

​				**used_letters.add(user_letter)**

→ if this is a valid character in the alphabet that I haven’t used yet, i will add the (user_letter) to (used_letters) set.

**if user_letter in word_letters:**

​				**word_letters.remove(user_letter)**

→ if the letter I have just guessed is in the word, I will remove that letter from (word_letters).



```python
word_list = [letter if letter in used_letters else '-' for letter in word]
print('Current word: ', ' '.join(word_list))
```

**[letter if letter in used_letters else '-' for letter in word]란 무엇일까?**

> > **List Comprehension** 기본 문법

```python
size = 10
arr = [0] * size
for i in range(len(size)):
    arr[i] = i * 2
```

(설명)

size = 10

arr = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]

```python
for i in range(len(size)):
    arr[i] = i * 2
```

→ i = o,

[0, 0, 0, 0, 0, 0, 0, 0, 0, 0]

→ i = 1,

[0, 2, 0, 0, 0, 0, 0, 0, 0, 0]

→ i = 2,

[0, 2, 4, 0, 0, 0, 0, 0, 0, 0]

...

→ i = 9,

[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]



위에 표현한 3 line이 아래의 하나의 line으로 표현할 수 있음:

```python
size = 10
arr = [i * 2 for i in range(size)]

print(arr)
```

<u>[ (변수를 활용한 값) **for** (사용할 변수 이름) **in** (순회할 수 있는 값) ]</u>

출처: [[Python] list comprehension에 대한 즐거운 이해](https://shoark7.github.io/programming/python/about-list-comprehension-python) 





> > 정리해보면, **[letter if letter in used_letters else '-' for letter in word]**는 

```python
word_list = [letter if letter in used_letters else '-' for letter in word]
print('Current word: ', ' '.join(word_list))
```

만약, word = ABC,

[ (letter if letter in used_letters else '-') **for** (A, B, C) **in** (ABC) ]

→ ABC 단어에서 A, B, C의 letter (변수)가

used_letters에 있으면 그 letter를 쓰고,

없다면, ' - '로 표현.



![image-20211011141536744](/images/2021-10-11-pythonproject5/image-20211011141536744.png)





----------------------------------------------------------------------




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

