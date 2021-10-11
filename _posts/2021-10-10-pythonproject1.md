---
Title: Beginner Python Project (1/12)
categories:
  - python
tags:
  - python
  - computer science
  - madlibs
---



# Beginner Python Projects (1/12)

**1. Madlibs**



**Madlibs Game** 이란?

→ 명사, 동사, 형용사 등 떠오르는 대로 단어를 작성하여, 스크립트/스토리 빈칸에 순서대로 단어를 채워넣어 내용을 채우는 게임.



그 재미있는 **Madlibs Game**을 위해 python으로 프로젝트를 만들어 봤어요.

python 에서 알아야하는 함수는



**f string**;

**f “{****변수****} “** **→** **앞에** **f****를** **붙이고****,** **변수를** **넣을** **위치에** **{****변수****}** **를** **넣으면** **쉽게** **사용할** **수** **있음**





```

# string concatenation (aka how to put strings together)
# suppose we want to create a string that says "subscribe to _____ "
youtuber = "ABC" # some string variable

# a few ways to do this
print("subscribe to " + youtuber)
print("subscribe to {}".format(youtuber))
print(f"subscribe to {youtuber}")

adj = input("Adjective: ")
verb1 = input("Verb: ")
verb2 = input("Verb: ")
famous_person = input("Famous person: ")
madlib = f"Computer programming is so {adj}! It makes me so excited all the tme because \
I love to {verb1}. Stay hydrated and {verb2} like you are {famous_person}!"

print(madlib)

```





![image-20211010161502060](/images/2021-10-10-pythonproject1/image-20211010161502060.png)

![image-20211010161513966](/images/2021-10-10-pythonproject1/image-20211010161513966.png)






* [12 Beginner Python Project - Coding Course](https://youtu.be/8ext9G7xspg)
  * 초급 Python 프로젝트-코딩 과정

-끝-

