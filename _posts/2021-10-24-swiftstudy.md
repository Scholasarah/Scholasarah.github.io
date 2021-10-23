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

**Lesson 3:How to build user innterfaces**





**Lesson 3 Challenge**

- 텍스트 작성 후, padding 및 background 색 표현



```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        
        Text("Hello, world!")
            .font(.body)
            .foregroundColor(Color.white)
            .padding(.all)
            .background(Color.green)
        
            .cornerRadius(10)
            .padding(.all)
            .background(Color.black)
            .cornerRadius(10)
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
```





![image-20211024085521422](/images/2021-10-24-swiftstudy/image-20211024085521422.png)







* [2021 SwiftUI Tutorial for Beginners](https://youtu.be/F2ojC6TNwws)

-끝-
