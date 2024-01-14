# befostudy
myself


2023.12.28~2024.1.12 수업 정리

-----
.editorconfig 파일에 추가할 내용

[*]
charset = utf-8-bom 
---- 한국어 관련 문제 해결


---01 코딩---
코딩-
: 인간이 컴퓨터에게 명령을 내리는 것(언어)

문법적인 측면
-	자료형과 변수
Int : 정수형 -10 -5 0 1 2 3 1000
float : 실수형 -2.87f 0.0f 5.2f
bool : 논리형 true false
FString : 문자열 TEXT(“이영훈”)
-	조건문
if / else if / else => Branch
switch case 
-	반복문
for => for each
-	함수
Function 기능: 착즙기, 입력/출력
-	클래스
:사용자정의자료형


논리적인 측면
: 순서를 세우고 그것을 차례대로 배열하고 각 각 논리적으로 해결한다.
-> 알고리즘 Algorithm

블루프린트 노드의 구조와 제어 흐름
변수와 함수
조건문
반복문
함수
클래스와 객체지향 프로그래밍

객체지향 프로그래밍(Object Oriented Programming)

상속성
추상화
캡슐화(은닉화)
다형성

언리얼 엔진의 라이프 사이클 함수


--------------------

02 슈팅-블루프린트

슈팅 블루프린트

슈팅 프로젝트 환경 구성
-	프로젝트생성
-	레벨 생성
-	게임모드생성
-	기본Pawn생성해서 게임모드에 적용
-	프로젝트세팅 Maps&Modes 에서 기본 게임모드와 기본맵으로 해당 레벨을 설정
플레이어 이동
-	어디다가 코딩을 할 것인가?(시점)
-	이동공식 P = P0 + vt
-	현재위치 = 이전위치 + 속도(방향 * 크기) * 시간
-	Vector의 합

Tail 제작 (Vector의 차)
Vector 의 이해 및 활용
총알 제작 및 이동
총알 발사하기 (SpawnActor를 이용한 동적생성)

자동총쏘기
적 제작
추첨을 통한 적의 진행방향 처리
충돌 처리
https://www.unrealengine.com/ko/blog/collision-filtering
폭발 VFX(Visual Effects) 처리

Enemy Manager 만들기
DestroyZone 제작하기

외부 모델링으로 교체하기
이동방향으로 회전

배경 스크롤(UV좌표 애니메이션)
점수 UI 제작 (Viewport)
플레이어 체력 (WidgetComponent)
게임 오버 UI 제작
실행 파일로 패키징하기

-----------------------


03  C ++ 

1.	프로젝트 생성과 빌드 (컴파일과정)
2.	자료형과 변수
3.	포인터 변수, 레퍼런스 변수
4.	배열 (배열, 리스트(STL vector))
5.	조건문
6.	반복문
7.	함수
8.	클래스
a.	생성자, 소멸자
b.	생성자 Overload
c.	Override : 부모의 함수를 재정의 해서 사용할때 
d.	가상함수 (Virtual) : 부모함수만들때, 자식이 재정의 가능함 이라는 의미이다.
e.	순수가상함수
f.	추상클래스 : 인터페이스
g.	this (포인터변수, 객체가 자신을 지칭)
h.	상속


--------------------------

04 C++ ,블루 프린트, 슈팅

슈팅 C++

[]
1.	프로젝트 생성과 빌드 (컴파일과정)
2.	로그출력 (Hello World)
3.	자료형과 변수
4.	UPROPERTY()
5.	조건문
6.	반복문
7.	배열 (TArray, TMap)
8.	함수
9.	UFUNCTION()
a.	BlueprintCallable
b.	BlueprintPure
c.	BlueprintImplementableEvent
d.	BlueprintNativeEvent
10.	클래스
a.	UClass
b.	CDO (Class Default Object)
c.	생성자의 역할





[프로토타입]
프로젝트 생성 및 카메라와 조명 설치
BP_Player 
꼬리 만들기
BP_Bullet 
플레이어 총쏘기
총알 사운드처리
자동 총쏘기
적 생성하고 이동처리(30%확률로 플레이어방향, 나머지 확률로 앞 방향)
충돌하기 (Actor 기반)
충돌하기 (Component 기반)
Bullet과 Enemy의 충돌
Enemy와 Player의 충돌
C++에서 충돌설정 하기
폭발 사운드처리
BP_EnemyManager
BP_DestroyZone
배경 스크롤

