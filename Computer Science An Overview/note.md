Computer Science: An Overview
=============================

- 담당 교수 송월봉
- 수업 시간 Fri at 1 PM A Week for 2 hours

# 2016-03-25 Fri
#### 컴퓨터와 로봇의 차이는 무엇일까?
- 컴퓨터

  추상적인 구조가 사람과 닮아 있다.
- 로봇

  외형적인 모습이 사람과 닮아 있다.

#### 개인용 컴퓨터의 기본적인 Architecture
1. S/W
2. H/W
  1. CPU
    1. MM _Main Memory_
    2. ALU _Arithmetic and Logic Unit_
    3. CU _Control Unit_

    넓은 의미로서 CPU 를 말한다면 위 세 가지 모두이지만
    좁은 의미로서 CPU 를 말한다면 ALU, CU 만을 가르킨다.
  2. periphery
    1. io deivce
    2. auxiliary memory
    3. modem
      - **mod**ulator: D -> A
      - **dem**odulator: A -> D

오래전 반도체가 없던 시절에는 디스크를 주기억장치로 활용하기도 했었음.

#### ALU
ALU 는 CPU 의 구성요이며 다음의 명령을 처리할 수 있다.

- Arithmetic
- Logic
- Relation _e.g lt, le, gt, ge (부등식), eq, ne_

> ne 는 표현할 때 _!=_ 또는 _**<>**_ 로 표기합니다.

##### Precedence
|Name      | Precedence |
|:---------|-----------:|
|Arithmetic|           1|
|Relation  |           2|
|Logic     |           3|

ALU 와 CU 를 하나의 칩으로 만든 것이 micro processor, 
이를 한번 더 줄여 processor 라고 부릅니다.

스마트폰의 프로세서는 AP 라고 부릅니다: **A**pplication **P**rocessor

_Media_ 감각, sensation 을 의미한다.
그렇다면 TV 는 **눈**과 **귀**를 동시에 사용하므로 TV 를 multi media 라고 부른다.

_UPS_ uninterruptible power supply 전원 공급 장치

## Algorithm
알고리즘의 시초는 수학이었다.
> 최대 최소 정리 증명에서 알고리즘이 사용되었음.

Godel's Incomplete Theorem: Some problems cannot be solved by algorithms

Algorithms for a magic trick

어떤 두 개의 비교 방법은 **정략적 비교**와 **정성적 비교** 두 가지가 있다.

### 컴퓨터 역사

#### 초기 컴퓨터
- Abacus
- Gear-based machines (치차식: 이빨식) 1600-1800
  - 네이피어의 봉
  - Blaise Pascal
  - Wilhelm Leibniz
    파스칼의 기계 발전
  - Charles Babbage 1830
    컴퓨터 제안
  
  이 이후 계산기 이론(컴퓨터)는 미국으로 넘어가게 된다.

#### Early Data Storage
- Punched Cards
  - Firsted used in Jacquard Loom 1801
  - 1970 년도에 대중적으로 많이 쓰여 유명해졌음

#### Early Computer
- Based on mechanical **relays**
  - 1944 Mark 1: by Howard Aiken and IBM

  relay 방식이란 다음과 같은 방식이다.
  
  ```
  --B------------
       spring
       
       magnet
  --A------------
  ```
  
  위와 같이 용수철과 자석을 닿지 않게 떨어트린다. 이 때 A 에서 전류가 흐르면 자석은 전자석이 되어 용수철을 끌어 당기게 된다. 용수철이 끌어 당져서 자석과 만나면 전류는 자석에서 용수철로 넘어 흐를 수 있게되므로 B 에도 전류가 흐르게 된다.

  A 전류 공급을 차단한다면 자석이 전자석의 성질을 잃게 되어 용수철과 자석은 떨어지게 되며 따라서 B 에 전류가 흐르지 않게 된다.

  이러한 방식을 relay 방식이라고 한다. 전류가 흐르면 1, 아니면 0 인 이진법적인 방법과 똑같다.

- Based on vaccum tubes
  - 1945 ENIAC 최초의 "전자" 계산기

#### Personal Computer
- First used by hobbyists.


이제 강의 시간 다 끝나가니까 자기도 피곤하기 시작했는지 이야기가 이리 뛰고 저리 뛰고 널뛰기하기 시작한다.

- 컴퓨터 세대
  1. ENIAC
  2. ...
  3. ...
  ...

과거 청계천 세운상사

IC: Integrated Circit

Dos: Disk Operating System (Disk OS)

Internet
- 1969: 미국 아르파넷. 미국 내 각종 연구 결과 공유를 위해 구축되었음

protocol 통신 규약

embedded

miniaturization