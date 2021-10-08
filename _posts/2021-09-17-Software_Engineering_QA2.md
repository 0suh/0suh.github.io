---
title: "Software Engineering QA2"
excerpt: " "

categories:
  - Software Engineering
tags:
  - [Blog, jekyll, Github, Git]

toc: true
toc_sticky: true

date: 2021-09-17
---

Software Engineering Q/A Sheet #2

Questions from Prof.

1. Compare sociotechnical systems to conventional technical computer-based systems.
   A. Technical computer-based systems는 하드웨어, 소프트웨어는 포함하지만 sociotechnical systems와 달리 operators와 operational processes를 시스템에 포함하지 않는다. 시스템과 상호작용하는 사람과 operational processes까지 모두 포함하는 socio-technology systems는 organizational policies와 rules에 의해 관리된다.
2. Assume the difference between a hardware failure and a software failure. Note that a hardware failure is represented by a bathtub curve.
   A. Software failure는 시간이 지남에 따라 failure가 지속적으로 감소하는 반면에 hardware failure는 시간이 지날수록 점점 감소하다가 일정 시간이 지난 후로는 급격하게 증가한다. 이는 하드웨어의 수명때문에 나타나는 bathtub curve라고 볼 수 있다.
3. Discuss about failure propagation between hardware, software and operator.
   A. Failure가 하드웨어, 소프트웨어, operator 중 한군데에서만 일어나도 서로간에 전파가 일어날 수 있다. 하드웨어에서 처음 failure가 일어난 경우, 예를 들어 센서를 인식하는 구성요소의 고장이 일어나면 software에서 신호를 받아들이지 못해 failure가 일어나고, operator에서도 제대로 작동하지 않아 전체 시스템에 문제가 생길 수 있는failure propagation이 발생할 수 있다.
   (Hardware failure : Extremes of environments, Temperature, Humidity, Ingress of dusts or liquids, Shock, Vibration, Signal screening, Cable separation.)
4. Discuss and remember about the system engineering process and the relationships between conceptual design, procurement, development, and operation.
   A. System engineering process중 conceptual design에서는 전체적인 목표, 특징을 반영하여 추상적인 시스템 디자인을 정하고, procurement 단계에서 이전 단계에서 정한 디자인에 맞는 시스템에 대하여 어떤 시스템을 개발/구입/외주할지 결정한다. 다음 development 단계에서는 요구사항의 구체화, 디자인, 건설, 통합, 테스트가 이루어지는데 앞단계들에서 구상된 시스템을 개발하는 과정이다. 그러므로 필요한 물품 조달과 구상들이 이루어지지 않으면 개발할 수 없다. Operation 단계에서는 고객의 환경에서 목적을 잘 반영하여 시스템이 구상되었는지 실제 사용되어진다. 새로운 요구사항이 생기면 반영하고 마지막에는 시스템이 해체된다. 4가지 단계 모두 하나라도 없으면 system engineering이 이루어지지 않으므로 서로 상호 의존적이다.
5. What do you think is necessary for parallel development of large systems?
   A. Plan이 중요하다. 하드웨어 변경을 위해서는 비용이 많이 들기 때문에 소프트웨어가 하드웨어를 대신할 수 있도록 하기 위하여 병렬 개발을 위한 계획을 잘 세워야 한다.
6. Discuss and remember the system development process from requirement development to system deployment.
   A. Requirements engineering: conceptual design에서 확인한 요구사항들을 분석하고 정리한다.
   B. Architectural design: 전체 시스템의 설계를 세우고, 각 구성요소들과 그것들의 관계를 정립한다.
   C. Requirements partitioning: 서브시스템이 요구사항 중 어떤 부분을 담당할지 결정한다.
   D. Subsystem engineering: 시스템의 소프트웨어 구성 요소들을 개발하고 operation process를 정의, business process를 재디자인 한다.
   E. System integration: 새로운 시스템을 만들기 위해 시스템요소들을 합친다.
   F. System testing: 전체 시스템을 테스트하고 문제점을 찾는다
   G. System deployment: 사용자들에게 시스템을 이용 가능하게 하는 과정으로 기존 시스템으로부터 데이터를 전송하고 다른 시스템들과의 소통을 가능하게 한다.
7. Discuss why procurement decisions affect system functionality, such as reliability.
   A. 잘못된 결정을 하게 되면 시스템의 배송 지연이나 작동 환경에 적합하지 않은 시스템을 개발하게 될 수 있다. 잘못된 시스템/공급자가 결정된 경우 시스템의 technical process와 software engineering 과정이 더 복잡해질 수 있다.
8. Discuss how the various activities of the system development process affect system dependability.
   A. 서브시스템으로 나뉘어 개발되었던 시스템들을 통합한 전체 시스템이 사용자가 원하는 대로 작동을 하는지 아닌지에 따라서 system dependability에 영향을 준다. 서브시스템은 세분화된 목표를 가지고 개발되었지만 통합될 때에는 전체적인 목표를 충족시키도록 이루어져야 하기 때문에 이 과정이 영향을 많이 미칠 것이다.
9. Discuss one or more examples of the various barriers to protect human error.
   A. 커뮤니케이션 : 인간의 오류는 커뮤니케이션 부족으로 인해 일어날 수 있으므로 모든 개발자, 상사와 소통하는데 불편함 없이 개방적으로 상호 교류가 일어나야 한다.
   B. 훈련+교육 증가
   C. 민감한 시스템에의 접근을 제한시킨다.
   D. 직무적성에 적합한 작업자를 해당 관련 업무에 배치/선발한다.
10. Discuss and summary about why the evolution is costly.
    A. 바뀐 요구사항에 따라 서브시스템을 바꾸려고 한다면 그 변화로 인해서 전체 시스템에 예상치 못한 문제점이 생길 수 있기 때문이다. 또한 새로운 구성요소의 통합으로 인해서 전체 구조에 변화가 생기면 전체적인 조정/변화가 필요하기 때문이다.

Questions from Student

1. Human errors의 예시에는 어떠한 것들이 있는가?
   A. 시스템 개발 단계(설계, 생산, 시험, 가동 등)
   i. 누락오류(자동차에서 하차 시 전조등을 끄는 것을 잊고 내려 방전이 된 경우))
   ii. 작위오류(주차금지 구역에 주차를 하여 스티커를 발부 받은 경우)
   iii. 순서오류(자동차 출발 시 사이드 브레이크를 내리지 않고 엑셀러레이터를 밟는 것과 같이 순서를 바꾸어 수행한 경우
   iv. 시간오류(수행해야 할 작업을 정해진 시간동안 완수하지 못하는 에러
   v. 불필요한 수행오류(작업 완수에 불필요한 작업을 수행하는 에러)
2. Plan-driven development 방식의 단점은 무엇인가?
   A. 너무 계획에 치중을 하게 되면 개발 방법 자체가 너무 형식에만 신경을 쓰게 되어 얽매일 수 있다. 이미 세워진 계획하에서 융통성을 발휘할 수 없는 부분이 발생하게 되고, 반드시 따라야 하는 단계들이 있을 경우 전체 개발의 흐름을 느리게 할 수 있다.
