# 🛠️Software Engineering🧰

## 📖주제
> ## 좌석 확인 시스템,Seat to Sit(이하 StS)  
&nbsp; StS는 좌석을 활용하는 모든 시설의 빈자리를 파악하는 서비스입니다. StS는 각 시설의 CCTV를 활용하여 현재의 시설 영상을 통해 실제 가게의 좌석을 파악하고, 전체 좌석 사용 현황을 웹으로 보여줍니다.  

> ## Functional requirements  
* StS는 영상정보(CCTV)를 활용하여 자동으로 빈자리를 파악하여 시설를 이용하고자 하는 고객들에게 제공합니다.
* StS는 인공지능을 이용하여 좌석의 사용 여부를 단순한 사람의 유무가 아닌 실제 사람이 판단한 것 처럼 정확히 빈좌석을 찾아냅니다.(예: 잠시 비운 자리(화장실, 흡연 등)는 빈 좌석으로 취급하지 않음)
* StS는 현재 좌석정보를 간략화 하여 현재 빈자리가 어디있는지 보여줍니다.
* StS는 웹과 앱을 통해 좌석 정보를 제공해줍니다.
* StS는 사용자가 지정한 시설이 만석일 경우, 사용자가 원하면 빈자리 알림을 해줍니다.
* 빈자리 알람을 해준 뒤, 알람을 받은 사람이 예약을 원하면 그 빈자리에 대한 5분간의 짧은 예약을 해줍니다.
* 웹은 시설 검색 및 등록된 시설을 보여주고, 각 시설을 눌렀을때 선택한 시설에 대한 실시간 좌석을 보여줍니다.  

> ## Nonfunctional requirements  
* 서비스 대상은 좌석을 활용하는 모든 시설입니다.  
* 서비스 사용자는 시설을 사용하는 모든 고객입니다.  
* StS는 시설의 모든 좌석 정보가 담겨있는 영상 정보 제공만으로 서비스를 제공할 수 있어야 합니다.  
* 웹에서 확인한 좌석 상태가 실제 좌석 현황과 90% 이상 일치해야 합니다.  
* 가게 운영시간이 아닐때에는 사용자에게 운영시간이 아님임을 정확히 알릴 수 있어야 합니다.  
* 좌석의 배치나 수가 변경되었을때 웹페이지에 빠른 업데이트가 필요합니다.(업데이트 혹은 버전관리)  
* 가게 내부에 좌석을 확인할 CCTV가 있어야 합니다.(추가적인 하드웨어)  
  
## Use case Diagram  
![캡처](https://user-images.githubusercontent.com/54730375/93861515-98df8e00-fcfb-11ea-8dea-46482d25d029.PNG)  
  
## Use case Description  
  
Use case name | ShowEmptySeat
-- | --
Participating actors | Customer
Flow of events | 1. Customer 가 원하는 시설을 클릭하여 "ShowEmptySeat"기능을 실행한다.<br/>                2. STS는 해당 시설의 가장 최신 좌석 정보를   처리한다.<br/>                3. STS는 처리된 정보를 UI로 나타내어 웹 페이지에 송출한다.<br/>   4. Customer는 송출된 웹 페이지로부터 좌석현황정보를 얻는다.
Entry condition | 1. 해당 시설이 영업중이어야 한다.
Exit condition | 1. Customer가 앱(웹)을   종료한다.
Quality requirement | 1. "NoticeSeat"기능을 통해 최신 좌석 정보를 보유해야한다.   2. UI로 나타내어진 좌석 배치도가 실제 시설의 좌석 배치와 완전히 일치해야한다.
   
## Scenario  
Scenario   name | 점심식사 장소 찾기
-- | --
Participating   actor instances | 길동: Customer
Flow   of events | 1.길동은 여자친구와 2주년 기념일로 점심을 먹는 중이다. 그 후 여자친구가 평소에 가고 싶어 했던 유명한 디저트 카페를 가려고 계획 중이다.<br/>   2.길동은 STS ”가게찾기” 로 디저트 카페를 찾은 뒤 “좌석보기” 를 통해 디저트 카페의 좌석현황을 확인했다.<br/>   3.디저트 카페는 현재 모든 자리가 손님들로 채워져 있었고, 길동은   “빈자리알림받기” 기능을 통해 빈좌석 알림을 설정해 놓았다.<br/>   4.빈자리 알림이 받은 뒤 길동은 지정한 자리에 “좌석예약” 권한을 부여받은뒤 예약 후 디저트 카페로 출발하엿다.  



## 🤝역할 분담
| Participant | Roles | Skills | Traning needs |
|:---:|:---:|:---:|:---:|
|강승환| Backend, ML Developer | Programing: `Python, C, JAVA, Android`<br/>Framework: `Django` | UML, Tensorflow, OpenCV |
|김가영| Team Leader, Document Editor, ML Developer | Programing: `Python, C, JAVA`<br/>Socket programming | UML, Tensorflow, OpenCV |
|서우빈| Communication Developer, ML Developer | Programing: `Python, C, JAVA, Android` <br/>Socket programming, OpenCV <br/>Framework: `Django` | UML, Tensorflow |
|전종원| Frontend, Database Administrator, Configuration Manager| Programing: `Python, C, php, Html` <br/>SQLite | UML, JavaScript, CSS |
