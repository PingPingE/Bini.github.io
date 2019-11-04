
*기업연계 프로젝트라 일부만 공개가능합니다.


<h1>딥러닝을 이용한 일부인 비전검사 시스템</h1>
<ul>
  <li>일부인이란?</li>
  <p>일부인은 연,월,일과 같은 날짜 정보</p><br>
  
  <li>목적</li>
  <p> 공장 라인에 설치된 비전인식 장치를 통해 생성되는 이미지파일을 서버에 저장하고 서버에서 <strong>불량이 발생했는지 실시간으로 확인</strong>하는 기술 개발</p>
  As-is | To-be | 기대효과
  ------ |------ |-----
  사람이 일일이 검사<br>인건비 증가의 부담<br>높은 불량률 | 항상 같은 성능 보장<br>인건비 감소<br> 높은 정확도<br>빠른 속도<br>실시간 | 실시간 정보 확인<br>최소 관리 인력 요구<br>불량 검출률 향상
  
    
  <li>기간</li>
  <p>2018.04.01 ~ 2018.09.30(6개월)</p>
  
  <li>일정</li>
  일시 | 내용
  ------ | -------
  2018.04 | 역할분담 및 자료조사
  2018.05 | 필요 물품 조사 및 구매
  2018.06 | 전체 시스템 구성도 제작
  2018.07 | HW 구축
  2018.08 | SW 구축
  2018.09 | Testing/Debugging
  
  
  <li>개발환경 및 언어(전체)</li>
  - MariaDB, YOLO, Android Studio, Visual Studio
  <br>
  - PHP, C++, C#
  <br><br>

  
  <li>역할</li>
  - OCR개발<br>
  - Testing/Debugging<br>
  - H/W 부품 제작
  <br><br>
  
  <li>결과</li>
    <ol>
      <li>UI를 통해 통과시킬 일부인을 설정한다.</li>
      <li>컨베이어벨트에 설치되어 있는 포토센서에 물체가 감지되고 영상이 캡쳐된다.</li>
      <li>캡처된 영상이 서버로 보내지고 일부인을 분석한다.</li>
      <li>설정된 일부인과 비교하여 2가지 상태로 구별을 한다.<br> -> 설정된 날짜와 같은 경우: PASS <br> -> 설정된 날짜와 다른 경우: NG </li>
      <li>모든 결과값들을 DB에 저장하고 UI에 띄워준다.</li>
      <li>NG일 경우 관리자의 모바일에 푸쉬알림을 띄운다.</li>
      <li>관리자는 모바일 앱을 통해 공장을 관리할 수 있다.</li>
    </ol>
  
  <br>

  <li>전체 시스템 구성도</li>
    <img width="588" alt="default" src="https://user-images.githubusercontent.com/47843060/53254284-6bd58e80-3706-11e9-9a19-d03dd4ba1287.png">
    <br><br>
    
<img width="609" alt="default" src="https://user-images.githubusercontent.com/47843060/53254293-6f691580-3706-11e9-8b81-1708f20b1d92.png">
<br><br><br>

  <li>전체 흐름도</li>
  <img width="588" alt="default" src="https://user-images.githubusercontent.com/47843060/53254296-71cb6f80-3706-11e9-9886-d7baabe83515.png">
<br><br><br>

  <li>서버</li>
    <img width="591" alt="default" src="https://user-images.githubusercontent.com/47843060/53254273-65dfad80-3706-11e9-82c0-c0add1780596.png">
    <br><br><br>

</ul>

<h2>딥러닝 알고리즘 : You Only Look Once (YOLO)</h2>
Yolo는 딥러닝 기반 객체 탐색 기법으로, 간단한 처리과정과 빠른 속도가 장점.
<br>
<h3>학습시킨 데이터(이미지, 텍스트)</h3>
<img width="300" alt="yolo2" src="https://user-images.githubusercontent.com/47843060/53254316-7abc4100-3706-11e9-988d-41b43ba51f28.png">
<br>*텍스트에는 해당 이미지에서 추출할 부분의 위치값과 라벨값이 포함되어있습니다.
<br><br>

<h3>학습시킨 후 생성된 weights 파일</h3>
<img width="300" alt="yolo1" src="https://user-images.githubusercontent.com/47843060/53254306-76902380-3706-11e9-967f-9754d15f9f3f.png">
<br>*weights파일은 대용량이므로 업로드 하지 못했습니다.
<br><br>

<h3>Test</h3>
<img width="600" alt="yolo3" src="https://user-images.githubusercontent.com/47843060/53254325-7d1e9b00-3706-11e9-9326-70120b666be9.png">
<br>*weights파일을 적용하여 test해보았습니다.


    
