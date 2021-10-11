---
Title: Beginner Python Project (4/12)
categories:
  - python
tags:
  - python
  - computer science
  - Rock Paper Scissor
---



# Beginner Python Projects (4/12)

**4. Rock Paper Scissor**



**Code 작성법**:

```python
import random

def play():
    user = input("What's your choice? 'r' for rock, 'p' for paper, 's' for scissors: ")
    computer = random.choice(['r', 'p', 's'])

    if user == computer:
        return 'It\'s a tie'
    # r > s, s > p, p > r
    if is_win(user, computer):
        return 'You won!'

    return 'You lost!'

def is_win(player, opponent):
    # return true if player wins
    # r > s, s > p, p > r
    if (player == 'r' and opponent == 's') or (player == 's' and opponent == 'p') or (player == 'p' and opponent == 'r'):
        return True

print(play())
```



졌을때:

![image-20211011140954517](/images/2021-10-11-pythonproject4/image-20211011140954517.png)

이겼을때:

![image-20211011141005268](/images/2021-10-11-pythonproject4/image-20211011141005268.png)

비긴 경우:

![image-20211011141014633](/images/2021-10-11-pythonproject4/image-20211011141014633.png)








* [12 Beginner Python Project - Coding Course](https://youtu.be/8ext9G7xspg)
  * 초급 Python 프로젝트-코딩 과정

-끝-

