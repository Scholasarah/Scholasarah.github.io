---
Title: Basic Python Course (4/4)
categories:
  - python
tags:
  - python
  - computer science
  - comments
  - try/except
  - module
  - PIP
  - class&object
  - object function
  - multiple choice quiz
---



# Basic Python Course (4/4)

**Python 4**

**Comments (주석)**



\# 를 활용하거나, ‘’’ (‘X3번)을 활용하면, comments 를 달아도, 보이지는 않음.

![image-20211010155444329](/images/2021-10-08-pythronprac4/image-20211010155444329.png)



**Try/Except (예외처리)**

Try:

​	오류날 수 있는 코드

Except [발생오류 (as 오류 메시지 변수)]:

​	오류 발생 시, 실행할 코드

![image-20211010155511409](/images/2021-10-08-pythronprac4/image-20211010155511409.png)

**0****으로** **나눴을때** **error message** **표현** **방법****:**

![image-20211010155526847](/images/2021-10-08-pythronprac4/image-20211010155526847.png)

![image-20211010155540435](/images/2021-10-08-pythronprac4/image-20211010155540435.png)



**Reading Files (파일 읽기)**

open(“열고싶은 파일 이름”, “r”)

→ 여기서 **r = read, w = write, a = append**(you can’t change or modify, but can ADD to the file)

**“r+” → read+write**



open(“employee.txt”, “r”) and all of the contents inside of it are stored inside employee_file variable.

<img src="/images/2021-10-08-pythronprac4/image-20211010155555058.png" alt="image-20211010155555058" style="zoom:50%;" />

To close →

![image-20211010155621104](/images/2021-10-08-pythronprac4/image-20211010155621104.png)

파일이 읽을 수 있는지 확인하는 함수

![image-20211010155649460](/images/2021-10-08-pythronprac4/image-20211010155649460.png)

print(employee_file.read()) → employee_file 내용을 보여주는 함수

![image-20211010155708357](/images/2021-10-08-pythronprac4/image-20211010155708357.png)



**print(employee_file.readline())** → 파일을 한줄씩 나타내는 함수.

5줄이면, 5번 써야 모든 llne이 나옴



**print(employee_files.readlines())** → 파일의 lines를 한줄로 array 시키는 작업.

print(employee_files.readlines()[1]) → 파일 lines 중에 index1 만 나옴.



**For Loops;**

![image-20211010155725890](/images/2021-10-08-pythronprac4/image-20211010155725890.png)



**Writing to Files (파일 쓰기)**

Employees 파일의 맨 마지막 부분에 “Toby - Human Resources” 를 추가하는 기능.

![image-20211010155741661](/images/2021-10-08-pythronprac4/image-20211010155741661.png)

하지만 조심해야하는 부분은,

두번 Run 버튼을 누르면, 내용이 두번 추가가 됨. (심지어 enter 도 안되고 이어서)

*** If you append sth wrong to the file, it’s permanent & getting saved inside the file.**



\n → Enter 의 기능을 가지고 있음.

![image-20211010155757957](/images/2021-10-08-pythronprac4/image-20211010155757957.png)



open(“employees.txt”, “w”) 를 쓰고, Kelly - Customer Service 라고 작성하고 Run 하면, 파일에 Kelly 내용만 있고, 나머지는 다 사라짐. (Overwrite 효과)



**Writing to File (3가지 기능):**

- Overwrite an existing file
- Write a new file and create it
- Append onto the end of file





**Modules & PIP**

다른 파이썬 파일을 불러와서 기능을 사용할 수 있음.

Import 파일_이름

print(파일_이름.~~~) → 파일이름+. 을 적으면, 자동으로 그 파이썬 파일안에 있는 함수를 다 가지고 옴.

![image-20211010155814424](/images/2021-10-08-pythronprac4/image-20211010155814424.png)

[**https://docs.python.org/3/py-modindex.html**](https://docs.python.org/3/py-modindex.html) 





**Classes & Objects**

\* Class = 설계도, 틀 같은 것

\* Object = 틀로 만든 과자, 설계도로 만들어진 피조물

![image-20211010155834370](/images/2021-10-08-pythronprac4/image-20211010155834370.png)

class 클라스이름: 

def__init__(self) → 초기화하는 함수 (적지 않으면 오류 발생)

__init__() function is called automatically every time the class is being used to create a new object.

![image-20211010155854769](/images/2021-10-08-pythronprac4/image-20211010155854769.png)



**Building a Multiple Choice Quiz**

<img src="/images/2021-10-08-pythronprac4/image-20211010155909940.png" alt="image-20211010155909940" style="zoom: 50%;" />

![image-20211010155930606](/images/2021-10-08-pythronprac4/image-20211010155930606.png)

![image-20211010155940943](/images/2021-10-08-pythronprac4/image-20211010155940943.png)



**Object Functions**

![image-20211010155955859](/images/2021-10-08-pythronprac4/image-20211010155955859.png)

![image-20211010160005028](/images/2021-10-08-pythronprac4/image-20211010160005028.png)



**Inheritance**

![image-20211010160023257](/images/2021-10-08-pythronprac4/image-20211010160023257.png)

![image-20211010160033582](/images/2021-10-08-pythronprac4/image-20211010160033582.png)

**ChineseChef를 추가해서, general chef가 할수 있는걸 다 할수있다고 가정하에, (inheritance 기능을 사용!)**

*** class ChineseChef(Chef): → Inside “ChineseChef“ class, I want to use all of the functions inside the “Chef” class.**

![image-20211010160048248](/images/2021-10-08-pythronprac4/image-20211010160048248.png)

General chef 는 make_special_dish = bbq rib 인데, 

ChineseChef 는 make_special_dish = orange chicken 임.

→ 즉, 그냥 overwrite 한다고 생각하고 다시 작성하면 됨!

![image-20211010160104772](/images/2021-10-08-pythronprac4/image-20211010160104772.png)





* [파이썬(Python) 배우기 - 초심자를 위한 기초강의모음](https://www.youtube.com/watch?v=rfscVS0vtbw)
  * 파이썬(Python) 배우기 - 초심자를 위한 기초강의모음

-끝-

