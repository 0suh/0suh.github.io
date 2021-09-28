---
title: "01_Network Model"
excerpt: " "

categories: Computer Network
tags:
  - [Blog, jekyll, Github, Git]

toc: true
toc_sticky: true

date: 2021-09-27
last_modified_at: 2021-09-27
---

# 01_Network Model

- Network model
- Switched Networks
  - circuit switching ->요새는 잘 안씀
  - packet swtiching
- Packet Swtiching
  - Datagram
  - Virtual history

## Network Models - computer network

### Data Communications

: wire cable/wireless 같은 transmission medium의 형태를 통한 두 디바이스간의 data의 교환

### Networks

: A set of (often refered to as nodes) connected by communication links

노드는 컴퓨터, 프린터, 혹은 모든 디바이스가 될 수 있다. 데이터를 송수신할 수 있는 장치

## Switched Networks

switched network : 가장 빠른 길을 찾도록 해주는 길라잡이

intermediate network nodes (routers) 로 이루어진 네트워크를 통해 SRC->DST 까지 데이터 전송

nodes와 connection의 모음 = communication network

2가지 switching technologies

1. Circuit switching (전화, old) : 길을 사전에 정하고 데이터가 따라간다.

   - 두 stations 사이에 Dedicated communication path(전용 채널 만들어 놓음), 공유하지 않는다.
   - 데이터 전송 전에 길이 정해진다.
   - 3가지 단계
     - Establish
     - Tranfer
     - Disconnect
   - 연결을 만들기 위해서 switching capacity와 channel capacity를 가지고 있어야 한다.
   - routing을 할 수 있는 지능을 가지고 있어야 한다.
   - 효율적이지 않음
     - 데이터가 없으면 capacity가 낭비된다.
   - connection을 만드는데 시간이 걸린다. (데이터 전송 전에 딜레이가 생김)
   - 한번 연결되면 전송이 transparent하다. (=한번 연결되면 통신이 잘 이루어진다)
   - voice를 위해 설계되었다.

2. Packet switching (New) : 사전에 길을 정하지 않음. Resource 점유 X, 공유 O --> 딜레이가 적다.

- shared, channelized
- 길을 사전에 정하지 않기 때문에 길이 막혀도 다른길을 선택할 수 있다.
  - ex. 전쟁중 - 문제생겼을때 해결 가능
-
