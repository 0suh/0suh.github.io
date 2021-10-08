---
title: "Software Engineering QA1"
excerpt: " "

categories:
  - Software Engineering
tags:
  - [Blog, jekyll, Github, Git]

toc: true
toc_sticky: true

date: 2021-09-10
---

Q/A Sheet #1- Introduction to SE

Questions from Prof.

1. On slide 7, why is the cost distribution pattern of the iterative model and component based model different from the waterfall?
   Waterfall model의 경우, requirement definition과 design 부분에서 차지하는 cost가 약 40%, implementation 20%, 나머지가 40%를 차지한다. 사용자의 requirement가 처음부터 정확한 경우가 많지 않기 때문에 비용이 더 필요하게 된다. Iterative model은 사용자의 요구사항이 정확하지 않은 상태에서 시작하여 specify하며 requirement를 충족시킬 때까지 반복적으로 돌아가기 때문에 waterfall에 비해서 비용이 더 적게 들 수 있다. Component model의 경우 좋은 구성요소들을 모아 하나의 시스템으로 만드는 구조이기 때문에 waterfall과 비용 분포가 다르다.
2. Explain the trade-off between the essential attributes on slide 12.
   Maintainability – Responsiveness(efficiency)
   Maintainability를 위해서는 초기에 component의 크기를 작게 해야 수정/추가/삭제가 용이하다. 하지만 이럴 경우 responsiveness가 떨어지게 된다. 왜냐하면 시스템 상호간의 반응속도가 component의 크기가 작기 때문에 속도가 떨어질 것인데 이와 반대로 responsiveness를 위해 component의 크기를 크게 하면 maintainability가 떨어지므로 trade-off관계를 가진다.
3. Compare the validation and verification activities.
   Verification(Static testing)은 소프트웨어가 에러 없이 목적을 잘 달성했는지, 개발이 잘 되었는지를 확인하는 것인 반면에 validation(dynamic testing)은 코드를 실행하여 test하는데 실제로 기대하는 상품을 개발했는지 확인하는 과정이다. .
4. Explain four fundamental software engineering activities.
   Specification, development, validation, evolution 4가지로 이루어지는데 specification은 사용자가 원하는 요구조건/제약조건들을 정의하는 단계이다. Development는 소프트웨어가 디자인되고, 프로그래밍되는 과정, validation은 사용자의 요구조건을 충족하는지 확인하는 과정, 마지막 evolution은 사용자나 마켓의 바뀐 요구사항이 반영되어 수정되는 단계를 말한다.
5. Discuss the types of applications on Slide 18-20 and find more than two examples for each type.

- Stand-alone applications: Notepad, Calculator, Microsoft Word
- Interactive transaction-based applications: e-commerce applications, mail, photo sharing
- Embedded control systems: software in a mobile phone, software in a microwave
- Batch processing systems: phone billing systems, salary payment systems
- Entertainment systems: In-car entertainment, In-flight entertainment, home theater system
- Systems for modelling and simulation: climate and weather models, solar activity models, communications and computation models
- Data collection systems: sensors inside an engine, sensors in a remote location
- Systems of systems: smart homes, air plane

6. Explain why you should choose different software engineering techniques, methods, and tools depending on the context of the software project.
   모든 소프트웨어 시스템에 적용가능하고 최선의 방법인 소프트웨어 기술은 없기 때문에 프로젝트의 내용에 따라 소프트웨어 기술, 방법, 도구들을 알맞게 선택하여 사용해야 한다.
7. Think about some fundamental principles that can apply to all types of software systems.
   사용자의 요구사항을 빠짐없이 반영하는 것, 오픈소스와 같은 기존에 있던 소프트웨어를 활용하는 것, dependability, performance을 고려하여 시스템을 만들기, development process를 완벽히 이해하기 등등이 소프트웨어 시스템의 기본적인 원칙이다.
8. Describe the distinctive changes in the software development process when using web or web services as a technical platform.
   Web은 소프트웨어 서비스의 가용성을 이끌어냈는데 소프트웨어의 재사용과, 프로그래밍 언어의 발전을 야기시켰다. Web-based systems을 통해 기존에 있던 software components와 systems로부터 시스템을 만들 수 있게 하였다.
9. Investigate the fatal consequences caused by unethical behavior or decisions by software engineers.
   2015년에 폭스바겐 사의 엔지니어들이 배기가스 배출 기준을 속이도록 자동차를 프로그래밍했던 것이 드러난 사례가 있고, 또 대선에 러시아 해커들이 개입했다는 사실이 밝혀진 사례로 나라 전체가 영향을 받은 경우도 있다고 한다.
10. Discuss with your colleagues what knowledge and efforts you need to be a competitive software engineer.
    문제점이나 에러 사항에 잘 대처할 수 있는 유연성이 필요하다. 또한, 작은 부분의 실수도 전체 software system에 굉장히 큰 영향을 미칠 수 있기 때문에 실수하지 않는 꼼꼼함이 필수적이다. Software system에서의 하나의 파트 뿐만 아니라 전체적인 프로세스를 이해할 수 있는 능력을 가지고, 각각의 파트에서 요구되는 사항들을 미리 알고 있어야 시스템 설계에 있어서 안정성, 효율성을 높여 경쟁적인 소프트 엔지니어가 될 수 있다고 생각한다. 또한, 공동으로 협력하여 진행하는 프로젝트가 많으므로 팀원과의 협력과 소통이 잘 이루어져야 한다고 생각한다.

Questions from Student

1. Engineering discipline에는 크게 어떠한 분야가 있는가?
   Chemical, civil, electrical, mechanical engineering로 크게 4가지로 나뉜다.
2. Web 서비스 중 클라우드 컴퓨팅이란 무엇이고 이것의 장점이 무엇인가?
   클라우드 컴퓨팅은 사용자의 직접적인 활발한 관리 없이 데이터 스토리지, 컴퓨팅 파워와 같은 컴퓨터 시스템 리소스를 필요시 바로 제공하는 것을 말한다. 즉, 일반적으로 인터넷 기반 컴퓨팅의 일종으로 정보를 자신의 컴퓨터가 아닌 클라우드에 연결된 다른 컴퓨터로 처리하는 기술을 말한다. 주문형 접근을 가능케하여 최소한의 관리 노력으로 빠르게 예비 및 릴리스를 가능하게 한다.
