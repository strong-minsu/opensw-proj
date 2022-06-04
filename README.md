# Mbti test project
https://majorbti.netlify.app/<br>

## 제안 배경 및 용어 설명
Mbti란 일상생활에 활용할 수 있도록 고안된 자기보고식 성격유형지이다. 특히 오늘날, MZ세대에서 대유행을 불러왔으며 인스타그램, 카카오톡 등을 활용해 공유하는 문화가 확산되어 크게 인기를 얻고 있다. 더불어, 코로나 시대로 인해 개인의 시간이 많아지면서 혼자 할 수 있는 간단한 테스트에 사람들의 관심이 크게 증가하였다. 이 테스트는 선택형 항목을 통한 사용자의 성격 분석을 요구하기 때문에 더욱 정교한 테스트 결과를 얻을 수 있다. 따라서 이러한 성격 유형의 테스트를 통해 자신이 어떤 사람인지 찾는 것에 우리 팀은 javascript을 이용하여 mbti테스트를 만듦으로써 간단한 심리테스트 서비스를 개발, 배포하고자 한다. 
테스트 대상은 단국대학교 학생들이며, 그에 따라 테스트의 주제를 “나와 어울리는 단국대학교 학과 찾기”로 선정하였다. 사용자(단국대학교 학생들)의 선택 항목을 분석하여 mbti를 찾고 어울리는 학과를 소개하는 것을 목표로 한다. <br><br>

## 시스템 기능(시스템에서 제공하는 기능 설명)
심리테스트 시스템의 기능을 대략적으로 나누어 보자면 아래와 같다.
1.   사용자에게 선택 항목 제공 (심리 결과 분석을 위한 질문)
2.   사용자가 선택한 항목을 통해 분석한 mbti와 mbti별 캐릭터, 그리고 어울리는 학과를 결과로 제공
    -   16가지의 성격 유형과 각 유형별로 3가지 이상의 학과 제공

### 페이지 디자인 예시
1. 테스트 시작 페이지
테스트 첫 페이지는 귀여운 시그니처 캐릭터와 함께 시작버튼으로 이루어진다.<br>
![image](https://user-images.githubusercontent.com/74875490/171296686-f3895e75-94c6-411d-a730-f8f0fcc1ba51.png)<br>

2. 항목 선택 페이지
테스트를 시작하면, 다음과 같이 사용자의 성격 유형을 분석할 수 있는 항목들을 보여준다. 사용자는 자신과 맞는 항목을 선택한다.<br>
![image](https://user-images.githubusercontent.com/74875490/171296814-39f999cb-04c4-4748-a557-4ef1161e9ff6.png)<br>
![image](https://user-images.githubusercontent.com/74875490/171297282-23095625-6bca-4c6c-a7bd-c6fa67ec1f7a.png)<br>


3. 분석 중임을 알리는 페이지
테스트 속 모든 질문에 응답했다면, 다음과 같이 어떤 유형인지 분석하는 창을 보여주며 결과 창으로 넘어가도록 설계할 예정이다.<br>
![image](https://user-images.githubusercontent.com/74875490/171877833-4ad19c3d-9732-4fd4-8f02-44f5b1ce84d3.png)
<br>

4. 분석 결과 알려주는 페이지
사용자가 응답한 결과에 알맞은 캐릭터를 내보내어 사용자의 특성을 알 수 있도록 한다. 주요한 특징들을 설명해주며, 아래의 사진과 같이 어떤 타입의 유형과 잘 맞고 그렇지 않은 유형은 어느 것인지 보여주기도 한다.<br>
![image](https://user-images.githubusercontent.com/74875490/171991542-85766bb4-4c5a-4600-8835-a1fc0461a4f6.png)
<br>

### 성격 유형별 추천 학과 정리
대략적인 설계는 위와 같이 진행될 예정이다. mbti 종류는 여러가지가 있는데, 이와 어울리는 학과들을 “단국대학교” 학과 내에서 모아 정리는 해보면 다음과 같다.<br>
![image](https://user-images.githubusercontent.com/74875490/168406663-56cd41f1-89b5-4ef8-84a3-d116a578d4c7.png)<br>
<br><br>

## 개발 일정 및 역할 분담
### 개발 일정
- 10주차
mbti 질문지 정리하기, 심리테스트 로직 설계하기, 우리 팀의 테스트 표지 디자인 개발하기
- 11주차
html, css, javascript를 이용한 웹 페이지 개발, 심리테스트 로직 구현하기
- 12주차
배포 및 추가 반영 사항 수정하여 테스트 구현 최종점검
- 13주차
내용 정리 및 발표 자료 정리<br>

### 역할 분담
![image](https://user-images.githubusercontent.com/74875490/168406748-4c4bf9db-3aae-4f14-9103-bb2f08164dff.png)<br><br>

## 구현
심리테스트 시스템의 기능을 대략적으로 나누어 보자면 아래와 같다.
1.   사용자에게 선택 항목 제공 (심리 결과 분석을 위한 질문)
선택지의 특성상 4지 중 하나의 항목을 선택해야 했다. 따라서 라디오 버튼을 이용해 이를 구현하였다. 일반적인 심리테스트 질문지 특성상 라디오버튼의 모양을 일반 버튼 모양으로 바꾸기 위해 CSS를 이용했다. 항목을 입력받아, 이후 javascript를 통해서 MBTI결과를 계산하는데 사용된다.
2.   사용자가 선택한 항목을 통해 분석한 mbti와 mbti별 캐릭터, 그리고 어울리는 학과를 결과로 제공
    -   16가지의 성격 유형과 각 유형별로 3가지 이상의 학과 제공
입력받은 항목값에 따라서 if-else문을 통해서 적절한 페이지로 연결되도록 구현하였다. 결과화면 페이지에는 다시하기 버튼을 넣음으로써 심리테스트 결과를 받아들이기 힘들 경우, 다시 테스트 받을 수 있도록 하였다.
3. 배포
https://www.netlify.com<br>
Netlify를 이용해 서비스를 배포하였다.
https://majorbti.netlify.app/<br>

## 참고문헌
MBTI 유형별 나에게 딱 맞는 학과는?! (tistory.com)<br>
지금 이대로가 좋아 나른하고 배부른 고양이 (myroutine.kr)