Computer Science: An Overview
=============================

- 담당 교수 송월봉
- 수업 시간 Fri at 1 PM A Week for 2 hours

MT 때문에 한 주 수업이 없었음

# WEEK 4
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

# WEEK 5
#### 정보 표현 단위
```
Bit -> Nibble -> Byte -> WORD -> Field -> Record -> Block -> File -> DB
```

##### WORD
1. half word 2 byte
2. full word 4 byte
3. double word 8 byte

##### Field
###### Number, String Field 를 구별하는 방법
산술 연산이 가능할 때, Number 이며, 그 외 경우에 대해서는 문자이다. 
예로 아파트 206 동을 표현하기 위해 206 만 쓴다고 할 때, 206 은 숫자로 취급하는 것 보다 
문자로 취급하는 것이 더 나은 선택이다.

상징적인 표현으로 Enter 를 눌러 한 줄 삽입할 때 마다 하나의 `Record` 가 생성되었다고 본다.
즉 Enter 는 `Record` 를 구분해준다. 따라서 여러 Enter 가 포함되어 있는 것을 File 이라 부른다.

##### Block
다루기 용이함 등을 위한 데이터 표현 단위로써, 파일의 부분 집합을 말한다.

##### DB
어떤 `DB` 는 Databank 라고도 불리는데, 여기에서 Bank 는 불특정 다수가 이용할 수 있는 시스템을 상징한다.
따라서 공공 데이터베이스같은 경우는 Bank 의 상징적인 의미를 차용하여 Databank 라고 부르기도 한다.

#### Abstraction

숫자 0 과 알파벳 O 를 구분하기 위해서 숫자 0 중간에 선을 하나 긋기도 한다.

#### Byte
하나의 문자를 표현하는 비트 묶음을 의미하며 다음 세 가지가 후보가 될 수 있다.

1. 6 Bit: 특별한 목적으로 사용된다.
2. 7 Bit: ASCII
3. 8 Bit: EBCDIC

그런데 표준은 3 번 8 Bit 이다.

**DBCS**: Double Byte Character System
**SBCS**: Single Byte Character System

데이터를 서로 구별하게 하는 ~~_유일한 값_~~을 **Key** 라고 부른다.

> 위에서 _유일한 값_ 이라고 쓰긴 했는데,
> Unique Key 도 있으므로 이 부분은 지우는 것이 맞는 것 같다.

각 문자를 입력하는 기계는 각 문자를 고유하게 구별해주므로 Keyboard 라 부른다.

> 억지 아닌가?
> 
> 편리함을 위해 키보드에 같은 키(Shift, Ctrl, Alt, etc)가 양 쪽에 두개식 있기도 한다.

#### Boolean Operation
1. AND
  
  Dot 으로 표기한다.

2. OR

  + 으로 표기한다.

3. NOT
  
  Prime 또는 위 쪽에 줄을 긋는다.

4. XOR

  (+) 으로 표기한다.

5. Buffer
6. NAND
7. NOR
8. XNOR

Gate 또는 Switch 라고 부른다.

트랜지스터 하나가 하나의 스위치 역할을 한다.

위 각각의 회로 표현을 알아둔다. NOT 의 트랜지스터를 이용한 회로 구현을 알아둔다.

#### Logic circuit
1. **conbinational**

  AND, OR, NOT 만을 사용하여 만들었다면 조합 논리이며,
  메모리 기능이 없어 **비트를 저장할 수 없다.**
2. **sequential**

  Flip-Flop 을 사용하여 만들었다면 순서 논리이며
  메모리 기능이 있어 **비트를 저장할 수 있다.**

#### Flip-Flop _Latch_
> Flip 뚝 - Flop 딱 뚝딱 뚝딱

A circuit built from gates that can store one bit.
- 하나의 라인은 1 을 저장한다.
- 다른 하나의 라인은 0 을 저장한다.
- 두 라인이 모두 0 이라면 최근에 저장된 값이 보존된다.

간단하게 말해서 RAM 은 Latch 로 구성되어 있다.
어떻게 작동하는 지 알아둔다.
  

##### 종류
1. SR
2. JK
3. D
4. T