[알파]
외부 모델링으로 교체
폭발 이펙트
점수처리 (UI)
최고점수처리 (UI) 
마우스 커서 처리, Input Mode
게임오버 시 일시정지 시키기
게임오버 (UI)
[베타]
플레이어 체력 (UI)
최고점수 저장하기/읽어오기 (파일 입출력)


----------------------------



2D슈팅게임 완성









-------------------------------> 노트 정리

리슨 서버(언리얼 네트워크)

미드저니 달리3 스테이블디퓨전(무료)

제안 기획 - 프로토타이핑 - 프로젝트 착수 - 개발 - 알파 - 베타 - 결과물

y 좌 우    그린  
x 앞 뒤    레드
z 위 아래  블루 

1유닛 = 1cm (언리얼기준)

기즈모 = 그시기

StaticMesh

vertex(정점) - 3차원 공간의 점 

edge(선) - 3차원 공간의 선 

폴리곤, 페이스 , 서피스 (면) - 3차원 공간의 면

삼각형 + 삼각형 = 사각형
폴리곤 + 폴리곤  = mesh

렌더링(표현한다)

머터리얼 에디터 - 비주얼 스크립팅


-
오브젝트 = 객체

코드의 문법 측면 
- 자료형과 변수
- 조건문
- 반복문
- 함수
- 클래스 - 언리얼의 액터

boolean => true or false 2진수 논리형
byte = 8비트 넘버(정수)
integer = 정수형

floeat = 실수
string = 문자열

int ; 정수형 -10, -5, 0 1 2 3 5 6 7 11
float : 실수형  -2,87f, 0.0f, 5.2f
bool : 
boolean : 논리형 = true , false 
FString : 문자열 "오자이슨"

FString : 문자열 TEXT(""오재승"") - 언리얼 C++
-

변수(val) : 데이터 집어넣기 (데이터를 넣는 그릇)

클래스도 일종의 자료형

조건문
if / else if / else = > branch
seitch case 
반복문
 for => for each , while 
함수
-Fuction 기능 : 착즙기, 입력/출력
 - 글로벌(전역변수) , 로컬(지역변수), 맴버변수
언리얼은 전역변수 없다능.

함수 스페이스?

클래스 - 속성, 기능

클래스는 하나지만 그 내부에 객체 많이 만듬

-


Level <- game mode base 

포제스(빙의) pawn에 빙의 f8 누르면 빙의 및 탈출


월드= 레벨

블루프린트 클래스

아이템 라벨에 있는거 - 인스턴스

콘텐츠 드로워에 있는건 클래스 그걸 밖으로 꺼내면 아이템 레벨에서 인스턴스
변수는 메모리 공간에 만들어짐 

변수
 ㄴ 오브젝트 - 역활(객체) - 친구, 아빠
 ㄴ 인스턴스 - 메모리 공간에 존재하는 것.

오재승 - 인스턴스
 ㄴ 집에 가면 아들, 친구랑 만나면 친구 - 객체 

화면에 보이면 액터

언리얼에서 보이는 오브젝트(객체) -> 액터
    ㄴ - > 그 안에 든 여러 객체 _ 컴포넌트 (구성 단위)
    ㄴ - > 그 외는 변수


ACTOR
 ㄴ rootComponet
      ㄴ comp
          ㄴ comp?

transform? 변환할수 이쓴ㄴ것
로케이션 릴레이션 스케일

위계구조(하이라키ㅣ)
---------------------------------------
event BeginPlay _ 생성될떄 한번
event ActorBeginOverlap -  겹칠때? 충돌?
evnet tick - 주기적으로

pin 

실행핀 > 
출력핀 o(오른쪽)
입력핀 ㅇ(왼쪽)

각 사각형은 함수 = 노드 

은닉화(캡슐화)

겟 - 가져오기
셋 - 집어넣기

추상화(모델링)

상속

다형성 - 오버로딩, 오버라이딩

녹색 ingtger
초록 float 

중간노드 컴포트?(변환)

부동소수점 연산 오차? 

== 비교 연산자

논리 연산자 &&  ||

------------
포윈드   
-----------
인클루시브 - 포함
엑스클루시프 -비포함

-

함수는 구현! 실행은 호출!

전체는 클래스!

함수 3단계
선언 Declare
정의(구현)
호출 Call

---------------------

클래스 - 객체지향 프로그래밍

변수(데이터)_바꿔서 넣을 수 있는 공간  <=> 상수(고정된)

자료형

컨버팅(자료 변환) 

컨버트 노드 int(수) 를 string(문자열)로 

폴 루프

펑션 = 착즙기

