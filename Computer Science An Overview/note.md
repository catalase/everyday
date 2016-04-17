Computer Science: An Overview
=============================

- 담당 교수 송월봉
- 수업 시간 Fri at 1 PM A Week for 2 hours

MT 때문에 한 주 수업이 없었음

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

데이터를 서로 구별하게 하는 -- _유일한 값_~~을 **Key** 라고 부른다._

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

**Clock Pulse**  
규칙적으로 발생하는 펄스를 Clock Pulse 라고 부른다.  

**Impulse**  
불규칙적으로 발생하는 펄스를 Impulse 라고 부른다.

펄스가 발생하면 위로 올라가므로 **H**igh 라고 부르고,
아래로 내려가면 **L**ow 라고 부른다.

##### 종류
1. SR
2. JK
3. D _Delay_
4. T _Toggle_

## S-R
입력은 **S**, **R**, **E**(or C.K) 로 이루어진다.
S AND E, R AND E 가 latch 에 두 입력으로 주어지므로 E 가 0 이라면 아무 일도 안일어나며 1 이라면 단순 latch 와 똑같은 동작을 한다.

## J-K
### Characteristic Table
|J|K|Next Q|
|-|-|------|
|0|0|Prev Q|
|0|1|0|
|1|0|1|
|1|1|Toggle|

### Excitation Table
|Prev Q|Next Q|J|K|
|------|------|-|-|
|0|0|0|X|
|0|1|1|X|
|1|0|X|1|
|1|1|X|0|

## [D](D)
새 입력 D 에 대하여 J = D, K = NOT D 로 놓으면 된다.
가장 많이 사용되는 플립플롭

[D]: https://en.wikipedia.org/wiki/Flip-flop_(electronics)#D_flip-flop

### Characteristic Table
|D|Q|
|0|0|
|1|1|

## T
새 입력 D 에 대하여 J = K = D 로 놓으면 된다.

### Characteristic Table
|T|Next Q|
|0|Prev Q|
|1|Toggle Q|

## Hexdecimal Notation
진법은 영어로 Base, or Radix

Weight: 각 자리 수에 할당된 값

16 진수 표현을 사용함으로써 2 진수 표현을 짧게 표현할 수 있음.

2 진 표현 -> 16 진 표현 변환 알아두기
이를 확장해서 i < j 에 대하여 2 \*\* i -> 2 \*\* j 표현 알아두기
예: 0.1 = 0.10000...

## RAM _Random Access Memory_
### 메모리 접근 방법
1. Sequential _순차 접근_: 테이프와 같이 데이터 위치와 access time 이 비례한다.
2. Random Acesss: RAM. access time 이 상수 시간이다.
3. Direct: 디스크 헤드가 섹터에 접근하는 것과 같이 access time 에 차이는 분명하게 존재하지만 큰 sequential 보다 큰 차이는 없다.

> access time 이 상수 시간이면 map?

따라서 매우 빠른 속도가 요구되는 주기억장치에 random access 가 적합하다.

이제 어떻게 Random Access 를 구현할 수 있는가?

## Encoder
**하나의 입력**으로부터 **여러 개의 출력**을 만든다.

## Decoder
**여러 개의 입력**으로부터 **하나의 출력**을 만든다.

> 개인적인 생각으로 Encoder 보다 Decoder 가 더 설계하기 쉬운 것 같다.

디코더 심볼은 네모 박스 안에 D 라고 써놓고 입력으로 n 개, 출력으로 m 개로 가는 디코더일 때, n X m 이라고 쓴다.

### RAN 종류
1. D _Dynamic_: 내부에 콘센서가 있어 방전된다.
2. S _Static_: 플립 플롭을 사용하여 방전되지 않고 상태를 유지한다.

### ROM: Read Only Memory
전류가 흐르지 않으면 아무 쓸모 없으나 전류가 흐르기 시작할 때 내용이 살아난다.
마치 퓨즈 여러 개를 가져다 놓고 퓨즈를 끊어놓아 원하는 바이너리 배열을 만드는 것과 같다. 전류가 흐르지 않는다면 도저히 데이터가 되지 않겠지만 전류가 흘렀을 때 끊어지지 않은 퓨즈에서는 1 의 값을 띄게 되며 끊어진 퓨즈에서는 0 의 값을 뛰게 된다. 퓨즈의 연결을 전자기적으로 제어할 수 없으므로 이 정보는 영구적으로 변하지 않는다. 여기서 퓨즈를 끊는 것을 굽는다고 표현한다.

