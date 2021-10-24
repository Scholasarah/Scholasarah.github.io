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

**Lesson 5:War Card Game UI Construction**



<u>Stack 방법:</u>

HStack - 이미지/텍스트를 양옆으로 stack

VStack - 이미지/텍스트를 위 아래로 stack

ZStack - 이미지/텍스트를 앞뒤로 stack



![image-20211024090701583](/images/2021-10-24-swiftstudy3/image-20211024090701583.png)

레슨 4까지 배운 내용들을 토대로, 카드 게임을 swift로 표현하는 챌린지 수업






```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        
        ZStack{
            Image("background").ignoresSafeArea()
            
            VStack{
                Spacer()
                Image("logo")
                Spacer()
                
                HStack{
                    Spacer()
                    Image("card3")
                    Spacer()
                    Image("card4")
                    Spacer()
                }
                
                Spacer()
                Image("dealbutton")
                Spacer()
                
                HStack{
                    Spacer()
                    VStack{
                        Text("Player")
                            .font(.headline)
                            .foregroundColor(Color.white)
                            .padding(.bottom)
                        Text("0")
                            .font(.largeTitle)
                            .foregroundColor(Color.white)
                    }
                    Spacer()
                    VStack{
                        Text("CPU")
                            .font(.headline)
                            .foregroundColor(Color.white)
                            .padding(.bottom)
                        Text("0")
                            .font(.largeTitle)
                            .foregroundColor(Color.white)
                    }
                    Spacer()
                }
                Spacer()
            }
        }
    
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
```



![image-20211024090627229](/images/2021-10-24-swiftstudy3/image-20211024090627229.png)






* [2021 SwiftUI Tutorial for Beginners](https://youtu.be/F2ojC6TNwws)

-끝-