클래스   = > 자료형  -> 변수 -> 객체(오브젝트) - > 인스턴스
(
속성 : 변수  = 맴버
기능 : 함수  = 메소드
)

---------------


변수는 메모리 공간에 만듬 - > 인스턴스(오재승)
객채는 역활? 오재승(인스턴스)은 위치에 따라 남편 아버지 직장인 친구 등으로 바뀜(오브젝트) 

논리적인 측면 
: 순서를 세우고 그것을 차례대로 배열하고 각 각 논리적으로 해결 - > 알고리즘 (문제해결능력)

---
조건문
반복문
함수
클래스와 객체지향  프로그래밍(Object Oriented Programming)

부모자식- is a ( 참조?)
플레이어 플레이블캐릭터 - has a  (소유) 
인터렉션(상호작용?_)

객체지향 4대 특징
-상속화
-추상화
-캡슐(은닉)화
-다형성

언리얼 엔진의 라이플 사이클 함수 (소프트웨어 객체 생애 주기?)

액터!
tick(업데이트되면서 계쏙 호출됨)
hit overrap?(물리적 충돌? 겹처짐!)

------------------------


3d (디멘션) 3차원 
axis - 축 
up forward back

ctrl-space = contentDraower 올리기

액터 -> 폰 -> 캐릭터  상속 순서
상위 클래스 

possessed(빙의) - 폰  
직립 보행 -캐릭터

언리얼 단위 = Cm

Orthographic _ 2D
Persipective -3D

auto Activate for Player = -0번 플레이어 (기본)

럭스- 루멘

플레이어 이동
- 어디다가 코딩을 할 것인가
- 이동공식 P = P0 + vt
-        현재위치 = 이전위치 *속도(방향*크기)*시간

P = P0 + velocity(dir*speed)*deltaSecond(t) 
 delta(순간)

-----------


= 대입 연산자

Vector 방향 x 크기  ->     (스칼라 포함) 위치는 상관 없음
Scalar 크기            .     (방향이 없으면 스칼라)

velocity 속도

---------------
p = p0 + vt  (등속도공식)

    ->   ->
v = v0 + at   (가속도공식)   a = 엑셀레이션(가속)

F = ma (힘 공식)
힘 = 질량x 가속도
--------------
deltaSecond (순간) = > C++ 에선 델타타임
FPS
공평해지기위해 트랜스폼?

펑션 함수

바인딩(묶다) _ 기능(함수)를
입력 
ㄴ action (단발성)
ㄴ axis (장발성?)
 축
A 버튼을 누르면 -1
D 버튼을 누르면 1 
아무것도 안 누르면 0 
 = Engine input 

입력은 포제스된 폰이 받을 수 있다능

horizontal -Y (좌 우)
Vertical - z ( 위 아래)
x (앞 뒤)

make vetcor

단위백터(노멀라이즈) 단위 1

C제곱 = A제곱 + B제곱  (피타고라스) = 루트2 = 약 1.4

이벤트[event] - 틱으로 활용 불가능 (inputAxis)
벨류[get] - 틱으로 연결해서 사용 (get)



메이크 백터 _동서남북
right up x pin _ 머리위?


백터의 합 _ 마이너스

Cross 방향 곱?

---
메이크백터 방향 바꿔도 위아래좌우 방향 그대로(절대좌표)
up rigth 물체 방향 바꾸면 위아래 좌우 뱡향 바뀜 (상대좌표)
dot _ 스칼라곱?
......

음원 추출할떄 
asset action - export

Migrate - 복사 복붙

API , 플러그인 활용

SDK

API 핸드폰(함수), SDK - 그외 부수자재(충전기) 포함, 플러그인은?'

프렉처- 클레스터(쪼개기)

레벨 합치기?

퍼시스턴트 레벨

change Streaming Method

레벨만 따로 저장

 <> 내부
"" 내가 만든건 

h 헤더에 선언
cpp 소스에 구현
메인에 호출 작성

namespace std
using namespace


컴파일이란?

듀플리케이트 복제
디플리게이트 삭제

Spawn - 액터를 레벨에 만들어낼떄

Trasnlate

카멜 파스칼 스네이크 

 - 파스칼이 가장 대중적(C++문법식 하나로 통일)


........................

큐브도 충돌체를 가지고 있다능

원본 소멸?

충돌체 설정해서 콜리션 눌러서 다 벽 만들쟈

함수에서 Sweep


lifespan

ALT 누르고 선 클릭하면 블록 떨어짐 


메모리 LEAK 을 방지하기 위해 destory zone 필요

메모리 블록

메모리 SLC, MLC, TLC/?

정반사광, 물리기반 렌더링

