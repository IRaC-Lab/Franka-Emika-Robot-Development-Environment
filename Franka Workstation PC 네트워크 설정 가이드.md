이 문서는 Franka Emika Panda robot을 제어하기 위해 Server PC의 네트워크 환경을 설정하는 과정을 설명한다.

### 로봇 설정
---
1. Franka Emika Panda robot 메뉴얼[^1] 중 장착및설치 안내에 따라 로봇을 안전하게 설치한다.
2. PC(운영체제 상관없음)의 이더넷을 DHCP로 설정한다.
	1. 로봇 설정 시 사용할 PC는 Server PC와 달라도 상관없다.
3. 로봇암(제어기아님)의 이더넷 포트와 PC의 이더넷 포트를 랜케이블을 사용해서 직접 연결한다.
4. PC의 이더넷 설정에서 IP를 할당받았는지 확인한다. (예: 192.168.0.11)
5. 웹브라우저(크롬 추천)를 실행하고 주소창에 <u>robot.franka.de</u> 입력 후 엔터키를 누른다.
	1. 보안되지않은 사이트라는 경고가 나와도 무시하고 접속한다.
6. Username과 password 를 생성한다.
7. 네트워크 설정에서 Shop Floor network의 DHCP를 비활성화하고 나중에 server PC와 직접 연결하기 위해 IP와 netmask를 설정한다.(예: Server PC IP: 192.168.0.2, Shop Floor IP: 192.168.0.22, netmask: 255.255.255.0)
	1. 펌웨어를 업데이트하기위해 인터넷에 연결되어야 한다면 Shop Floor network를 DHCP로 설정하고 제어기의 인터넷 포트와 공유기를 랜케이블로 연결한다.
	2. 왼쪽의 Frank World 메뉴에서 online 상태가 되면 펌웨어를 업데이트 할 수 있다.
8. End effector가 설치되어있다면 end effector까지 설정후 로봇 설정을 마친다.

### Workstation PC 네트워크 설정
---
1. 로봇 제어기와 PC(OS:Ubuntu)를 랜케이블로 직접 연결한다.
2. Ubuntu의 네트워크 설정에서 사용할 이더넷장치를 Manual로 설정한다.
3. 로봇 설정에서 설정한 Shop Floor IP와 연결되도록 IP와 netmask를 설정한다. (예: Server PC IP: 192.168.0.2, Shop Floor IP: 192.168.0.22, netmask: 255.255.255.0)
4. 제어기의 전원을 켠다.
5. 제어기 부팅이 완료된 후 ping 명령을 사용해서 제어기와 네트워크 연결을 확인한다.

### Franka Desk 접속
---
1. 웹브라우저를 실행하고 Shop Floor IP로 접속한다. (예: https://192.168.0.22)
	1. 보안되지않은 사이트라는 경고가 나와도 무시하고 접속한다.
2. 로봇설정에서 설정한 username과 password로 로그인한다.
3. Franka Desk를 이용해 로봇을 설정하고 사용할수 있다.
4. Desk의 자세한 사용법은 메뉴얼[^1] 을 참고한다.


### 참고문헌
[^1]:  Product Manual Franka Emika Robot https://download.franka.de/documents/100010_Product%20Manual%20Franka%20Emika%20Robot_10.21_EN.pdf
 