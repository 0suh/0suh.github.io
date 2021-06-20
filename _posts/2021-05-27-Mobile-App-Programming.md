```
---
title:  "모바일앱프로그래밍실습 퀴즈 요약"
excerpt: "md 파일에 마크다운 문법으로 작성하여 Github 원격 저장소에 업로드 해보자. 에디터는 Visual Studio code 사용! 로컬 서버에서 확인도 해보자. "

categories:
  - ['MobileApp']
tags:
  - [Blog, jekyll, Github, Git]

toc: true
toc_sticky: true
 
date: 2021-05-27
last_modified_at: 2021-05-27
---
```

## 모바일 앱 프로그래밍 실습

2. #### **Introduction to android**

   - 안드로이드 용어
     - Activity
     - Content Provider
     - Broadcast receiver
     - Service
     - Component
     - Layout
     - View&View group
     - Context (object containing the global state of an app. environment)
     - Intent (A messaging object to request an action from another app component)

3. #### **Basic Layout, View**

   - View & Layout

     - View: usually draws something the user can see and interact with

     - Viewgroup: an invisible container that defines the layout structure for View and other ViewGroup objects

     - <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526221309074.png" alt="image-20210526221309074" style="zoom:50%;" />

     - Layout(=ViewGroup)

       <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526221405490.png" alt="image-20210526221405490" style="zoom:50%;" />

     - View
       - ![image-20210526221427029](/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526221427029.png)

     - ID
       - 모든 View object 는 integer ID를 가진다.
       - android:id="@+id/button"
         - @ symbol at the beginning of the string indicates that the XML parser should parse and expand the rest of ID string and identify it as an ID resource 
         - symbol means that this is a new resource name that must be created and added to our resources(in R.javafile)
       - 각각의 View object는 ID로 접근가능
     - Layout Parameters

4. #### **Advanced UI**

   - **HorizontalScrollView (Layout이 아니다!!!!!)**
     - Scrollable 하지만 Clickable 이나 Focusable하지 않다.
     - 하나의 View/Layout만 위치할 수 있다. 
     - 여러개 뷰를 넣으려면 Layout을 먼저 넣어야 한다.

   - LayoutInflater (Inflation: 객체화)

     - XML로 정의된 리소스를 View로 바꾼다.
     - <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526222520607.png" alt="image-20210526222520607" style="zoom:50%;" />
     - LayoutInflater Inflater = (LayoutInflater) getSystemService (Context.LAYOUT_INFLATER_SERVICE);
     - inflater.inflate(R.layout.sub_layout, container, true);

   - ListView

     - The list items are automatically inserted to the ListView using Adapter.

     - Constructor of Adapter

       ArrayAdapter(Context context, int resource, List<T> objects);

5. #### **Activity Conversion, Intent & Broadcast**

   - Android Intent
     - An Intent is a messaging object you can use to request an action from another app component
     - Request actions from other components
     - **Explicit intent** specify the component by supplying **package name or component class name.**
     - **Implicit intent** do not specify name, just declare general action such as show the location on a map. 

   - Android Broadcast
     - Sending message protocol which declared by Android system or other application
     - Implicit Intent is exactly same with the broadcast message

6. #### **MutiThreading in Android**

   <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526225840875.png" alt="image-20210526225840875" style="zoom:50%;" />

   - UI thread (Main thread)
   - Background thread
   - AsyncTask (library forandroid multi-threading)
     - A class that supports main thread work and background thread work at the same time.
     - Executed AsyncTask is an object (재사용불가, 한번만 실행됨)
     - 동시에 오직 하나의 AsyncTask만 run
     - <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526230502173.png" alt="image-20210526230502173" style="zoom:50%;" />
     - 

7. #### **HTTP Connection**

   - HTTP(Hypertext Transfer Protocol)

     - HTTP is an application communication protocol for web service.

     - Client usually send HTTP request with JSON format and server will send response.

     - There are many HTTP methods(such as GET, POST, PUT, DELETE…), but we will treat only 2 methods, GET and POST.

       <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526231356403.png" alt="image-20210526231356403" style="zoom:50%;" />

     - GET: used to request data from a specified resource

     - POST: used to send data to a server to create/update a resource

     - #### **The most important thing is that You can’t use HTTP network in MainThread. **(because mainActivity cannot use network, all network communication should use thread or AsyncTask)

8. #### What is Flutter?

   - Flutter is...

     - An open-source mobile UI framework developed by Google

     - Can use to build native-looking Android and iOS applications from the same code base. 

     - Instead Java or kotlin language, Flutter use ‘Dart’ programming language. •

     - Offers fast development tools (support “hot reload”), modern and reactive. 

     - Consists of two important parts 

       – An SDK : includes tools to compile your code into native machine code 

       – A reactive Framework : UI Library based on widgets 

