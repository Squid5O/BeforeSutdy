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