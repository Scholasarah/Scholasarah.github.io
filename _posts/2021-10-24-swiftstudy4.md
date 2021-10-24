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
