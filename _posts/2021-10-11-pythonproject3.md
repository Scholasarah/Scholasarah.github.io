---
Title: Beginner Python Project (3/12)
categories:
  - python
tags:
  - python
  - computer science
  - Guessing number
---



# Beginner Python Projects (3/12)

**3. Guess the Number (User)**



```python
import random

def computer_guess(x):
    low = 1
    high = x
    feedback = ''
    while feedback != 'c':
        if low != high:
            guess = random.randint(low, high)
            print('guess by computer', guess)
        else:
            guess = low # could also be high b/c low = high
        feedback = input(f'Is {guess} too high (H), too low (L), or correct (C)?? ').lower()
        if feedback == 'h':
            high = guess - 1
        elif feedback == 'l':
            low = guess + 1
        print('------------- while')
    print(f'Yay! The computer guessed your number, {guess}, correctly!')

computer_guess(10)
```



![image-20211011140048890](/images/2021-10-11-pythonproject3/image-20211011140048890.png)

![image-20211011140103027](/images/2021-10-11-pythonproject3/image-20211011140103027.png)



예시)

**1. While loop**

Low = 1

High = 10

Feedback = ‘’



Guess = 1 ~ 10

→ 4 (guess by computer)

Feedback = ‘L’

**→ low = guess (4) + 1 = 5**



**2. While loop**

Low = 5,

High = 10,



Guess = 5~10

→ 8 (guess by computer)

Feedback = ‘H’

**→ high = guess(8) - 1 = 7**



**3. While loop**

Low = 5,

High = 7,



Guess = 5~7

→ 7 (guess by computer)

Feedback = ‘C’

**→ print (f’Yay! The computer guessed your number, {guess}, correctly!')**










* [12 Beginner Python Project - Coding Course](https://youtu.be/8ext9G7xspg)
  * 초급 Python 프로젝트-코딩 과정

-끝-

