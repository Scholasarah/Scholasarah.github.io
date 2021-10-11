---
Title: Beginner Python Project (2/12)
categories:
  - python
tags:
  - python
  - computer science
  - Guessing number
---



# Beginner Python Projects (2/12)

**2. Guess the Number (Computer)**

Random 이라는 함수를 lib에서 import 해옴.

random.randint 함수 → 랜덤으로 1개의 숫자를 뽑을 수 있음.





**CODE 작성법:**

```python
import random

def guess(x):
    random_number = random.randint(1, x)
    guess = 0
    while guess != random_number:
        guess = int(input(f'Guess a number between 1 and {x}: '))
        if guess < random_number:
            print('Sorry, guess again. Too low.')
        elif guess > random_number:
            print('Sorry, guess again. Too high.')
    print(f'Yay, congrats. You have guessed the number {random_number} correctly!!')

guess(10)
```



![image-20211011135837819](/images/2021-10-11-pythonproject2/image-20211011135837819.png)



While loop 에서 guess한 숫자가 random_number랑 같지 않을때,

**< random number** 인지 **> random number** 인지에 따라 print 되는 글이 다르고,

Guess = random_number (While loop이 깨지는 순간) 일때는 맞췄다는 글이 print 됨.






* [12 Beginner Python Project - Coding Course](https://youtu.be/8ext9G7xspg)
  * 초급 Python 프로젝트-코딩 과정

-끝-