### ROM 종류
1. Mask: Read Only ROM. 우리가 흔히 아는 한번 W 하면 영구적으로 저장되는 ROM 이다.
2. P _Programmable_: 사용자가 ROM 데이터를 **한번만** 원하는 정보로 맞출 수 있다. 예로 공씨디가 있다.
3. EP _Erasable_: PROM 과 같으나 전자기적으로서가 아닌 자외선으로 지울 수 있다.
4. EEP _Electronic_: ROM 이나 전기적으로 RW 가 가능하다. 예로 USB 가 있다.

## Disk
보통 Disk 라 함은 Magnetic Disk 를 말한다. 왜냐하면 가장 많이 그리고 널리 쓰이는 Disk 가 Hard Disk 이니까!

hard disk 는 동심원으로 구분되며 동심원은 다시 트랙으로 나뉘고 track(트랙) 으로 나뉘고 track 은 다시 sector(섹터) 로 나뉘는데, sector 는 head 가 한번에 읽을 수 있는 구간이다.

## ASCII
7 bit 를 사용하여 문자를 표기하나 1 byte 가 8 bit 이므로 컴퓨터 메모리에서 표현할 때, 보통 맨 앞에 0 을 넣는다.

```
1 2 3 4 5 5 7
-----|-------
 Zone
      Numberic Zone
```

아스키 인코딩은 아무렇게나 대응 관계(encoding)를 정의한 것이 아니라 규칙이 있는데, 첫 세 비트를 `Zone` 이라 명명되어 있고, 나머지 네 비트를 `Numberic Zone` 이라 명명하고 있다.

### Zone
1 0 0 -> Alphabet Group 1
1 0 1 -> Alphabet Group 2
0 1 1 -> Number [0, 9]

Example: A -> 100 0001, C -> 100 0011

## EBCDIC
8 bit 아스키 코드 확장
아스키 코드와는 약간 다른 체계를 가지고 있다.

```
1 2 3 4 5 6 7 8
------|--------
 Zone |   BCD

1 1 upper case, number
1 0 lower case
0 1 special character
0 0 not assigned
    0 0 A - I
    0 1 J - K
    1 0 S - Z
    1 1 0 - 9
```

### BCD
10 진수 하나를 4 bit 로 표현하는 것을 말한다.
즉 다음과 같다.

```
10 = 0001 0000
192 = 0001 1001 0010
```

## 문자 표현
한글을 모두 완성형으로 표현할려면 몇 자가 필요할까? 19 * 21 * 28 = 11172 자가 필요하다.

## 숫자 표현
1. Binary Notation
  - Overflow
  - Truncation

> 2 진 체계를 사용하는 컴퓨터에서 Binary 표현 말고 다른 표현이 있나?

Weight 를 위에서 설명했었는데 Quantity 라고도 불른다.
참고로 덧셈에서 자리 올림 수를 Carry 라고 부른다.

## ALU
1. Adder 가산기
  1. Full adder
  2. Half Adder
2. Suber 감산기
  1. 보수 발생기 (1 의 보수, 2 의 보수)
3. Muler 증산기
  - shifter
4. Diver 제산기

여기서 놀라운 사실이 밝혀졌다. 가산기와 Binary Notation 만 적절히 사용해서 감산기, 증산기, 제산기를 모두 구현해낼 수 있다!

곱셈에 있어 곱해지는 수를 피승수라 부른다.
곱하는 수를 승수라 부른다.

### Adder
두 정수를 더할 때 첫번째 자리를 더하는 방법과 두번째 자리를 더하는 방법이 다르다. 왜냐하면 두번째 자리부터는 Carry 가 이전 자리로부터 올라오기 때문에 세 수를 더해주어야 한다. 이를 토대로 첫번째 자리를 구하는 Adder를 Half Adder라 부르고 두번째 자리부터는 Full Adder 부른다.

수업 시간에서는 Half Adder 를 구현하였으나 Full Adder 는 시간 관계상 구현해보지 않았으므로 해봐야 한다.

