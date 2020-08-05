
# 딥러닝을 이용한 일부인 비전검사 시스템
## 목적 및 목표
공장 라인에 설치된 비전인식 장치로부터 이미지 파일을 받아 일부인(날짜 도장)을 실시간으로 검사(PASS or NG)하는 시스템 개발

## 기대효과
- 365일 동일한 성능 보장
- 인건비 감소
- 높은 정확도
- 실시간 검사
- 빠른 속도

## 개발인원
- 3명

## 개발기간
- 2018.04~2018.09(6개월)

## 진행과정
  
  | 일시 | 내용 |
  |:------:|:------:|
  | 2018.04 | 역할분담 및 자료조사 |
  | 2018.05 | 필요 물품 조사 및 구매 |
  | 2018.06 | 전체 시스템 구성도 제작 |
  | 2018.07 | HW 구축 |
  | 2018.08 | SW 구축(서버, 모바일앱, OCR, 클라이언트 UI)|
  | 2018.09 | Testing/Debugging |
  
  
## 개발환경(전체)
  - MariaDB
  - Android Studio(모바일앱)
  - Visual Studio(서버)
  - Darknet(OCR)
 
<br><br><br>
   
## 역할
  - YOLOv2 기반 OCR개발
  - Testing/Debugging
  - H/W 부품 제작
<br><br><br>
   
## 시스템 구성

<img width="609" alt="default" src="https://user-images.githubusercontent.com/47843060/53254293-6f691580-3706-11e9-8b81-1708f20b1d92.png"/>
<img width="591" alt="default" src="https://user-images.githubusercontent.com/47843060/53254273-65dfad80-3706-11e9-82c0-c0add1780596.png"/>
<br><br><br>
 
##  시스템 동작 시나리오

- 전체 시스템 구성도
<img width="588" alt="default" src="https://user-images.githubusercontent.com/47843060/53254284-6bd58e80-3706-11e9-9a19-d03dd4ba1287.png"/>

- 전체 흐름도
<img width="588" alt="default" src="https://user-images.githubusercontent.com/47843060/53254296-71cb6f80-3706-11e9-9886-d7baabe83515.png"/>

1. UI를 통해 통과시킬 일부인을 설정한다.
2. 컨베이어벨트에 설치되어 있는 포토센서에 물체가 감지되고 영상이 캡쳐된다.
3. 캡처된 영상이 서버로 보내지고 일부인을 분석한다.
4. 설정된 일부인과 비교하여 2가지 상태로 구별을 한다.
  - 설정된 날짜와 같은 경우: PASS
  - 설정된 날짜와 다른 경우: NG
5. 모든 결과값들을 DB에 저장하고 UI에 띄워준다
6. NG일 경우 관리자의 모바일에 푸쉬알림을 띄운다.
7. 관리자는 모바일 앱을 통해 공장을 관리할 수 있다.
  

## 결과
- 학습데이터로 활용하지 않은 제품으로 300번 테스트한 결과, 평균 0.13초의 속도와 100% 정확도로 불량 검출
<br><br><br>
 
# 상세 과정(본인 역할)

## 알고리즘 선택
<img src="https://user-images.githubusercontent.com/47843060/89375300-5b617a00-d728-11ea-811f-d1aef7be8b38.png" width=80% height= 70%/>

<br><br><br>
 
## 데이터 수집
<img width="500" alt="yolo2" src="https://user-images.githubusercontent.com/47843060/53254316-7abc4100-3706-11e9-988d-41b43ba51f28.png"/>
<br>*텍스트에는 해당 이미지에서 추출할 부분의 위치값과 라벨값이 포함되어있습니다.<br>

- 제품의 종류별로 20개씩 수집 -> 총 100개(5종류)
- 7 : 3의 비율로 Train 셋, Test 셋 분할
- 직접 촬영으로 이미지 데이터 생성
  - 다각도로 촬영
  - 회전, 빛 조절 등으로 다양한 데이터 생성
- Labeling Tool을 활용하여 Labeling 수행
<br>
*BBox-Label-Tool 활용

<br><br><br>
 
## 학습 및 테스트
<img width="1000" alt="yolo4" src="https://user-images.githubusercontent.com/47843060/68098593-d62f0780-ff00-11e9-9b53-e53dea5cfed8.JPG">



    
