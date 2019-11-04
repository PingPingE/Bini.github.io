
*기업연계 프로젝트라 일부만 공개가능합니다.


<h1>딥러닝을 이용한 일부인 비전검사 시스템</h1>
<ul>
  <li>일부인이란?</li>
  <p>일부인은 연,월,일과 같은 날짜 정보
    <br>
    
  <li>기간</li>
  <p>2018.04.01 ~ 2018.09.30(6개월)</p>
  <br>
  
  
  <li>개발환경 및 언어(전체)</li>
  - MariaDB, YOLO, 안드로이드 스튜디오, Visual Studio
  <br>
  - PHP, C++, C#
  <br><br>

  
  <li>역할</li>
  - OCR개발<br>
  - TEST<br>
  - H/W 부품 제작
  <br><br>


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


    
