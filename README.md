# 🛠️Software Engineering🧰

## 📖주제
> ## 좌석 확인 시스템,Seat to Sit(이하 StS)  
&nbsp; StS는 좌석을 활용하는 모든 시설의 빈자리를 파악하는 서비스이다. StS는 각 시설의 CCTV를 활용하여 현재의 시설 영상을 통해 실제 가게의 좌석을 파악하는 서비스 입니다.  

&nbsp; StS는 영상정보(CCTV)를 활용하여 자동으로 빈자리를 파악하여 시설를 이용하고자 하는 고객들에게 제공한다. StS는 인공지능을 이용하여 좌석의 사용 여부를 단순한 사람의 유무가 아닌 실제 사람이 판단한 것 처럼 정확히 빈좌석을 찾아낸다.(예: 잠시 비운 자리(화장실, 흡연 등)는 빈 좌석으로 취급하지 않음) StS는 현재 좌석정보를 간략화 하여 현재 빈자리가 어디있는지 보여준다. StS는 웹과 앱을 통해 좌석 정보를 제공해준다. 또한 사용자가 지정한 시설의 빈자리 알림을 해준다. 웹은 시설 검색 및 등록된 시설을 보여주고, 각 시설을 눌렀을때 선택한 시설에 대한 실시간 좌석을 보여준다.  

> ## Quality requirements  
* 서비스 대상은 좌석을 활용하는 모든 시설이다.  
* 서비스 사용자는 시설을 사용하는 모든 고객이다.  
* StS는 시설의 모든 좌석 정보가 담겨있는 영상 정보 제공만으로 서비스를 제공할 수 있어야 한다.  
* 웹에서 확인한 좌석 상태가 실제 좌석 현황과 오차가 없어야 한다.  
* 가게 운영시간이 아닐때에는 사용자에게 운영시간이 아님임을 정확히 알릴 수 있어야 한다.  
* 좌석의 배치나 수가 변경되었을때 웹페이지에 빠른 업데이트가 필요하다.(업데이트 혹은 버전관리)  
* 가게 내부에 좌석을 확인할 CCTV가 있어야 한다.(추가적인 하드웨어)  

## 🤝역할 분담
| Participant | Roles | Skills | Traning needs |
|:---:|:---:|:---:|:---:|
|강승환| Backend, ML Developer | Programing: `Python, C, JAVA, Android`<br/>Framework: `Django` | UML, Tensorflow, OpenCV |
|김가영| Team Leader, Document Editor, ML Developer | Programing: `Python, C, JAVA`<br/>Socket programming | UML, Tensorflow, OpenCV |
|서우빈| Communication Developer, ML Developer | Programing: `Python, C, JAVA, Android` <br/>Socket programming, OpenCV <br/>Framework: `Django` | UML, Tensorflow |
|전종원| Frontend, Database Administrator, Configuration Manager| Programing: `Python, C, php, Html` <br/>SQLite | UML, JavaScript, CSS |
