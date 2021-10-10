---
Title: Basic Python Course (3/4)
categories:
  - python
tags:
  - python
  - computer science
  - dictionary
  - while 반복문
  - for 반복문
  - guessing game
  - exponent function
  - nested loops
  - translator
---



# Basic Python Course (3/4)

**Python 3**

**Building a Better Calculator**

op = operator (+ - / * )

![image-20211010154559710](/images/2021-10-08-pythonprac3/image-20211010154559710.png)



**Dictionaries**

Key : value 순으로 작성

![image-20211010154618394](/images/2021-10-08-pythonprac3/image-20211010154618394.png)

Value 를 받기 위해서는 2가지 방법이 있음.

**1. print(monthConversions[“Nov”])**

![image-20211010154635465](/images/2021-10-08-pythonprac3/image-20211010154635465.png)

**2. print(monthConversions.get(“Nov”))**

![image-20211010154657035](/images/2021-10-08-pythonprac3/image-20211010154657035.png)

\* get function 을 사용하면 아래와 같이 dictionary에 작성하지 않은 내용들을 “**None**” 으로 표시함.

![image-20211010154715161](/images/2021-10-08-pythonprac3/image-20211010154715161.png)

![image-20211010154728984](/images/2021-10-08-pythonprac3/image-20211010154728984.png)



**While 반복문** 

**i = i + 1 → i += 1** **으로도** **표현이** **가능**

![image-20211010154751862](/images/2021-10-08-pythonprac3/image-20211010154751862.png)



**Building a Guessing Game**

![image-20211010154810971](/images/2021-10-08-pythonprac3/image-20211010154810971.png)

**Setting a limits to the no. of guesses**

![image-20211010154827649](/images/2021-10-08-pythonprac3/image-20211010154827649.png)



**For 반복문**

Giraffe Academy 의 letter를 프린트하라는 의미

![image-20211010154847964](/images/2021-10-08-pythonprac3/image-20211010154847964.png)

Friends 리스트에서 친구들을 리스트하라는 의미 

![image-20211010154905341](/images/2021-10-08-pythonprac3/image-20211010154905341.png)

숫자 range

**0<=  &  <10 (****앞에는** **포함****,** **뒤는** **포함** **안함****!)**

![image-20211010154922026](/images/2021-10-08-pythonprac3/image-20211010154922026.png)

![image-20211010154935070](/images/2021-10-08-pythonprac3/image-20211010154935070.png)

len(friends) → friends 의 숫자(length 함수) = 3

그럼 위의 함수는 range(3)을 찾는거고, range 3 → 0,1,2 를 찾으라는 의미니깐

**friends[index] → friends[0], friends[1], friend[2]** **의** **의미를** **가지고** **있음**

![image-20211010154952113](/images/2021-10-08-pythonprac3/image-20211010154952113.png)

![image-20211010155002062](/images/2021-10-08-pythonprac3/image-20211010155002062.png)



**Exponent Function (지수함수)**

print(2**3) → 2 cube = 8

For loop 를 활용한 파이썬

![image-20211010155020075](/images/2021-10-08-pythonprac3/image-20211010155020075.png)

(해설)

for index in range(power_num)에서 power_num = 4

근데 for loop 안을 보니까 pow_num을 사용안함. 즉, 그냥 pow_num은 loop을 돌리는데만 사용한다는 얘기.

**그래서 index가 0,1,2,3 총 4번 돌아가는 for loop를 사용한다는 의미.**



result = result * base_num

1* 3(index=0일때) * 3(index=1일때) * 3(index=2일때) * 3(index=3일때)



🍯**팁!**

for loop는 돌리는데 아까처럼 index 사용할 필요 없을때는

for _ in range(4): 처럼 underscore를 쓰기도함.



**2D Lists & Nested Loops (배열속 배열과 반복문 속 반복문)**

4rows & 3columns

**number_grid[row][col] → number_grid[0][1] → 0****번째** **row & 1****번째** **column = 2**

![image-20211010155043528](/images/2021-10-08-pythonprac3/image-20211010155043528.png)

Using **For loop inside For Loop**;

![image-20211010155110654](/images/2021-10-08-pythonprac3/image-20211010155110654.png)



**Building a Translator**

Giraffe Language;

Vowels (모음) → g

——————————

dog → dgg

cat → cgt

![image-20211010155127640](/images/2021-10-08-pythonprac3/image-20211010155127640.png)

*** Lower/Upper capital letters (****좀** **더** **advanced** **된** **예시****)**

![image-20211010155143515](/images/2021-10-08-pythonprac3/image-20211010155143515.png)







* [파이썬(Python) 배우기 - 초심자를 위한 기초강의모음](https://www.youtube.com/watch?v=rfscVS0vtbw)
  * 파이썬(Python) 배우기 - 초심자를 위한 기초강의모음

-끝-

