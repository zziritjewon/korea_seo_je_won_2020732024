
for homework2
repository name is not available korean word, so my name wirtten "korea_seo_je_won"

# 5주차 제어공학

#### State Variables
푸는 과정에 있어서 어떠한 체계가 있었으면 좋겠다! >> state 도입
: 수식화할 때, system안에 state를 정의해서, 이 state를 중심으로 문제를 풀어보자 (단순 미방을 푸는 것이 아니라)
(state끼리도 관계가 형성이 되기도 함)
: 문제를 푸는 과정에 있어서 의미를 부여, 컴퓨터에게 일을 시키기 쉽게 식을 바꿔나가는 과정

방정식의 차수에 따라 state갯수 결정(2차미분>> state 2개)

2차미분을 간단한 1차미분 연립으로 바꿀 수가 있음(켬퓨터에게 시키기가 쉬움)

x1(t)를 커패시터에 쌓이는 전압으로 지정, x2(t)를 인덕터흐르는 전류로 설정(무작위로)
x1과 x2가 서로 항등식만 안되면 돼(서로다른 두개의 state이기만 하면 상관 없다)
예를 들어 직렬일 때 인덕터 전류와 저항 전류를 각각 x1 x2라고 잡으면 안된다.
예를 들어 직렬일 때 인덕터 전류를 X1, 저항의 전압을 X2라고 정하면 단순하게 R만 곱하는 관계가 된다.(두 STATE는 하나의 STATE와 같은 결과임)
>서로 독립적인 STATE로 설정을 해줘야한다.

??왜 우리가 STATE를 만들어야하는가??

>다차 미분방정식이 여러개의 1차미분방정식으로 쪼개진다. >라플라스변환으로 풀기 > 왼쪽은 초기상태가  파이티값에 의해 바뀐결과
     오른쪽은 INPUT이 파이티에 의해서 바뀐 결과물이 된다. 결과식 자체가 물리적 의미를 갖게된다.

STATE는 보통 벡터로 정의가된다. >> State vector(여러개의 state들로 구성)

# state differential equation
다차 미분방정식 >> 여러개의 1차미분방정식 >> 1차 행렬 미분방정식으로 바꾼 이 결과를~

그 state들과 input을 조합해서 output을 만드는 방정식 : output equation

위의 두가지를 묶어서 state space equation!!!!!!

>state라는 것의 의미가 부여, 따라서 중간과정에서 의미를 파악가능
>>식 자체가 1차행렬방정식이기 때문에 컴퓨터에게 시키기가 굉장히 쉬워진다.
결과식에서의 파이(t)를 state transition matrix라고 한다.


ss: state space equation풀어주는 매트랩 명령어
initial(sys, x0, [0,5]);  : 시스템의 이 초기값으로 [0,5] 0초부터 5초까지 시뮬레이션