9. #### **Flutter Widget**

   - Widget
     - all in the flutter is a widget
     - 안드로이드스튜디오의 뷰와 비슷하지만 다름
     - 3가지 종류 - Stateless Widget, Stateful Widget, Inherited Widget
     - Stateless Widget: 변하지 않음. ex) Icon, Logo, Text
     - Stateful Widget: dynamically changes ex)checkbox, Radio, TextField
     - widget은 다른 위젯을 포함할 수 있음 (children)
   - Widget Tree
     - After you make new flutter project, there is main.dart in lib directory. 
     - At Android, you make your UI using .xml file. 
     - At flutter, you describe your UI using widget tree.

10. #### **Flutter Widget2**

    - MaterialApp and Scaffold
      - Normally runApp get MaterialApp Widget
      - MaterialApp's home field is filled with Scaffold
      - MaterialApp: widget for Route(like Changing Activity) and Theme
      - Scaffold: Display your application with proper format
        - AppBar 와 Bodypart를 만들 수 있게해줌 customize도 가능
    - Change Theme of application
    - Several Advanced Widgets
      - ListView (static, dynamic data 모두 가능, ListViewAdaptor처럼 itemBuilder가 데이터 display함)
      - Container: Layout Widget that contains only one child (Row, Column이랑 비슷함, 위젯의 사이즈 속성이 없을 때 사용함- ListView, TextField, alignmnet field로 정렬가능)

11. #### **Flutter Navigator**

    - Navigator
      - 모바일앱에는 스크린이나 페이지(풀 스크린)이 있는데 flutter 에서는 routes로 부른다. 
      - flutter navigator widget이 route를 관리한다.
      - Navigator's Stack Management<img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210526235255141.png" alt="image-20210526235255141" style="zoom:50%;" />
    - Navigation
      - Direct Navigation
        - 페이지를 직접 불러서 다음 페이지(라우트)로 넘어간다.
        - "MaterialPageRoute" class와 "Navigator.push()" function 사용
        - 라우트에게 이름 없음 => un-named routing
      - Static Navigation
        - Route Map과 함께 다음 라우트로 이동
        - 라우트는 라우트앱에 이름을 할당받아야함
        - "Navigator.pushNamed()" function 사용
        - 각각의 라우트는 이름이 있음 => named routing
      - Dynamic Navigation
        - Has the advantage that you can create routes and access the passed through arguments.
        - "onGenerateRoute()" function과 "Navigator.pushNamed()" function 사용
        - 각각의 라우트는 이름이 있음 => named routing
    - State Management
      - Sharing states between different pages
        - When managing states within single page, you can use StatefulWidget. 
        - Managing states between different pages with the StatefulWidget is very complicated and inefficient.
      - Flutter recommends to use StatelessWidget and reload the full or the part of page with state management tool whenever updating states.
      - Flutter supports efficient state management tools 
        - Provider with ChangeNotifier (Simple) 
        - Redux (Powerful) 
        - Bloc (Powerful) …

12. #### **Flutter Networking**

13. #### Platform Channel

    - 왜 필요한가? ex) flutter cannot access to the smartphone’s sensor data. We can get sensor data by using platform channel

       <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210527015140862.png" alt="image-20210527015140862" style="zoom:50%;" />

    - 아키텍쳐
      - Messages are passed between Flutter app(client) and host(Android or IOS) using platform channel. 
      - On Flutter, we use MethodChannel(API) to send message which call Host side function, and Android MethodChannel will receive method call and send back result. 
      - There are 3 kinds of common channels. 
        - MethodChannel :When you want to call android(or IOS) function. You can invoke a method from flutter app to native platform code. 
        - EventChannel :Using when user want asynchronous stream data. You can treat the event which occurred continuously (e.g. sensor data).
        - BasicMessageChannel (When you use a codec for encoding and decoding, e.g. image)

14. #### Asynchronous programming in Flutter

    - Flutter's Multi-threading

      - 가능한가?

        Despite being a single-threaded language, Dart offers support modern, asynchronous, and reactive method : isolates and event loops

        <img src="/Users/youngsuh/Library/Application Support/typora-user-images/image-20210527015510139.png" alt="image-20210527015510139" style="zoom:50%;" />

    - Isolates and Event Loops
      - An isolate is what all Dart code runs in, which has its own memory and a single thread of execution that runs an event loop.
      - When Application have a enormous computation to perform, then user can us Isolate.spawn() or Flutter’s compute() function
      - The isolates can work together by passing messages back and forth, using its event loop
      - This lack of shared memory offer some key benefits 
      - An event loop is a background infinite loop which periodically wakes up and looks in the event queue for any tasks that need to run.
      - If any exist, the event loops puts them onto the run stack if and only if the CPU is idle. 
      - When app runs an event loop, it grabs the oldest event from its event queue, processes it, goes back for the next one, processes it, and so on, until the event queue is empty
      - So, Dart handle these in the following way. 
        - 1. An activity that is well-known to be slow is started up as normal. 
          2.  The moment it begins waiting for something — disk, HTTP reque st, whatever — it is moved away from the CPU. 
          3. A listener of sorts is created. It monitors the activity and raises an alert when it is finished waiting. 
          4. The reference to that listener is returned to the main thread. This reference object is known as a Future. 
          5. The main thread continues chugging along its merry way. 
          6. When the waiting activity is finally resolved, the event loop sees it and runs an associated method on the main thread to handle finishing up the slow event