> 여기서 여담으로 모듈(또는 패키지) 제작에 반드시 필요한 
> 네 가지 기본 단계가 떠올랐다. 당연하게 보일수도 있으나 일단 써본다.
> 
> 1. 수학적 해석 (모델 고안 등)
> 2. 설계 (해당 분야에 직접 적용하여 구현)
> 3. 테스트: 여기서 실패하면 1번 또는 2번으로 간다...
> 4. 완성
> 5. 유지 보수
> 

#### Half Adder
두 입력 A, B 에 대하여

Sum S = A XOR B = A(NOT B)+(NOT A)B= **(A+B)(NOT AB)** = **(A+B)(NOT C)**  
Carry C = AB

위 식에서 주목해서 볼 부분은 굵은 글씨가 쳐진 부분이다. 약간의 조작을 통해 연산자의 갯수를 5 개에서 3 개로 줄였다! 연산자의 갯수와 게이트의 갯수는 같으므로 이는 곧 게이트의 갯수를 줄인 셈이다.

> 조금 더 나아가서 위 경우로 비추어 보아 우리가 왜 수학을 배워야 하는지,
> 그 이유에 한 가지 답이 될 수 있다. 수학적으로 행한 것이 단순히 추상적 사고에
> 그치는 것이 아닌 실제 세계에 반영된다. 이것은 실로 매우 놀라운 일이 아닐 수
> 없다.
> 
> 연산자의 갯수가 줄어들면 사용할 게이트의 갯수가 줄어들며 (더 정확하게 말해서 최대 게이트 수가 줄어든다)
> 이것은 설계에 직접적인 영향을 준다. 
> 직접적인 영향에는 다음과 같은 것들이 있다.
> 
> 1. 단가 감소 (제품 가격 감소)
> 2. 성능 향상
> 3. 크기 감소
> 4. 중량 감소
> 5. 전력 소비 감소: 유지 및 보수에 필요한 돈 절감
> 
> 대략 위의 장점이 있다.

## Binary Number Notation
1. Fixed Point Number
2. Floating Point Number

> Floating 을 한국어로 "부동" 이라고 번역했는데,
> 여기서 "부"는 아닐 부가 아닌 떠나딜 부를 의미한다.
> 사실상 to 부정사

### Compliment
1. R\`s
2. (R-1)\`s

> n 의 보수는 그 수의 음수 표현이다. - 송월봉 교수

#### (R-1)\`s
R-1 보수 시 덧셈 최상위 캐리값을 다시 최하위 캐리에 더하면 된다.

1 의 보수는 NOT 게이트에 통과시키기만 하면 바로 R-1 의 보수를 얻을 수 있다!

```
R-1 1010101 = NOT 1010101 = 0101010
```

#### R\`s
2 의 보수를 구하기 위해서는 1 의 보수를 구한 후 1 를 더한다.  
2's = 1's + 1

R 의 보수 시 최상위 캐리값은 그냥 버린다.


보수를 사용한 덧셈 시 최상위 부호 값이 잘못 나온다면 해당 덧셈은 오버플로우가 발생한 덧셈이다.
여기서 캐리값이 잘못 나왓다는 것은 더할 수 두 수의 부호 비트가 모두 0 이거나 1 임에도 결과 값의 부호 비트가 입력 비트의 부호값과 다름을 의미한다. 만약 두 입력의 부호 비트가 서로 다르다면? 오버플로우가 발생할리가 없다. 왜냐하면 -2 ** n + 2 ** n - 1 = -1 이므로 전혀 오버플로우가 발생하지 않는다.

> 오버플로우를 부정하다고만 봐야할 것이 아니다. 
> 오버플로우를 활용할 수도 있다!  
> 오버플로우가 발생한다면 그 수는 다시 제일 작은 음수로 
> 회귀하거나 제일 큰 양수로 회귀하므로 순환성을 가진다.
> 이러한 순환성 활용할 수 있다.

##### `0` 의 2 의 보수
0의 2 의 보수는 어떻게 처리해야 하나?

msb 가 1 이면 음수인 것을 활용하여 정하는 것이 나은 선택이다.

### Fixed Point Number
#### Signed Magnitude Method
MSB (Most Significant Bit) 가 수의 부호를 결정한다.