차폐 (ambinet Occusiatn>)?{

노멀라이즈  = 백터의 크기를 1로 바꿈 



법선 백터 - 빛 반사 계싼?

roughness = smoothness


----------------------

레퍼런스의 개념
이름 지니는 대상에 별명을 붙여주는 행위

구조체가 아니라 클래스(Class)
클래스 = 멤버 변수 + 멤버 함수
변수가 아니라 객체(Object: 완전한 대상체)

구조체의 유용성
관련 있는 데이터를 하나의 자료형으로 묶을 수 있다. 
따라서, 프로그램의 구현 및 관리가 용이해진다.

디폴트 복사 생성자
사용자 정의 복사 생성자가 없을 때 자동 삽입
멤버 변수 대 멤버 변수의 복사를 수행
CopyCon2.cpp, CopyCon3.cpp

디폴트 복사 생성자 복사 형태
얕은 복사(Shallow Copy)!

Static Mesh (스태틱 메시)는 비디오 메모리에 캐시되고 그래픽 카드에서 렌더링할 수 있는 폴리곤 세트로 구성되는 지오메트리 조각


--------------------
collisiosn (충돌) 프로젝트 설정 _ 관계설정

오늘은 UV애니메이션 (스크롤) 할거얌

나나이트?

머테리얼 도메인을 서페이스->유저인페이스로 수정 _ BG

UV느 ㄴ뭘까? 매쉬에 머테리얼을 입히는것?/?
 UV = 
사각형이 있으면 가로를 U 세로를 V

UV맵핑 _ 위키피디아

offset? 

BG-_mat
--- UV 애니메이션

tex Coord, Panner(예를 통해 움직임) _ x 가로 y 세로

림라이트? Rrim Light, 프레넬 효과 ,,픽셀 

RGB 0 하얀색 ~ 255 검은색 0 ~ 1

적용해도 어두웠따가 다시 밝아짐. - 오토 익스포져. <- 요거 꺼야함

----------------------------------
인덱스 컬러? bgP>???

OVER FLOW방지를 위해 INT를 자주 쓴다


유저인터페이스- 슬레이스 위젯 스타일 _코딩으로 직접 만드는 Ui - 옜날 스타일
위젯 블루프린트 가즈아 - 유저 위젯을 상속

레터박스

위젯- 변수 연결 ( 바인드) - > 함수 연결을 의미

cast로 변신

점수는 불렛에서 올린다

HP 만들기
--
slot 앵커 스트레치 0000



int HP=9;
int MaxHP = 10;

float? invetor 해야함

색깔에 함수 넣지마라!

절두체?

레스트라이즈? 랜더링 파이프라인 

------------------------
MS : DirectX(DX) - Windows 전용
크로노스 그룹 : OpenGL - OpenGLES2.x - vulkan
애플 : ?

크로스플랫폼

hP player 에서 health bar 위젯은 로케이션이 없다. (로컬스페이스x ) _/ > 월드 스페이스값을 따라감 -
 ㄴ 비행기 로컬은 있음



-------------

Blur 블러
background blur

widget -> palette -> blur

버튼 클릭_ 인터랙션 -> detail - > is Variable -> 변숨만듬

quit preference - > quit(진자 종료), ->background(아래로감)

게임인스턴스는 삭제 안됌 !

 Z Buffer ( 덱스 버퍼?)  - > blueprint add to Viewport - > Zorder - > 순서

inputMOde
1.game
2.ui

플레이어 사망시 get playerPawn 불러올수 없어서 에러 

윈도우 빌드

사운드?! wave- 언리얼 자체 압축

푸리에 무한급수 FFT(패스트 푸리에 변환)

뉘앙스 

포인터? * _ 크기거 고정되어 있음 . 주소값을 집어넣음

포인터 레퍼런스는 원본을 바꿈
void -아예 없다. null_비어있는 공간 사용(용량차지) 
포인터는 ? 배열과함꼐

--------------------------

v.at?
stack? _ 자료구조 - > 배열 -> 리스트 - > 해시 -> quere , stack, tree , graph, 데이터 변수

변수 -일반
	ㄴ 포인터
	ㄴ 레퍼런스
STL(스탠다드 테이블 라이브러리)

C++ 백터 클래스

알고리즘 

code
-----
data
-----
heap    - 동적 생성 변수(new),  사용자가 사용하고 싶을떄 씀, delte 시 반환
-----
stack    - 지역 변수가 만들어지는 메모리 공간 , 함수 호출시 할당, 노출시 반환?

malloc 메모리 할당?

언리얼은 스마트 포인터 사용

////////////
#include <iostream>

using namespace std;

//배열 : 연속된 메모리 공간을 할당받은 변수의 목록
  // ㄴ 장점: 리스트 보다 접근 속도가 빠르다.
  // ㄴ 단점: 삽입/삭제가 불편함
int main()
{//함수 안에 있는 변수는 다 지역변수

	int array[5]; //정적

	array[0] = 10;

	int* pArray = new int[5]; //동적 //이름 없는 메모리 5개 주소를 옮겨줌, //*포인터

	pArray[0] = 10;

	if(pArray != nullptr)
		delete[] pArray;//배열 파괴
}

///////////////////////////////////////////////////

넣는거 push, 뺴는거 pop
psuh_Back -> 마지막에 넣어줌

스택_드럼통
큐는 막대?


///////////////////////////////
#include <iostream>
#include <vector>

using namespace std;
//리스트
int main()
{
	vector<int> v;//자료형

	v.push_back(true);
}
//////////////////////////

i += 1; //복합 대입 연산다
i++; //증감 연산자


////////////////#include <iostream>
#include <vector>

using namespace std;


//반복문
int main()
{
	const int size = 10; // 상수 선언. 상수는 쓰기 금지 온리 읽기만! //포인터 변수에 저장.

	int ar[size]{ 0 }; //변수는 상수로 사용 못함.

	for (int i = 0; i < size; i++) {
		cout << ar[i] << endl;
	}

}
/////////////////////////////////

---아스키문자

---------------------클래스

public , pritavte

선언 없으면 기본 public

생성자 함수? // consturce 

this 는 객채를 의미, 자기 지칭 - >

//overlodading 함수중복 ?

/////////////////
#include <iostream>
#include <stdio.h>

using namespace std;

class 동물
{
public:
	int 이름;
private:
	int 나이;
protected:
	int 재산;

public:
	void 짖다() {
		cout << "으르릉";
	}
};

class 고양이 : public 동물
{
public:
	//재정의 override 오버라이드
	void 짖다() {
		동물::짖다();
		cout << "야옹";
	}
};

//반복문
int main()
{ 
	고양이 냥냥이;
	냥냥이.짖다();

}
//////////////



-----추상 클래스 : 인터페이스

큰쪾에서 작은쪽의 캐스팅은 다이죠오부 : 동물 -> 고양이  반대는 성립x

.......----------------------------------------------------------------------------

토마토 비쥬얼 어셋 

Coding - codingMap new level 만들어

gamebasemode 는 레벨이 끼운다

CodingGameModeBase 

codingPawn

디폴트 폰 클래스

월드셋팅 -gamemode override


c++ codingPawn.h - #pragma once? 무엇을 방지?

UCLASS() 함수명

버츄얼_가상함수 _ 아무나 상속 가능

ACodingPawn? 이름

생성자는 존재?
태어나는건 beglin play

라이브코딩! 언리얼에서 항상! - > 끄고 제네레이트- > 시발 파일 사라짐

빌드 - 컴파일+실행

C++ A, U는 언리얼 코딩 규칙 접두사(명명규칚)

오브젝트 -> 액터 -> 폰 상속 순서

언리얼 빌드툴 , 헤더툴

헤더 인클루드 제네레이터 헤더가 젤 밑에 있어야함
헤더가 언리얼과 C++을 연결

ctrl+space  , ctrl+shift+space

C++ 서식문자

한국어 쓸려면 헤더 파일 인코딩 바꿔서 저장


프로젝트 - > 추가 - >edieter coding ->  w저장 _> "[*] chareset = utf-8-bom" 을 root=true 아래로 복사


////////////////////
//cpp
	UE_LOG(LogTemp, Warning, TEXT("Hello World!!"));
	
	UE_LOG(LogTemp, Warning, TEXT("number : %d, pi : %f"), number, pi);

	UE_LOG(LogTemp, Warning, TEXT("isOK : %d"), isOK); //false 0 아니면 다 true

	UE_LOG(LogTemp, Warning, TEXT("myName : %s"), *myName);  // 포인터 주소 값


////   h
public:
	int32 number = 0;
	float pi = 3.14f;
	bool isOK = true;
	FString myName = TEXT("ohjaweng");
//////

---------------------------------------------------


인헤리티드 inherited = 상속성
UPROPERTY
(Edit / Visible) + (Anywhere/ Defaults / Instance) 어디에서나 수정 or 볼 수 잇께

F11 디버그

tset은 하나만 들어감


ㅡ종료ㅡ 1.14 굳