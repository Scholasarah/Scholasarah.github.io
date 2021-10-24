---
Title: SwiftUI Study
categories:
  - Swift
tags:
  - Swift
  - SwiftUI
  - iOS
---



# SwiftUI Study

**Lesson 6:Swift Programming: Variables and Constants**

<img src="/images/2021-10-24-swiftstudy4/image-20211024091436108.png" alt="image-20211024091436108" style="zoom:50%;" />



**Swift Variables**

​	var myVar → 지정한 variable의 이름은 myVar 

![image-20211024091502165](/images/2021-10-24-swiftstudy4/image-20211024091502165.png)

**표현법:**

​	**var** myInt = 100

​	print(myInt)

​	혹은

​	**var** myInt:Int = 100

​	print(myInt)

<u>표현하는 방법이 다양함</u>

![image-20211024091522321](/images/2021-10-24-swiftstudy4/image-20211024091522321.png)





**Swift Constants**

![image-20211024091604458](/images/2021-10-24-swiftstudy4/image-20211024091604458.png)

→ 이미 myConst 를 hello로 지정해두었는데, 바로 다음에 world 로 바꾸어 버리면, ERROR가 생김.



작성법:

​	var firstName = “Tom”

​	let lastName = “Smith”



<u>var과 let의 차이</u>

→ The difference between a constant and a variable is that you *cannot* reassign a different piece of data to a constant after declaring it. 

*(Variables are much more flexible than constants.)*



**Variable & Constants naming 할때의** 🍯**TIP!**

- **Camel casing** simply means starting the first word with a lowercase letter, and starting every subsequent word with an uppercase letter.

[Reference Page](https://codewithchris.com/swift-tutorial-complete/ )



**Lesson 6 Challenge**

Challenge:
 4 people have dinner and want to split the bill.
 Calculate the total with tax then how much each person owes.
 Assign it to the variable, 'split' and then print it out to the console area.



```swift
let people:Double = 4
let subtotal:Double = 128
let tax = 0.13
var split:Double = 0

//Solution 1:
split = (subtotal * (1+tax)) / people
print(split)
```


```swift
let people:Double = 4
let subtotal:Double = 128
let tax = 0.13
var split:Double = 0


//Solution 2:
var totalCost = subtotal + (subtotal * tax)
split = totalCost / people
```






* [2021 SwiftUI Tutorial for Beginners](https://youtu.be/F2ojC6TNwws)

-끝-
