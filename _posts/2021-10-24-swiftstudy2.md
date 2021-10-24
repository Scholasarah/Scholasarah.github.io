---
Title: SwiftUI Study 2
categories:
  - Swift
tags:
  - Swift
  - SwiftUI
  - iOS
---



# SwiftUI Study 2

**Lesson 4:SwiftUI Views and Containers**

![image-20211024090233135](/images/2021-10-24-swiftstudy2/image-20211024090233135.png)



Image("logo").resizable().aspectRatio(contentMode: .fit)
→ logo 이미지를 삽입해서, resize (전체 페이지로 크게 키움) & content mode 로 화면에 맞게 비율을 맞추는 표현.





**Lesson 4 Challenge**

![image-20211024090259842](/images/2021-10-24-swiftstudy2/image-20211024090259842.png)



<u>Swift 작성법:</u>



```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        
        VStack{
            ZStack{
                Image("toronto").resizable().aspectRatio(contentMode: .fit).cornerRadius(10)
                VStack{
                    Text("CN Tower")
                        .font(.largeTitle)
                        .padding([.top, .leading, .trailing])
                    Text("Toronto")
                        .font(.body)
                        .padding([.leading, .bottom, .trailing])
                }
                .background(/*@START_MENU_TOKEN@*//*@PLACEHOLDER=View@*/Color.black/*@END_MENU_TOKEN@*/)
                .foregroundColor(Color.white)
                .cornerRadius(10)
                .opacity(0.8)
            }.padding()
            
            ZStack{
                Image("london").resizable().aspectRatio(contentMode: .fit).cornerRadius(10)
                VStack{
                    Text("Big Ben")
                        .font(.largeTitle)
                        .padding([.top, .leading, .trailing])
                    Text("London")
                        .font(.body)
                        .padding([.leading, .bottom, .trailing])
                }
                .background(/*@START_MENU_TOKEN@*//*@PLACEHOLDER=View@*/Color.black/*@END_MENU_TOKEN@*/)
                .foregroundColor(Color.white)
                .cornerRadius(10)
                .opacity(0.8)
            }.padding()
        }
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}

```





* [2021 SwiftUI Tutorial for Beginners](https://youtu.be/F2ojC6TNwws)

-끝-
