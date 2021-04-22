---
title: 'Sensor Networks'
subtitle: '센서네트워크 관련 공부한 내용들'
date: 2021-03-09 00:00:00
featured_image: '/images/under-construction.jpg'
---

![](/images/under-construction.jpg)

----
## 인터넷이란?

### 인터넷이란? : 구성요소 관점
* computing device 사이에는 엄청나게 많은 연결이 존재한다.
-> 이러한 장치들을 host 또는 end system 이라고 부른다.
-> 서버, PC, 패킷 교환기(router, switch), 기지국 등의 장치들이 있다.
-> end system 들은 Communication link 와 Packet switch를 통해 거미줄처럼 모두 연결되어 있다.

#### Communication links
데이터를 전달하는 매체로 동축 케이블, 구리선, 광케이블, 라디오 스펙트럼 등의 물리 매체로 구성되어 있다.
-> transmission rate(전송률) : bandwidth(대역폭) 이라고도 한다. 각각의 링크들이 가지는 데이터 전송 속도로 초당 비트수(bps)로 나타낸다.

#### Packet switchs
중간에 데이터 전달을 위해 있는 디바이스들로 router와 switch가 있다.
-> Packet : 한 end system에서 다른 end system으로 데이터를 보낼 때 그 데이터를 세그먼트(segment) 단위로 나누고 헤더(header)를 붙여서 만든 데이터 덩어리 이다. 받는 end system 에서는 받은 packet들을 원래의 데이터로 재조립 한다.

#### Internet
네트워크의 네트워크로 ISP 간의 연결이다.
-> ISP(Internet Service Provider) : end system들은 ISP를 통해 인터넷에 접속한다. 통신사들이 대표적인 예이다. 그리고 각각의 ISP들 끼리도 연결되어 있어야 한다. 또한 ISP 사이에도 계층이 존재한다.

#### Protocol
메세지(데이터)의 전달, 회수 컨트롤 하는 통신 규약이다.
-> TCP/IP, HTTP, Skype 등이 있다.

#### Internet Standards
인터넷에 적용되는 기술들을 동일하게 적용 될 수 있도록 정하는 표준이다.

### 인터넷이란? : 서비스 관점
어플리케이션이 작동할 수 있도록 서비스를 제공해 주는 인프라구조 이다.
-> Web, VoIP, email, game 등이 있다.
-> 어플리케이션에 프로그래밍 인터페이스를 제공해 준다.

#### Distribution application(분산 어플리케이션)
서로 데이터를 교환하는 많은 end system을 포함하는 어플리케이션

### 프로토콜이란?
통신 개체 간에 교환되는 메시지 포맷, 순서뿐 아니라 메시지의 송수신, 다른 이벤트에 따른 행동들을 정의한다.
-> 프로토콜에 따라 인터넷이 동작한다.

## Network edge
Network edge - 네트워크 가장자리
hosts(직접 통신하는 end system) : 클라이언트(client), 서버(server)가 있다.
-> 클라이언트는 보통 사용자 즉, PC나 모바일 등을 의미한다.
-> 서버는 보통 데이터 센터에 존재한다.

### Access networks and physical media
#### Access network

#### Access network
사용자로 부터 인터넷으로 접속하기까지의 구간을 의미한다.
-> host 부터 첫번째 router 까지의 구간을 의미한다.

#### DSL(digital subsciber line)

전화선을 이용해 인터넷 접속 서비스를 받는다.
-> DSLAM을 이용해 voice(전화)는 전화망으로, data는 인터넷 쪽으로 보낸다.
-> upstream(집->서버)의 전송률 < 2.5 Mbps (typically < 1Mbps)
-> downstream(서버->집)의 전송률 < 24 Mbps (typically < 10Mbps)
-> 요즘은 잘 사용하지 않는다.

#### cable network

케이블을 활용해 인터넷에 접속한다.
-> HFC : 구리와 광을 이용한 케이블로 downstram의 전송률은 < 30Mbps, upstream의 전송률은 < 2Mbps로 up/down stream의 전송속도가 다르기 때문에 접속이 비대칭(asymmetric)이라 한다.

케이블을 통해 가정을 ISP 라우터에 연결한다.
-> 각 집들은 cable headend로 가는 access network를 공유한다.
-> DSL(dedicated access)과 달리 shared access로 여러 집에서 공유된다.(여러 가구가 동시에 다운하면 나눠서 하기 때문에 시간이 느려진다.)

Frequency division multiplexing : 신호의 주파수에 따라 보내는 내용(데이터, 비디오 등) 구분이 가능하다.

#### home network


#### Enterprise access networks(Ethernet)

주로 회사, 대학 등에서 사용한다.
-> 스위치를 통해 부서, 학과 별로 인터넷이 연결되도록 한다.
-> 전송률이 10Mbps ~ 10Gbps 까지 나온다.
-> 상호 연결된 스위치들이 더 큰 인터넷으로 연결된다.

#### Wireless access network
무선랜으로 와이파이 등을 의미한다.

* wide-area wireless access : 통신사들이 운영하는 기지국을 통해 서비스 하는 네트워크이다.
-> 3G, 4G, 5G 등

와이파이 vs wide-area(5G)
와이파이 : 유선 인터넷의 접속 망의 맨 마지막에서 디바이스까지 무선으로 연장한 것으로 설계 자체가 멀리 있는 사용자를 목적으로 한 것이 아니다. 이동 목적 역시 없다(노트북 >> 핸드폰). unlicensed spectrum에 해당하는 주파수를 사용한다.(무료, 데이터 섞일 수 있음(품질 보장 x))

5G : 무선으로 이동하면서 전화 할 수 있도록 만들어진 시스템 에서 발전한 것으로 속도보다 이동성에 중점을 뒀다.(-> 전화보다 데이터 사용위주로 변화됨). licensed spectrum에 해당하는 주파수를 사용한다.(통신사에서 해당 대역을 사서 license를 받아서 사용하니까 유료, 각기 다른 주파수 쓰기 때문에 데이터 관리 가능(품질 보장))

#### Hosts: sends packets of data
host는 데이터를 전달하는 기능을 가지고 있다.
-> 전송하려는 데이터를 더 작은 사이즈로 잘라서 보내는데 이것을 packet 이라 부른다.

Packet : 데이터를 전달 할 때 해당 비트수를 한번에 보내는게 아니라 나눠서 보내는 것으로 보통 데이터 앞에 컨트롤 메세지(헤더)를 붙여서 보낸다.
-> 실제 전송되는 데이터 단위

전송시간 = (패킷당)비트수/전송률 = L/R
(전송률 = link transmission = link capacity = link bandwidth 라고도 불림, 초당 보낼 수 있는 비트수로 단위 생각 잘해야함.)

예) 1000비트 짜리 패킷, link 전송률 1Mbps
-> 전송시간 = 1000/10^6 = 1ms

### physical media
데이터 통신에서 정보를 저장하거나 전송하는 데 사용되는 물리적 물질(구리 또는 유리)

bit : 송신기와 수신기 사이에서 전파되는 데이터
physical link : 송신기와 수신기 사이에 존재하는 회선
guide media : 견고한 매체를 따라 신호가 전파됨 - 구리, 섬유, coax 등
-> 유선이기 때문에 속도가 느려지면 안테나를 더 설치하면 된다.
unguided media : 무선으로 신호가 자유롭게 전파됨 - 라디오 등
-> 무선이기 때문에 신호 감쇄가 심하고 속도와 안테나의 개수와 상관 없다.(오히려 간섭이 일어남)
#### physical media

twisted pair(TP, 꼬임쌍선) : 2개의 절연 동선.
coaxial cable(동축 케이블) : 2개의 구리선. 동심원 형태를 이룸(평행 x).
fiber optic cable(광선) : 속도가 빠름. 전자파의 영향이 적고 굉장히 멀리 이동 가능(신호 감쇠가 적음).
radio : 무선(전자기 스펙트럼을 통한 신호 전달). 환경의 영향을 많이 받음. 간섭이 존재함(반사, 물체의 영향, 간섭 등).

1.3 Network core
인터넷의 end system 들을 연결하는 패킷 스위치들과 링크들의 연결망
-> end system 들을 연결 시켜주는 중간역할을 하는 부분
-> 망 사업자들이 깔아 놓은 router 들의 집합.
-> 가입자 망 끼리 연결시켜 주는 router 들의 집합.
-> 많은 양의 데이터를 빠른 속도로, 원하는 목적지로 잘 배달해 주는 것이 목적.
-> packet switching 을 통해 전송

packet switching
패킷이 어디로 보내질 지 결정하는 것이다.
보내야 할 메세지를 패킷이라는 단위로 나누고 라우터들을 거쳐서 패킷을 전송한다.
한 라우터로 부터 다음 라우터까지 연결된 회선이 속도가 있어서 속도에 따라 패킷을 전달하게 된다.
-> 각각의 패킷은 최대 link capacity로 전송된다.

1.3.1 Packet switching : store-and-forward
패킷은 store-and-forward 방법을 통해 전달된다.
패킷을 보내면 일단 라우터에서 받고 어디로 보낼지 판단한 후 그쪽으로 패킷을 전달한다.
-> 저장 후 전달 방식.
-> 해당 패킷의 모든 데이터를 다 받아야 출력 링크를 통해 목적지로 패킷을 전송한다.
-> 출발지 부터 목적지 사이에 라우터가 존재하는데, 한 패킷을 라우터로 보낸 후 다 받은 다음 다시 전송한다.
-> 중간 라우터가 전체 패킷을 받아서(store) 처리 후 전송(forward)

R bps의 전송 속도를 가진 회선을 통해 L bit의 패킷을 전송하는 데 걸리는 시간 : L/R 초
end to end delay : 2 x L/R (전송 딜레이 무시했을 때)
-> L/R 은 one-hop delay(한 구간 source에서 router 까지, 또는 router에서 router 까지, 또는 router에서 destination 까지 등)
-> hop의 수 x transmission delay = end to end delay가 된다.
-> 만약 store and forward 방식이 아니었다면 바로 보내기 때문에 transmission time 없이 한번에 갈 수 있다.
라우터가 패킷을 받아서 처리해야 할 문제(경로 어디로 갈지 등)가 있기 때문에 sotre and forward 방식을 사용한다.


예시
L(패킷 비트수) = 7.5M, R(전송률) = 1.5Mbps -> L/R = 5
-> 총 패킷이 세개라 하면 1번이 라우터에 가는 시간 L/R
-> 2번이 라우터에 가는시간, 1번이 라우터에서 목적지로 가는 시간 L/R
-> 3번 올라오고 2번 가는 시간 L/R
-> 3번 목적지로 가는 시간 L/R
-> 총 4 x L/R 시간이 걸림
-> 만약 store and forward 아니었으면 L/R 만에 다감.

1.3.2 Packet switching : queueing delay, loss
queueing
라우터가 처리를 해서 다음 라우터로 전달하는 속도 보다 들어오는 속도가 더 빠르면 넘치는 데이터들을 라우터의 버퍼에 쌓는다.
-> 데이터가 들어오는 속도보다 회선의 속도(나가는 속도)가 느리면 라우터의 메모리(큐)에 패킷이 쌓여서 딜레이가 발생한다.
-> 네트워크의 혼잡 정도에 따라 달라질 수 있다.

loss
큐 역시 메모리이기 때문에 한계가 있다. 즉, 저장할 수 있는 패킷의 수가 정해져 있기 때문에 큐가 꽉 차면 패킷을 더이상 받지 않고 drop(loss)한다.
-> 데이터 처리가 느려지고 손실 발생이 가능하다.


예시
A와 B가 100Mb/s의 속도로 패킷을 보내고 있고 라우터에서 나가는 링크의 속도가 1.5Mb/s 일 때 queueing delay가 발생하고, 전송이 느려지게 될 것이다.
(참고 mbps : 초당 비트수, Mb/s : 초당 바이트수)


1.3.3 Two key network-core functions
네트워크 코어의 주요 function 두개

Routing
받은 패킷을 목적지 까지 빠르게 전달하기 위해 어디로 보낼지 판단하는 것이다.
-> 목적지에 따라 경로를 정함

Forwarding
아웃풋 인터페이스가 여러 개 있는데 어디로 보낼지 결정하는 것이다.
-> 포워딩 테이블을 보고 결정함
-> 데이터의 Destination address(header value랑 관련)를 보고 어떤 아웃풋 인터페이스로 보낼지 정하는데, 이 때 포워딩 테이블을 보고 판단한다.
-> 이 테이블을 만들고 관리하는 방법이 라우팅 알고리즘(어떤 라우터 끼리 연결되어 있고, 어디로 보내는 것이 가장 합리적일 지 결정)


즉, 패킷의 헤더에 목적지의 주소가 있고, routing algorithm을 통해 forwarding table을 만든 후 라우터에 패킷이 오면 패킷의 목적지 주소와 table의 header value를 보고 output link를 결정하여 내보낸다.
-> 라우팅 : 경로 생성을 위해 라우터끼리 협력 / 포워딩 : 패킷이 왔을 때 실제 전달하는 기능

1.3.4 Alternative core : circuit switching
circuit switching
출발지와 목적지 사이의 경로가 정해지면 필요한 자원들(버퍼, 링크 전송률 등)이 예약된다.
-> 여러 circuit이 있을 때 라우터들 사이에 어떤 circuit을 사용할지 정하면 다른 애들은 이 circuit을 사용하지 못한다.
-> dedicated resource : no sharing -> 간섭이 없다. 보장되어 있다.
-> 회선에서 아무런 정보의 이동이 없더라도 공유가 안되기 때문에 idle 한 상태로 남아있게 된다.(예를 들어 전화 중 아무 이야기도 안할 때 데이터의 전송이 없지만 그 회선을 다른사람이 사용 못함(자원 낭비))
-> 주로 전화망에서 사용된다.

-> 그림에서 만약 라우터들 사이의 전송속도가 1Mbps라면 회선이 4개 이므로 각 연결당 250Kbps의 전송속도를 갖는다.

특징
1. 경로를 미리 정한다.
2. 자원을 공유 안한다.(독립적)
3. delay와 loss가 완화된다.(자기만의 경로가 정해져 있기 때문에)

Circuit switching : FDM and TDM

FDM : frequency division multiplexing
-> 회선에 신호가 전달이 될 때 주파수를 분리해 놔서 동시 전송 가능(섞이지 않게)
-> 미리 정한 주파수만을 사용한다.
-> 그림에서 유저가 5명이라면 한명은 못사용한다.

TDM : time division multiplexting
-> 모든 대역을 사용하지만 시간으로 나누는거
-> 마찬가지로 4명의 유저에게 다 할당했으므로 5명이면 한명은 사용 못한다.

1.3.5 Packet switching vs Circuit switching
패킷 스위칭이 공유하기 때문에 많은 사용자가 네트워크를 사용 가능하다.

예시

-> 데이터를 전송할 트래픽이 있을 때 active라 하는데, active 시간이 전체 시간의 10%이다
-> 전체 시간 중 10%는 보낼 데이터가 있고, 나머지 90%는 보낼 데이터가 없음.

circuit switching
1Mbps 의 link를 사람 당 100Kpbs를 사용하므로 총 10명이 사용할 수 있다.(1M / 1K = 10)

packet switching
-> 여러 사용자가 동시에 사용하게 되면 큐잉 딜레이 때문에 늦게 도달할 수 있다.
-> 하지만 사용자가 35명이라 해도 11명 이상의 인원이 동시에 active할 확률은 0.0004(0.04%)보다 작다.
-> 많은 사용자가 사용이 가능해져서 효율성이 높아진다.

packet switching vs circuit switching
무조건 패킷이 좋은가?

패킷의 장점

트래픽이 균형 잡힌게 아닐 때 자원 공유하면 유리함
-> 내가 사용 안할 때 다른애가 사용이 가능하니까
서킷은 자원 예약 과정(call setup)이 필요 하지만 패킷은 이런 과정이 필요 없고 단순하다.
패킷의 단점

밀리는 문제(큐잉 딜레이, 손실)
-> reliable한 데이터 전송과 congestion control을 위한 프로토콜이 필요하다.
오디오, 비디오와 같이 bandwidth의 보장이 필요한 경우 패킷은 보장이 안된다.
1.3.6 Internet structure : network of networks
인터넷 구조 : 네트워크의 네트워크
end system 들은 access ISP(Internet Service Provider, 가입자망)를 통해 인터넷과 연결되어 있다.
Access ISP 끼리 서로 연결 되어있어야 한다.
-> 연결 되어 있어야 임의의 두 호스트가 서로 패킷을 보낼 수 있다.
네트워크의 네트워크는 매우 복잡하다
-> 경제적, 국가적 정책에 따라 연결 되었다.

네트워크 구성 방법
수백만개의 access ISP 들이 존재한다. 어떻게 연결할 까?

모든 access ISP 들을 서로 연결해 준다. -> 연결이 너무 많아져서 불가능하다.


중간에 하나의 global ISP가 존재한다. -> 모든 망들이 global ISP를 통해 다른 망으로 가도록 한다(돈을 내고 사용) -> 전세계를 하나의 global ISP로 관리하는것은 힘들다


여러 ISP들이 존재한다. -> 어느 하나에 몰리면 그 ISP가 힘들다.


IXP(ISP 끼리 연결시켜 주는 라우터)를 통해 ISP 끼리 서로 연결해 주자(peering)(자기들 끼리는 무료)


access net을 ISP와 연결해 주는 regional net을 만드는 경우도 있다.
-> 특정 지역에서 여러 가입자 망들한테 자기네 망을 이용하여 ISP를 지원해 주는거 -> 가입자가 regional net한테 돈 내고, regional net이 ISP로 돈 내는거(망 사용료)


Content provider network -> 자체적으로 유뷰트 같은 서비스 제공해 주는 네트워크

구글은 전 세계에 데이터 센터들이 있고, 이 데이터 센터들을 연결하기 위해 ISP를 사용하지 않고 자기들이 직접 연결함(public 망이 아님(private한 망), 구글 데이터만 이동하게 되어 있음) -> 구글이 사용자에게 서비스 제공할 때는 ISP와 협약 맺음

현재 인터넷 구조(계층적 구조 - 완전한 계층은 아님, 제공자 소비자 구조)

1.4 Delay, loss, throuput in networks
-> 성능 측정 지표들


패킷의 도착 속도가 나가는 속도보다 커지면 패킷들은 큐에 쌓이게 되고 자신의 턴을 기다리게 된다.
-> 딜레이 발생(queueing delay)
-> 버퍼가 꽉차게 되면 패킷의 손실(loss)이 일어난다.


딜레이는 총 네가지의 구성 요소로 나누어 생각해 볼 수 있다.
1. processing delay(nodal processing)

패킷 전송 전에 프로세싱 하는 딜레이(비트 에러 체크, output link 결정) -> 데이터 처리에 걸리는 시간
보통 1 msec 보다 적게 걸린다.(굉장히 작음)
queueing delay
전송을 위해 output link를 기다리는 시간(나가기 위해 걸리는 시간 -> 큐 안에서 나가기 까지 걸리는 시간)
라우터에서 얼마나 밀리는 지에 따라 달라진다.
transmission delay
dtrans = L/R
패킷의 모든 비트들을 회선에 올리는 시간 -> 큐에서 link로 모든 비트를 내보내는데 걸리는 시간
propagation delay
한 비트가 목적지 까지 회선을 따라 이동하는데 걸리는 시간
d: physical link의 길이, s: propagation 속도 -> dprop = d/s
예시 1

자동차의 속도 : 프로파게이션 딜레이와 관련 있음 -> 100km/h 로 가정
톨 부스 : 라우터 역할 -> 트랜스미션 딜레이와 관련 -> 서비스 하는데 12 sec이 걸린다고 가정
자동차 : 비트역할
carvan : 패킷 역할
carvan이 두번째 톨 부스에 줄 서기까지 얼마나 걸릴까(첫 차가 톨부스에 도착하면 마지막 차도 올때까지 대기한다고 가정)
-> 전체 carvan이 톨부스를 통과하는데 걸리는 시간 : 한 대당 12초 걸리니까 총 10대 이므로 120초
-> 마지막 차가 첫번째 톨부스에서 두번째 톨부스까지 가는 시간 : 100km를 100km/h로 달리니까 1시간
-> 전체 걸리는 시간 : 1시간 + 2분 = 62분

예시 2
자동차의 속도 : 1000km/h 로 가정
톨부스 : 서비스 하는데 1분이 걸린다고 가정
모든 차가 첫번째 톨부스에서 서비스 되기 전에 차가 두번째 톨부스에 도달 할까?
-> 차 한대가 다음 톨까지 가는데 걸리는 시간 : 1000km를 60분에 가니까 100km는 6분에 감(propagation delay = 6분)
-> 전체 carvan이 톨부스를 통과하는데 걸리는 시간 : 1분 x 10대 = 10분
1시에 출발한다고 했을 때
-> 첫차가 두번째 톨까지 가는데 걸리는 시간 : 1분 + 6분 = 7분 -> 1시 7분 도착
-> 두번째 차가 두번째 톨까지 걸리는 시간 : 7분 -> 1시 1분 출발, 1시 8분 도착(첫 차가 달리기 시작할 때 두번째 차는 톨부스에서 처리중이니까 1시 1분에 톨부스에 진입하는거)
-> 세번째 차가 두번째 톨까지 절리는 시간 : 7분 -> 1시 2분 출발, 1시 9분 도착
...
-> 첫 차가 도착했을 때(1시 7분) 8번째 차가 톨부스에서 처리중이고, 9,10번째 차는 대기상태
-> 차 한대가 2번째 톨에 도달하는 동안 맨 뒤 세대는 아직 첫번째 톨도 통과 못한 상태
-> 전체 걸리는 시간 : 프로파게이션 딜레이 6분 + 트랜스미션 딜레이(1분 x 10대) = 16분

1.4.1 queueing delay
R : 회선의 전송 속도 -> 단위시간 동안 보낼 수 있는 데이터의 양(bps)
L : 패킷의 길이(크기)
a : 단위시간 당 도착하는 패킷의 개수 -> 1초에 몇개의 패킷이 라우터에 들어오는가
(모든 패킷이 L로 같다고 가정)
La : 1초에 몇비트의 데이터가 라우터에 들어오는가 -> traffic이 들어오는 속도
R : traffic이 나가는 속도

-> La/R = traffic intensity(트래픽 밀도) = 들어오는 속도와 나가는 속도의 비율
-> La/R = 0 : queueing delay가 적다
-> La/R = 1 : 비율은 같아서 들어오는 속도가 일정하다면 딜레이가 없을 수 있지만, 라우터로 들어올 때 일정하게 들어오는 것이 아니라 어느 때는 많이, 어느 때는 적게 들어오기 때문에(들어오는 패턴이 랜덤) 한꺼번에 트래픽이 몰리게 되면 그 순간에 queueing이 생기게 되어 delay가 커진다.
-> La/R > 1 : 들어오는 속도가 더 크기 떄문에 queue는 끝없이 증가하고, drop이 없다고 가정하면 기다리는 시간이 무한해 진다.

1.4.2 packet loss

큐는 유한한 용량을 가지고 있다.
큐가 가득 차게 되면 더이상 패킷 못받으니까 패킷이 드랍된다.
-> 재전송을 통해 다시 보내야 한다.

1.4.3 Throughput

throughput : sender와 receiver 사이에 비트가 전송되는 속도를 의미한다.

instantaneous : 순간적 -> 특정 지점에서의 속도
average : 평균적 -> 전체적인 속도

Rs < Rc : Rc가 더 빠르지만 라우터에 도달하는 Rs에서 오는 데이터들 만큼만 전송할 수 있다. -> 속도는 Rs에 따라 결정된다.
Rs > Rc : Rs가 더 빠르기 때문에 라우터에 패킷이 도달 하더라도 Rc의 속도로 패킷을 전달하게 된다. -> 속도는 Rc에 따라 결정된다.
-> bottleneck link : 앞에 있는 것의 전송 속도가 느리다면 뒤에 있는 파이프가 속도가 빠르더라도 앞의 속도에 맞춰야 한다. 마찬가지로 뒤의 것이 속도가 더 느리다면 앞에서 빨리 보내주더라도 늦게 보낼 수 밖에 없다 -> end to end의 전송속도가 결정된다.
throuput : internet scenario

출발지가 10개, 목적지가 10개 있고, 한 파이프를 통해 보낼 때 end to end throughput은 Rs,Rc,R/10(공유 네트워크를 여러명이 나눠 사용) 중 가장 작은 것에 따라 결정된다. 그리고 그것이 bottleneck link가 된다.
-> 보통 core는 좋은 것을 쓰기 때문에 Rs나 Rc가 bottleneckdl ehlsek.


 

* switching - 2계층

같은 네트워크(같은 LAN)에 있는 장치들 사이에서 데이터 패킷 switch
switch는 2계층 주소 (MAX address)를 사용해 어디로 데이터 패킷을 보낼지 안다.
* routing - 3계층

다른 네트워크들 사이에서 패킷 route
router는 네트워크의 목적지 IP 주소를 이용하여 패킷 보낼 곳을 안다.
 

Link layer 관련 용어들

호스트와 라우터들: nodes
communication 경로 사이에서 인접한 노드들을 연결하는 communication channels: links
wired links
wireless links
LANs -> L(link)
PAN -> P(personal)
2계층 패킷: frame, 데이터그램 인캡슐화
data-link layer는 데이터드램을 링크를 통해서 하나의 노드에서 물리적으로 인접한 노드로 전송하는 역할이다.

 

 

Link layer services

framing, link access:
데이터그램에 header와 trailer를 더해 frame으로 인캡슐화
공유되는 매개체라면 채널 접근
"MAC" address는 출발지를 나타내기 위해 frame header에 사용한다.
IP 주소와 다름
인접한 노드들 사이에서 reliable delivery
wireless links: 에러율 높음
무선은 에러가 많아서 체크를 많이 해야 함 (에러 확인하면 다시 보내는데, 다시 보내는게 많아서 유선보다 느림)
wire link(유선, 광케이블): 에러율 매우 작음
flow control: 인전한 송신 노드와 수신 노드 사이의 페이싱(pacing)
error detection
signal attenuation, noise로 에러 유발됨
수신자는 에러 탐지 
수신자의 재전송을 위해 시그널을 보내거나 frame을 버림
error correction:
수신자가 식별하고 bit error를 수정한다.
half-duplx and full duplex
half-duplex: 보내고 받는거 다 가능하지만 한 번에 하나만 가능하다.
즉, 두 end points가 서로 서통할 때, 둘 다 보내고 받을 수는 있지만, 둘 다 동시에 보낼 수는 없음
full-duplex: 보내고 받는게 동시에 가능 (반은 보내는 쪽, 반은 받는 쪽으로 사용하면 됨)
무선은 한 번에 못 함
 

 

* link layer은 "adaptor"에서 구현된다. (모든 호스트에 있는)

 

 

 


sending side:

데이터그램을 frame으로 인캡슐화
에러 확인 비트, rdt, flow control 등을 추가
receiving side:

에러, rdt, flow control 찾음
데이터그램을 추출해서 상위 계층에 보냄
 

 

 

 

 

Error detection

Parity checking
single bit parity: 

 

짝수 페리티 비트라면 1의 개수가 짝수가 되도록 parity bit를 설정하고,

홀수 페리티 비트라면 1의 개수가 홀수가 되도록 parity bit 설정

 

 


 

1차원 bit parity의 경우, 오류를 찾을 수는 있지만 수정은 불가

 

2차원 bit parity는 잘못된 부분 찾아서 수정도 가능

하지만 redundant한 bit가 2배가 됨

 

보통 detection만 한다. 

잘못되면 다시 보내면 되니까 ㅎㅎ

 

 

 

 

 

Checksum

4계층에서 사용하는 error detection -> checksum
Cyclic redundancy check (CRC)
D%G=R
나머지를 데이터에 붙여서 보내면 받는 쪽은 나누어 떨어짐

 


 

나머지가 없다는 것은 에러가 없다는 것을 의미

 

 

 

 

 

 

 

 

 

 

 

 

 

 

 

Multiple access links, protocols

"links"의 두 가지 타입:
point-to-point:
전화 접속을 위한 PPP
Etherner switch, host 사이의 point-to-point link
broadcast:
옛날 방식의 Ethernet
upstream HFC
cocktail party 효과 -> 옆 사람이 시끄러우면 나도 시끄럽게 말하고, 점점 시끄러워짐
이를 방지하기 위한 것: medium access control (polling) <- 충동 방지
한명씩 말하도록 컨트롤
medium = multiple
단일 shared broadcast channel
노드에서 동시에 두 개 이상이 전송: interference(간섭)
만약 노드가 두 개 이상을 동시에 받는다면 collision
collision 발생 조건
shared media
동시에 여러개의 시그널을 receive
ㄴ 이를 구분해내지 못할 때
multiple access protocol -> collision 줄이는게 목적
노드들이 어떻게 channel을 공유할지 결정하는 분산된 알고리즘
예: 노드가 언제 전송할지 결정
channel sharing에 대한 communication은 자기 자신의 channel을 사용해야만 한다.
협력하는 out-of-band channel 없음
 

 

MAC protocols: taxonomy

three broad classes:

channel partitioning
채널을 작은 조각(time slots, frequency, code)로 나눔
노드에게 조각을 독점적으로 할당
random access
나눠지지 않는 채널, 충돌 허용
충돌로부터 복구(recover)
taking turns
노드들이 교대로 작동하지만, 보낼게 많은 노드는 오래 턴을 가질 수 있다.
 

 

Channel partitioning MAC protocols: TDMA (Time Division Multiple Access)

충돌 발생하지 않음 -> 자기 턴에만 보내니까
시간을 partitioning
"rounds" 안에서 채널에 접근
각 스테이션은 각 라운드 안의 고정된 길이의 슬롯을 가진다 (길이=패킷 전송 시간)
노드에게 각 시간 슬롯을 각각 할당해준다.
노드는 전송할 새로운 패킷이 있으면 자신에게 할당된 시간 슬롯 동안 패킷 비트들을 전송한다.
사용하지 않는 슬롯은 낭비되는 것
전송할 패킷을 가진 노드가 하나일지라도 타임슬롯 R/N 대역폭으로 한정된다
ex: 6-station LAN, 1,3,4는 패킷 가짐, 2,5,6 슬롯은 낭비

 

 

Channel partitioning MAC protocols: FDMA (Frequency Division Multiple Access)

TDM은 브로드캐스트 채널을 시간으로 공유하지만, FDM은 R bps의 채널을 다른 주파수로 나눠서 각 주파수를 N개 노드 중 하나에게 할당한다. (각 R/N의 대역폭을 갖는다)
TDM과 장단점 유사
frequency bands로 채널 스펙트럼을 나눔

각 스테이션은 고정된 frequency band를 할당 받음
frequency bands에서 사용하지 않는 전송 시간은 낭비됨
ex: 6-station LAN, 1,3,4는 패킷 가짐, 2,5,6 frequency bands는 낭비

 

 

Random access protocols

노드가 전송을 위한 패킷을 가지고 있을 때
전체 채널 데이터 속도 R로 전송
노드 간의 우선순위 없음
두 개 이상 노드를 전송 -> collision
random access MAC protocol은 명시한다:
어떻게 충돌을 탐지할지
어떻게 충돌로부터 복구할지 (예: 지연된 재전송을 통해)
random access MAC protocol의 예:
slotted ALOHA
ALOHA
CSMA, CSMA/CD, CSMA/CA
 

 

Slotted ALOHA

가정:
모든 frame은 같은 사이즈
시간을 같은 사이즈의 슬롯으로 나눈다
노드는 슬롯 시작에서 전송 시작 (시작과 함께 노드 보낼 수 있음)
각 노드는 언제 슬롯이 시작하는지 알 수 있게끔 동기화 되어 있다.
만약 2개 이상의 노드가 슬롯에서 전송되면, 모든 노드는 충돌을 감지함
작동:
노드가 새로운 frame을 얻으면 다음 슬롯으로 전송
만약 충돌이 없다면: 노드는 다음 슬롯으로 새로운 노드를 보낼 수 있다.
만약 충돌이 있다면: 노드는 성공할 때까지 각 subsequent slot에서 frame을 재전송하며, 각 전송시 성공할 확률은 P이다

 

 

 

S 구간처럼 활동하는 노드가 하나일 때만 전송 가능

충돌이 일어나면 아무도 못 쓰게 함 -> 단점

 

 

 

 

 

 

 장점:
혼자만 활동하는 노드는 계속해서 채널의 최고 속도(full rate)로 전송할 수 있다.
전송할 프레임이 있는 노드를 활성 노드라고 함
하나의 노드가 전체 채널을 쓸 수 있음
고도로 분산된(highly decentralized): 노드에 있는 슬롯은 동기화해야한다.
단순
단점:
충돌, 기다리는 슬롯
슬롯 낭비 - 활성 노드가 많으면 일부 슬롯이 충돌로 인해 낭비된다, 활성 노드가 없을 경우
충돌 탐지가 느림 (?)
clock synchronization
효율성
: long-run fraction of successful slots (많은 노드들, 보내기 위한 많은 프레임을 갖는 모두)
가정: 전송을 위한 많은 프레임을 가지는 N개의 노드가 각 슬롯에 전송할 확률 -> p
주어진 노드가 슬롯에 전송 성공할 확률 = 
p
(
1
−
p
)
N
−
1
어떤 노드가 전송 성공할 확률 = 
N
p
(
1
−
p
)
N
−
1
최고의 효율성: 최대 확률 
N
p
(
1
−
p
)
N
−
1
많은 노드에서, 
N
p
(
1
−
p
)
N
−
1
에서 N이 무한으로 가면:
max efficiency = 1/e =0.37
ㄴ> 채널이 사용중일 확률
기껏해야 37%만이 유용한 전송을 한다. (채널 이용률이 37% 이하라는 말)
 

 

Pure (unslotted) ALOHA

만약 위 방법에서 slot이 없다면

단순하고 동기화 없음

 


성능 2배로 안 좋아짐
 

 

CSMA (Carrier Sense Multiple Access)

CSMA: 전송하기 전에 누가 보내고 있는지 들음:
만약 채널이 낭비되고(아무 일도 안하고) 있다면: 전체 프레임 전송
누가 말하고 있으면 쉬었다가 보냄 -> 충돌 줄임
CSMA collisions
충돌은 여전히 발생할 수 있다
channel propagation delay: 신호가 채널의 한쪽 끝에서 다른 쪽 끝으로 전파되는 데 걸리는 시간
이러한 전파 지연이 길수록 네트워크의 다른 노드에서 이미 시작된 전송을 캐리어 감지 노드가 감지할 수 없는 경우가 더 증가한다.
collision: 전체 패킷 전송 시간이 낭비됨
거리, 전파 지연은 충돌 확률 결정에 역할을 한다.

 

 

시간이 지나면서 거리가 늘어나는 것 -> propagation delay

 

노란색은 처음에 말하는 사람이 없어서 전송

빨간색도 처음에는 말하는 사람이 없어서(자기가 들을 수 있는 위치에) 전송

 

전송 후, 조금 있다 충돌

 

충돌이 일어나면 바로 멈춤

 

 

 

 

 

CSMA/CD (collision detection)

CSMA/CD: carrier sending, deferral as in CSMA
짧은 시간 안에 충돌 탐지
충돌하면 전송을 중단시켜 채널 낭비를 줄임 -> CSMA는 전송 뒤 충돌해도 그대로 전송함
충돌 탐지:
유선 LAN에서는 쉬움: 시그널 길이 측정, 전송 비교, 시그널 받기
무선 LAN에서는 어려움: 수신 신호 세기가 로컬 전송 세기에 압도되서 신호를 못 받음 (탐지 불가)
 

 

 

Ethernet CSMA/CD 알고리즘

NIC는 네트워크 계층으로부터 데이터그램을 받고, frame을 만든다
만약 NIC가 채널이 놀고 있다고 느끼면 프레임 전송을 시작한다. 만약 NIC가 채널이 바쁘다고 느끼면, 채널이 널널해질 때까지 기다렸다 전송한다.
만약 NIC가 다른 전송을 탐지하지 않았고, 전체 프레임을 전송했다면, NIC는 프레임 전송 완료!
만약 NIC가 전송하는 동안 다른 전송을 탐지했다면, 중단하고 jam 신그널을 보낸다.
중단 후, NIC는 binary (exponential) backoff에 진입: (exponential random backoff)
m번째 충돌 이후, NIC는 {0, 1, 2, ..., 
2
M
−
1
}에서 랜덤하게 K를 고른다. 그리고 NIC는 K*512bit 시간을 기다리고 step 2로 돌아간다.
충돌이 많으면 backoff 간격이 커짐
즉, 전송했는데 충돌 일어나면 1초 기다림. 다시 보냈더니 또 충돌 일어나면 2초 기다리고, 또 충돌 일어나면 4초... 이런식
 

"Taking turns" MAC protocols

channel partitioning MAC protocols:
high load에서 효율적이고 공정하게 채널 공유
low load에서 비효율성: 채널 접근 지연, 한 개의 노드만 활동할 때만 1/N bandwidth 할당함
random access MAC protocols:
low load에서 효율적: 하나의 노드는 완전하게 채널 유틸리티 사용 가능
high load: 충돌 오버헤드
"taking turns" protocols
다 사용하기는 하지만 중앙에서 처리 필요
 

 

"Taking turns" MAC protocols

polling:
마스터 노드는 전송할 차례인 slave 노드를 방문함 
마스터가 자신을 선택해 줄때만 말할 기회를 얻음
slave 장치들은 멍청
문제:
polling overhead
latency (지연 시간)
single point of failure (하나 망하면 다 망)
token passing:
마스터 노드 없이 토큰을 노드들 사이에서 돌리면서 토큰 받은 노드가 말하게 함
문제:
token overhead
latency
토큰 하나만 돌리면 너무 느리면 토큰 두 개로 늘릴 수 있음
single point of failure
어떤 노드가 토큰 버려버리면 아무도 말 못 함


MAC addresses and ARP

우리가 지금까지 쓰던 IP는 8bit 4개로 총 32bit IP 주소이다
전세계에서 유일한 나만의 IP를 가짐
위치하고 바인딩 되어있음 (IP를 보고 위치를 알 수 있음)
MAC(or LAN or Physical or Ethernet) 주소
모든 디바이스들은 MAC 주소를 가짐
네트워크 세그먼트의 데이터 링크 계층(2계층)에서 통신을 위한 네트워크 인터페이스에 할당된 고유 식별자
 

* IP는 주민등록번호 느낌 -> 변하지 않음

* MAC address는 집 주소 느낌 -> 이사가면 바뀜

 

 

LAN addresses

MAC 주소는 IEEE에서 할당 -> unique를 보장
제조업자는 MAC 주소 공간의 일부분을 구매
MAC flat address -> portability
MAC addr은 처음부터 끝까지 모든 digit으로 무언가를 구분하지 않음. 계층이 없음 -> flat하다
flat한 게 IP와의 차이 (IP 주소는 계층적이니까)
 

 

ARP: address resolution protocol

Q: IP주소를 알 때, 인터페이스의 MAC address를 어떻게 결정하는가?
ARP table: LAN에 있는 IP 노드(호스트, 라우터)들 각각은 테이블을 가진다.
몇몇 LAN 노드를 위해 IP/MAC address 매핑; <IP address, MAC address, TTL>
TTL (Time To Live): 일정 시간 지나면 매핑된 주소 사라짐 (보통 20분)
 

ARP protocol: same LAN

A가 B에게 데이터그램을 보내고 싶다면
A는 B의 MAC addr을 모른다 (A 테이블 내에 존재하지 않음)
A는 B의 IP 주소가 담긴 ARP 쿼리 패킷을 broadcast한다
목적지 MAC 주소를 FF-FF-FF-FF-FF-FF로 채워서 보냄
LAN에 있는 모든 노드는 ARP 쿼리를 받음
B는 ARP 패킷을 받고, A에게 자신의(B) MAC 주소를 넣어서 답장함 
A의 MAC 주소로 프레임을 보냄 (unicast) -> (받은 쿼리에 source addr 적혀있으니까)
A는 IP-MAC addr 쌍을 자신의 ARP 테이블에 저장함 
ARP는 "plug-and-play"
와이파이 등에 연결하는 순간 자동으로 동기화됨. 그 때부터 <IP, MAC addr> 업데이트 
노드는 net 관리자에게 간섭받지 않고 ARP 테이블을 만든다.
 

 

☆Addressing: routing to another LAN☆

walkthrough: R(라우터)을 통해 A에서 B로 데이터그램을 보냄
여기서는 MAC addr만 보임
A는 B의 IP 주소를 안다고 가정
A는 첫 번째 hop 라우터(R)의 IP 주소를 안다고 가정
A는 R의 MAC addr 주소를 안다고 가정

목적지 주소를 라우터의 MAC 주소로 지정하면, 나가고 싶다는 신호로 간주됨
현재 네트워크 밖으로 데이터그램을 보내겠다는 말
그럼 라우터는 그 패킷 안에 적힌 IP 주소를 보고 해당 호스트로 보내기 위해 라우팅 테이블을 보면 포워딩을 함
이 때 사용하는 것이 longest prefix matching 알고리즘
IP는 3계층, MAC addr은 2계층
 즉,
A는 목적지 주소(MAC dest)를 FF-FF-FF-FF-FF-FF로 채워서 broadcasting 함
만약 반응이 없다면, 현재 네트워크 내에 B가 존재하지 않는다는 말
그렇다면 이제 목적지 주소를 라우터의 MAC addr로 채워서 보냄 -> "안에는 없으니 밖에 알아봐주세요~"
라우터는 그 frame을 받으면 MAC 주소 때고, IP src:A, IP dest:B를 가지는 데이터그램 포워드
 

 

Ethernet

이더넷은 네트워크에 연결된 각 기기들이 MAC 주소를 가지고 이 주소를 이용해 상호간에 데이터를 주고 받을 수 있도록 만들어졌다. 각 기기를 상호 연결시키는 데에는 허브, 네트워크 스위치 등의 장치를 이용한다.
지배적인 유선 LAN 기술
token LANs과 ATM보다 간단하고 저렴
 

Ethernet: physiscal topology

bus: 90년대 중반에 인기
모든 노드가 같은 충돌 영역에 있음
star: 요즘 많이 사용
중앙에서 switch가 똑똑하게 관리
mac learning, switch learning

 

Ethernet frame structure

송신 어댑터는 이더넷 frame에서 IP 데이터 그램을 캡슐화한다.

preamble: 10101010 패턴이 7byte(->10101010이 7번 반복)하고 10101011 패턴이 1byte
수신자, 송신자 클락 속도 동기화하는데 사용
preamble을 쭉 보낸 후, 첫 번째 6byte destination, 그 다음 6byte source를 보냄
dest를 먼저 들어보고, 자기가 아니라면 무시(frame 버림)하고 자기이면 쭉 들음
frame에 들어있는 데이터를 네트워크 계층 프로토콜로 보냄
type: 어떤 상위 계층 프로토콜인지 지정
CRC: cyclic redundancy check at receiver
crc붙여서 에러 탐지하거나 복구함
 

Ethernet: unreliable, connectionless

connectionless: 송수신자 사이에서 handshaking 없음
unreliable: 수신한 NIC은 ack이나 nack을 송신자한테 보내지 않음
CRC 붙여서 탐지되면 버리고, 탐지 안되면 어쩔 수 없는 것
나머지는 TCP한테 맡김
Ethernet's MAC protocol: unslotted CSMA/CD with binary backoff
 

 

Ethernet switch

link layer device: 적극적인 역할을 맡음
Ethernet frame을 저장하고 포워딩함
들어오는 프레임의 맥어드레스를 조사하고, 프레임이 세그먼트에 전달될 때, 하나 이상의 나가는 링크로 프레임을 선택적으로 포워딩한다.
CSMA/CD를 사용하여 세그먼트에 액세스
transparent
호스트는 스위치의 존재를 인지하지 못 함
plug-and-play, self-learning
우리가 스위치에 플러그를 꽂는 순간(접속하는 순간) 자동으로 동기화 됨
스위치가 환경 설정할 필요없음
 

Switch: 여러개를 동시에 전송

호스트는 스위치와 직접 연결(direct connection)함
스위치는 패킷 buffer
각 스위치는 스위치 테이블을 가짐
entry: <MAC addr of host, interface to reach host, time stamp>
라우팅 테이블 느낌
Ethernet protocol은 각 들어오는 링크를 사용, 충돌 없음; full duplex
각 링크는 자신의 충돌 영역이 있음
switching: A-to-A' and B-to-B'로 충돌없이 동시에 전달할 수 있다.

 

A에서 A'로 보내기

A는 현재 누가 A'인지 모름
A가 A'한테 보낼거라고 스위치에 보내면, 스위치는 스위치 테이블을 업데이트 함(learning)
스위치:는 A라는 MAC addr은 interface 1번에 연결되어 있음을 알게되고 스위치 테이블에 저장한 후 60초 동안 기억
스위치가 스위치 테이블을 봄
매치가 되면, 해당 인터페이스에 보낸다.
매치가 안되면, flooding 한다. (다른 모든 애들한테 보냄)
A'는 flooding된 데이터를 보고 자기를 찾는 다는 것을 알면, 스위치한테 알려줌. 그럼 스위치는 A'는 interface 4번과 연결된다는 것을 알게됨
이러한 과정을 MAC switching learning or MAC learning이라고 부름
 

 

라우팅과 스위칭의 learning 차이

MAC switching learning: 플러그를 꽂자마자(통신이 시작하자마자) 있는걸 가지고 계속 업데이트함 
뽑힌거에서 오는 걸 보고 습득을 하면서 업데이트
인접한 애 찾기
routing: 옆에 있는 hop의 정보를 가지고 다익스트라나 벨만포드로 업데이트를 함
경로 찾기

 

 

 

라우터 vs 스위치

둘 다 store and forward
라우터: 네트워크 계층 장치 
스위치: 링크 계층 장치
둘 다 forwarding table을 가짐
라우터: IP주소를 사용해서 테이블 연산 -> 라우팅 알고리즘
스위치: flooding을 이용해서 포워딩 테이블 학습 (MAC addr 학습)
3계층 장비라 세 계층의 주소를 다 봐야함



Network layer

송신자 호스트에서 수신자 호스트로 세그먼트를 transport
송신측: 세그먼트를 datagrams으로 캡슐화
수신측: segment를 transport layer로 전달
 

2개의 주요 network layer functions

forwarding:
라우터의 input포트에서 적절한 라우터의 output포트로 패킷을 이동시킴
routing:
출발지에서 목적지까지 패킷이 이동할 경로를 결정
라우팅 알고리즘을 이용하여 포워딩 테이블을 만드는 작업

 

routing algorithm: 경로 결정

 

forwading table: 선택된 경로를 저장해 둔 것

 

 

 

 

 

 

 

 

 

 

 

 

 

 

Connection setup

datagram이 전송되기 전에, 두 개의 end hosts와 중간 라우터들은 virtual connection을 설립한다.
라우터가 관여
network layer vs transport layer connection service:
network: 두 개의 호스트 사이(vc의 경우 호스트가 라우터를 개입시킬 수도 있다)
transport: 두 개의 프로세스들 사이
 

Connection, connection-less service

datagram network는  네트워크 계층 connectionless 서비스를 제공한다.
virtual-circuit network는 네트워크 계층 connection 서비스를 제공한다.
TCP/UDP 연결 지향, 비연결지향 transport 계층 서비스와 유사하지만
service: host-to-host 
구현: 네트워크 코어에서 구현됨
 

네트워크 상에 데이터를 전송하기 위한 방식은 크게 회선교환 방식과 패킷교환 방식으로 나눌 수 있다.
Datagram Network:

데이터는 한 개 이상의 패킷으로 구성되어 네트워크로 전달되게 되는데 데이터그램 네트워크는 각 패킷의 전달 경로가 다를 수 있다. 이 때문에 목적지에 도착하는 패킷의 순서가 송신자에서 보낸 순서와 맞지 않을 수 있기 때문에 목적지에서 패킷의 재조합이 필요하다.

Virtual-Circuit Network:

송신지에서 목적지로 패킷을 보내기 전에 전달된 패킷이 이용할 경로를 미리 예약하게 된다. 예약하는 과정은 각 경로에 존재하는 라우터의 라우팅 테이블에 자신의 송신지와 목적지의 경로를 설정하게 된다. 패킷을 전달하기 전에 경로를 설정해야 한다는 부담이 있긴 하지만 한번 경로가 설정되면 송신지에서 목적지로 보내는 패킷들은 순서가 보장되어 전달되기 때문에 목적지에서 재조합할 필요가 없다

 

 

Virtual circuits(VC) forwarding table


 

Vurtual circuits: signaling protocols

used to setup, maintain teardown VC
오늘날 인터넷에서 사용하지 않음

 

 

Datagram networks

no call setup at network layer
routers: end-to-end 연결에 대해 no state
네트워크 계층에서는 connection이라는 개념이 없다
목적지 호스트 주소를 사용해서 패킷을 포워딩한다.
 

Datagram forwarding table


 


 

Longest prefix matching

지정된 대상 주소에 대한 포워딩 테이블 항목을 찾을 때, 대상 주소와 일치하는 가장 긴 주소 접두사를 사용
 


예를 들어, 11001000 00010111 000110의 link interface를 찾을 때, 1번과 겹치는 것이 많기 때문에 1번과 2번 중 1번을 선택하게된다.

 

 

Datagram or VC network: why?

Internet(datagram)

컴퓨터 사이에서 데이터 교환
많은 link 타입들
다른 특성 
균일한 서비스 어려움
"smart" end system
중간에 있는 라우터는 멍청해도 ㄱㅊ
 

ATM(VC)

전화에서 진화
end system이 멍청
중간에 있는 라우터들이 똑똑해야 함


Router architecture overview
라우터의 주요 2가지 기능:

라우팅 알고리즘/프로토콜(RIP, OSPF, BGP) 작동
들어오는 데이터그램을 나가는 링크로 포워딩 시킴

 

Input port function


 

 

검색을 통해 패킷의 출력 포트가 결정되면 패킷을 스위칭 구조로 보낼 수 있다.

 

 

 

 

 

match - 목적지 IP 주소를 찾음

action - 패킷을 스위칭 구조를 통해 지정된 출력 포트로 보냄

 

 

 

 

 

Switching fabrics

스위칭 구조를 통해 패킷이 입력 포트에서 출력 포트로 실제로 스위칭(즉, 전달)되므로 스위칭 구조는 라우터의 핵심이다.
패킷을 인풋 버퍼에서 적절한 출력 버퍼로 이송시킴
switching rate: 패킷이 인풋에서 아웃풋으로 전송될 수 있는 속도
switching fabrics의 3가지 타입

CPU(라우팅 프로세서)를 직접 제어해서 스위칭하는 전통적인 방식이다
입/출력 포트는 전통적인 I/O 장치처럼 작동함
패킷이 도착하면 입력 포트는 라우팅 프로세서에게 인터럽트를 보내 패킷을 프로세서 메모리에 복사한다. (패킷은 시스템 메모리에 카피됨)
속도는 메모리 bandwidth에 의해 제한된다. (데이터그램 당 2 bus crossings)
 


데이터그램이 입력 포트 메모리에서 (라우팅 프로세서의 개입 없이) 공유 버스를 통해 출력 포트 메모리로 이동
모든 출력 포트에 패킷이 수신되지만 라벨과 일치하는 포트만 패킷을 유지한다.
라벨은 스위치 내에서 버스를 통과하기 위해서만 사용되므로 출력 포트에서 제거된다.
동시에 여러 패킷이 다른 입력 포트로 라우터에 도착하면 한번에 하나의 패킷만 버스를 통과할 수 있기 때문에 하나를 제외한 모든 패킷은 대기함
bus contention: switching speed는 bus bandwidth에 의해 제한됨
속도: 메모리 << 네트워크


bus bandwidth의 제약을 극복
N개의 입력 포트를 N개의 출력 포트에 연결
각 수직 버스는 교차점에서 각 수평 버스와 교차하며 스위치 구조 컨트롤러에 의해 언제든지 열거나 닫을 수 있다.
여러 패킷을 병렬로 전달 가능
두 개의 서로 다른 입력 포트에서 나오는 두 개의 패킷이 동일한 출력 포트로 보내지는 경우 -> 한번에 하나의 패킷만 특정 버스에서 전송될 수 있으므로 나머지 하나는 입력포트에서 기다려야 한다.
 

 

Output ports


전송 속도보다 데이터그램 도착 속도가 더 빠르다면 버퍼링이 필요하다
scheduling discipline은 전송되길 기다리는 (queued)데이타그램 사이에서 고른다
 

 

 

 

Output port queueing

버퍼가 커지면 라우터의 메모리가 소모될 수 있음
패킷을 저장할 수 있는 메모리가 없을 때 패킷 손실 발생
 

얼마나 많은 버퍼가 필요할까?

버퍼링: B, 평균 왕복 시간: RTT(250msec), C: 링크 용량
B = RTT*C   -> 상대적으로 작은 양의 TCP 흐름에 대한 큐잉 분석
많은 수의 TCP 흐름(n)이 링크를 통과할 때, 필요한 버퍼링은 
R
T
T
∗
C
√
N
이다
 

Input port queuing

입력 회선을 통해 도착하는 모든 패킷을 전송하기에 스위치 구조가 충분히 빠르지 않다면 -> queuing
Head-of-the-Line(HOL) blocking: 

입력 포트에 있는 서로 다른 2개의 패킷이 같은 출력 포트(빨간색)을 향해 간다. 이 중 한 패킷은 차단되고 입력 큐에서 기다려야 한다 => HOL blocking


The Internet network layer


network layer - 3계층
Routing protocol: 패킷이 목적지까지 가는 경로 결정 - static과 dynamic 프로토콜로 구분됨
path selection - 다익스트라, 벨만 포드 등에서 선택
RIP: Routing Information Protocol 
OSPF: Open Shortest Path First          -> 최단 경로 우선 프로토콜
BGP: Border Gateway Protocol           -> 외부 라이팅 프로토콜
 

5계층 -> 4계층 -> 3계층 => 복잡성 낮아짐
ICMP(Internet Control Message Protocol): 인터넷 제어 메시지 프로토콜
오류 메시지를 전송받는데 주로 쓰임(ping)
 

 

IP datagram format


TTL - 라우팅 잘못하면 루프가 생길 수 있는데 TTL이 이를 방지한다.
라우터마다 1씩 감소하고 0이 되면 버려짐
identifier, flags, fragment offset - IP fragment(단편화)와 관계있다.
IP의 새로운 버전인 IPv6는 단편화를 허용하지 않는다.
upper layer(protocol) - 일반적으로 IP 데이터그램이 최종 목적지에 도착했을 때만 사용되는 필드
이 필드 값은 IP 데이터그램에서 데이터 부분이 전달될 목적지의 전송 계층의 특정 프로토콜을 명시한다.\
header checksum - 라우터가 수신한 IP 데이터그램의 비트 오류를 탐지하는데 도움을 줌
 

IP fragmentation, reassembly

모든 링크 계층 프로토콜이 같은 크기 네트워크 계층 패킷을 전달할 수 없다 -> 6장에서 배움
어떤 프로토콜은 큰 데이터그램 전달하는 반면 다른 프로토콜은 작은 것만 전달 가능
MTU(Mszimum Transmission Unit): 링크 계층 프레임이 전달할 수 있는 최대 데이터의 양
링크 타입이 다르면 MTU도 다르다
각 IP 데이터그램은 한 라우터에서 다른 라우터로 전송하기 위해 링크 계층 프레임 내에 캡슐화되므로 링크 계층 프로토콜의 MTU는 IP 데이터 그램의 길이에 엄격한 제약을 둔다.
큰 IP 데이터그램을 net 내에서 분할한다(fragmented)
하나의 데이터그램이 여러 개의 데이터그램으로 나뉨
마지막 목적지에서만 "재조립(reassembled)"됨
IP header bifs는 fragments의 순서와 identify 하기 위해 사용된다
ex)

 

4000 = 3980+20(header)

 

 

 

 

1480(body)+20(header)

 

 

현재 보내야 할 내용은 1020byte 남았으므로 (1020+20)byte 보냄

 

 

fragflag는 마지막 데이터그램만 0으로 표시하여 내용 끝났음을 표시

 

 

 

 

 

 

IP addressing: introduction


IP 주소: 32bit - 호스트와 라우터의 인터페이스 식별
호스트는 일반적으로 네트워크와 연결되는 하나의 링크를 가진다.
호스트 IP가 데이터그램을 보낼 때 이 링크를 통해 데이터 링크를 보낸다
호스트와 physical link 사이의 경계를 '인터페이스'라고 부른다.
라우터의 작업: 한 링크로부터 데이터그램을 수신하여 다른 링크로 전달하는 것
2개 이상의 연결된 링크가 필요
라우터와 이런 링크 사이의 경계 또한 인터페이스라고 함
모든 호스트와 라우터는 IP 데이터그램을 송수신할 수 있으므로 IP는 각 호스트와 라우터 인터페이스가 IP 주소를 갖도록 요구한다.
따라서 기술 면에서 IP 주소는 인터페이스를 포함하는 호스트 라우터보다는 인터페이스와 관련이 있다.
IP 주소: 호스트를 identifier 할 32-bit
인터페이스의 IP 주소 일부는 연결된 '서브넷'이 결정
오른쪽 그림을 보면, 하나의 라우터가 7개의 호스트를 연결한다.
왼쪽 3개의 호스트와 연결된 라우터 인터페이스 모두 223.1.1.xxx 형식의 IP 주소를 갖는다.
즉 동일한 왼쪽 24비트를 사용한다.
또한 4개의 인터페이스가 중계하는 라우터 없이 하나의 네트워크에 서로 연결되어 있다.
이 네트워크는 이더넷 LAN으로 상호 연결되고 이 경우 인터페이스는 이더넷 허브나 이더넷 스위치 또는 무선 액세스 포인터로 상호 연결된다.
세 호스트들의 인터페이스들과 하나의 라우터 인터페이스로 연결된 네트워크는 서브넷을 구성한다고 말한다.
IP 주소체계는 이 서브넷에 223.1.1.0/24라는 주소를 할당해주는데, 여기서 /24는 서브넷 마스크라 부르며 32비트 주소의 왼쪽 24비트가 서브넷 주소라는 것을 가리킨다.
 

 

 

Network prefix and Host number

network prefix는 네트워크 식별, host number는 특정 호스트를 식별(정확히는 네트워크의 인터페이스를 식별)

network prefix가 얼마나 긴지 어떻게 알 수 있을까?
명시적인 정의를 사용한 network prefix (class bassed addressing, A,B,C,D...)
IP 주소의 네트워크 부분을 8,16,24비트로 제한하고 각각을 A,B,C 클래스 네트워크로 분류
network prefix를 유연하게 prefix/netmask로 나타냄. (classless)

Classful IP Addresses의 문제
큰 네트워크에 비해 네트워크 주소가 너무 적음(부족)
2계층 구조는 클래스 A 및 클래스 B 주소가 있는 대규모 네트워크에는 적합하지 않음
Fix #1: subnetting
호스트 ip 주소가 10,000개 필요한데, 클래스 C로는 부족해서 클래스 B를 할당 받으면, 
클래스 B = 2^(32-16) =65,000
그럼 65000-10000개가 낭비됨
 

 

Subnets


IP 주소: 
서브넷 부분 - high order bits
호스트 부분 - low order bits
subnet:
IP 주소의 같은 서브넷 부분을 가지는 디바이스 인터페이스
서로 라우터의 개입 없이 물리적으로 접근 가능
서브넷: 서브넷을 결정하려면 먼저 호스트나 라우터에서 각 인터페이스를 분리하고 고립된 네트워크를 만든다. 이 고립된 네트워크의 종단점은 인터페이스의 끝이 된다. 이렇게 고립된 네트워크 각각을 서브넷이라고 부른다.
인터퍼이스의 IP 주소는 연결된 subnet이 결정한다.
 

Subnetting


문제: 조직에는 독립적으로 관리되는 여러 네트워크가 있다.
solution 1. 각 네트워크 주소를 할당
관리 힘듦
조직 밖에서 각 네트워크로 addressable 해야 함
식별 가능한 identifiable address를 가져야 함
solution 2. IP 주소 구조에 계층 추가 => subnetting
 

 

 

Subnetting의 기본 아이디어

IP 주소에서 호스트 넘버 부분을 subnet numnber와 host number로 나누자

서브넷은 조직 내에서 자유롭게 할당될 수 있음
내부적으로 서브넷은 분리된 네트워크로 다뤄진다
서브넷 구조는 조직 밖에서 볼 수 없다
 

Subnet Masks

라우터와 호스트는 호스트 넘버의 시작을 식별하기 위해 extended network prefix (subnet mask)를 가진다.



" /24 ": subnet mask

-> 32 bits 주소의 왼쪽 24bits가 서브넷 주소라는 것을 가리킴

 

 

 

Classful IP Address의 문제점 3

유연하지 못하다! 
주소가 많이 필요하면 감당하지 못함
Fix #2: Classless Interdomain Routing(CIDR)
 

CIDR - Classless Interdomain Routing

 목표
효율성을 늘리도록 IP 주소를 재구성
라우터 테이블 엔트리를 최소화하기 위해 계층적으로 라우팅 집계
주요 개념: IP 주소의 네트워크 id(prefix)의 길이를 임의로/유연하게 네트워크 계층에 따라 정의하라
결과:
라우터는 포워딩을 위해 IP 주소와 prefix 길이를 사용한다
모든 advertised된 IP 주소는 prefix를 포함해야 한다.
예:
네트워크 주소의 CIDR notation: 192.0.2.0/18
"18"은 첫 18bits가 주소의 네트워크 부분이라는 것을 말함
네트워크 부분을 네트워크 prefix라고 부름
어떤 사이트가 1000 IP 호스트 주소를 지원 가능한 IP network domain이 필요하다고 가정하자.
CIDR을 사용하면, 네트워크는 1024 = 
2
10
(>1000) 주소의 연속된 블락을 할당한다
32-10=22bit long prefix
 

CIDR and Address assignments

backbone ISPs는 IP 주소 공간의 큰 블락을 얻은 후 자신의 고객들에게 주소 블락의 일부분을 재할당한다.
ex)
ISP가 206.0.64.0/18 주소 블락을 소유한다고 가정하자. 16384(
2
32
−
18
)
 IP 호스트 주소를 나타내는
고객이 800 호스트 주소를 요청한다면?
512=
2
9
<800<1024=
2
10
 -> 32-10 =22
a/22 블락 할당. 예: 206.0.68.0/22 -> 고객에게1024(
2
10
)개의 IP 주소 블락을 줌

 

IP addresses: 어떻게 얻을 수 있나?

어떻게 호스트는 IP 주소를 얻나?
한 기관은 ISP로부터 주소 블록을 획득하여, 개별 IP 주소를 기관 내부의 호스트와 라우터 인터페이스에 할당한다.
라우터 인터페이스 주소에 대해서, 시스템 관리자는 라우터 안에 IP 주소를 할당한다
호스트에 IP를 할당하는 것은 일반적으로 동적 호스트 구성 프로토콜(Dynamic Host Configuration Protocol, DHCP)을 더 많이 사용한다.
네트워크 관리자는 해당 호스트가 네트워크에 접속하고자 할 때마다 동일한 ip 주소를 받도록 하거나, 다른 임시 ip 주소를 할당하도록 DHCP를 설정한다.
DHCP는 호스트 IP 주소의 할당뿐만 아니라, 서브넷 마스크, 첫 번째 홉 라우터 주소나 로컬 DNS 서버 주소 같은 추가 정보를 얻게 해 준다.
네트워크에서 자동으로 호스트와 연결해 주는 DHCP 능력 때문에 "plug and play"라고도 한다
 

정적 IP VS 동적 IP

정적 IP - 데스크탑처럼 항상 IP가 변하지 않음 
장점: 정체성이 있음, 항상 들어올 수 있음
단점: 사용성이 떨어짐, 얼마 쓰지도 않으면서 계속 할당받고 있어야 함
동적 IP - 내가 가진 IP가 계속 바뀜
장점: cost 절약
단점: 고정적으로 데이터 받는 서비스 사용 불가
 

 

DHCP

host broadcasts "DHCP 발견" 메시지 [optional]  - 호스트가 DHCP 서버 발견 메시지 발송
DHCP 서버는 "DHCP 제공" msg로 응답 [optional] - 
host는 "DHCP request" msg로 IP 주소 요청
DHCP 서버는 "DHCP ack" msg로 주소 보냄
 

 


1. 새롭게 도착한 호스트는 상호 동작될 DHCP를 발견. 클라이언트는 포트 67번으로 UDP 패킷을 보낸다. UDP 패킷은 IP 데이터그램으로 캡슐화된다.

 

2. 클라이언트가 출발지 IP 주소 0.0.0.0으로 보내면 DHCP가 채워서 IP 할당해서 *보냄

 

 

 

 

 

 

 

 

 

 

 

DHCP 기본 동작 원리

DHCP discover
device가 부팅되면 동일 서브넷에 위치한 DHCP 서버를 찾기 위해 DHCP discover 메시지를 이더넷 망에 브로드캐스팅한다. (IP dest:FF-FF-FF-FF-FF)
DHCP offer
DHCP discover 메시지를 수신한 DHCP 서버는 DHCP offer 메시지를 broadcast 또는 unicast로 클라이언트에게 전송한다. 여기에는 장치(클라이언트)에게 임대해 줄 IP 주소와 자신의 IP 주소가 포함되어 있다.
DHCP request 
클라이언트는 DHCP offer 메시지로부터 받은 네트워크 정보들을 사용하겠다고 요청
DHCP ACK
DHCP 서버는 'DHCP ACK' 메시지를 통해 클라이언트의 IP 주소, Subnet mask, Default gateway IP 주소, DNS 서버 IP 주소, Lease Time(IP 주소 임대 시간)을 전달한다.
 

 

 

 

DHCP: more than IP addresses

DHCP는 서브넷에서 할당받은 IP 주소 외에도 다음 정보를 전달
고객의 first-hop router의 주소
DNS 서버의 이름과 IP 주소
network mask ( network host portion of address)
 

 

DHCP: Example


노트북과 연결하기 위해서는 IP 주소, first-hop router 주소, DNS 서버 주소가 필요하다: use DHCP
DHCP는 UDP로 캡슐화되고, IP로 캡슐화되고, 802.1 Ethernet으로 캡슐화된다.
Ethernet frame은 LAN으로 broadcast(dest:FFFFFFFFFFFF), 작동되는 DHCP 서버에서 받음
Ethernet은 IP demuxed로 demuxed되고, UDP는 DHCP로 demuxed된다.
 

 

unicast: 1대 1 통신
multicast: 1대 다 통신
broadcast: 전체 통신 (원하지 않더라도 모두에게 패킷 다 보냄)
DHCP는 unicast 안됨
why? IP 주소를 모르니까 => 그래서 broadcast 함
 

 


DCP 서버는 클라이언트의 IP 주소, 클라이이언트의 first-hop router의 IP 주소, DNS 서버의 이름 및 IP 주소를 포함하는 DHCP ACK을 공식화한다
DHCP 서버 캡슐화, 클라이언트에 프레임 전달, 클라이언트에서 DHCP로 demuxing
이제 클라이언트는 자신의 IP주소, name, DSN 서버의 IP 주소, 자신의 first-hop router를 알게 된다.
 

 

 

 

 

DHCP 정리

호스트가 네트워크에 접속할 때 서버로부터 IP 주소를 동적으로 얻음
주소가 변할 수 있고, 재사용이 가능하다
 

NAT: Network Address Translation


motivation: 로컬 네트워크는 오로지 한 개의 IP 주소만 가진다.
ISP로부터 필요하지 않은 주소 범위: 모든 디바이스를 위해 단 하나의 IP 주소만 있으면 된다.
바깥 세상과으로부터 독립됨:
밖에 알리지 않고 로컬 네트워크에 있는 디바이스의 주소를 바꿀 수 있다.
로컬 네트워크의 주소를 바꾸지 않고 ISP를 바꿀 수 있다.
로컬 net에 있는 디바이스는 바깥세상에 의해 명시적으로 addressable, visible하지 않는다.
하나의 네트워크 망에서 여러 개의 디바이스들이 존재할 때, 그들 각각에게 실제 IP를 하나씩 주게 되면 IP를 너무 많이 필요로 한다. -> 이를 해결하는 방법이 NAT(네트워크 주소 변환) 
현재 사용 중인 IPv4 주소가 많이 남아있지 않음
implementation: NAT router must:
outgoing datagrams: 모든 나가는 데이터그램의 (출발지 IP 주소, 포트 번호)를 (NAT IP 주소, 새로운 포트 번호 -> 목적지 주소로 사용)로 대체한다.
모든 (출발지 IP 주소, 포트 번호)->(NAT IP 주소, 새로운 포트 번호) 변환 쌍을 NAT translation table에 기록한다.
incoming datagrams: 들어오는 데이터그램의 목적지 필드에 있는 (NAT IP 주소, 새로운 포트 번호)를 NAT 테이블 내의 상응하는 (출발지 IP 주소, 포트 번호)로 바꾼다.

외부에서 보기에는 하나의 IP 주소인(138.76.29.7)만 알고 있다.
NAT 라우터는 ISP의 DHCP 서버로부터 IP 주소를 얻고, NAT-DHCP-라우터로 제어되는 홈 네트워크의 주소 공간에서 DHCP 서버를 실행하여 컴퓨터에게 주소를 제공
16bit의 port-number field:
하나의 LAN 주소로 동시에 60,000개의 연결이 가능
[(WAN side addr) 138.76.29.7, 5001]이랑 [(LAN side addr) 10.0.0.1, 3345]를 바인딩한 것 => flow
60,000개의 flow를 생성할 수 있다는 말
NAT은 논란의 여지가 있다.
라우터는 3계층까지만 처리해야 한다.
end-to-end 법칙을 위반함
host가 중간 노드에서 (IP 주소, 포트 번호) 수정 없이 직접 통신해야 한다는 원칙을 어김
장점: 경제적
단점: 인터넷 원칙을 어김 (smart end, dump middle)
NAT 대신 IPv6로 주소 부족 문제를 해결해야 한다. -> 라고 NAT 사용 반대하는 사람들의 주장
 

NAT traversal problem

 


클라이언트가 10.0.01인 주소를 가지는 서버와 연결하고 싶다면?
이는 LAN의 로컬 주소로 클라이언트가 이를 목적지 주소로 사용할 수 없다.
클라이언트는 오직 138.76.29.7 주소만 알 수 있다.
해결책1: 주어진 포트에서 들어오는 연결 요청을 서버로 전달하도록 NAT을 정적으로 구성
 

 

즉,

NAT Router의 특성: 내부에 있는 클라이언트가 외부로 나가는 요청을 해야 테이블에 해당 정보를 매핑해서 외부와 연결이 됨
문제1: 서버는 클라이언트 요청을 기다리는 역할임으로 테이블이 만들어지지 않음 
NAT side에서 나갈 때만, 주소 변환 쌍이 테이블에 업데이트됨
내부에서 외부로 트래픽이 나갈 때 생성된 NAT 매핑 테이블을 활용하여 외부 트래픽이 내부로 들어오는 것
문제2: 내부 사설 아이피는 사설 인터넷 내에서만 유효하기 때문에 외부에서 접근 불가
해결책1: 특정 서버를 위해 관리자가 NAT 테이블에 서버 정보를 매핑해두는 방식
특정 포트로 들어오는 연결 요청을 서버로 전달(forward) 하도록 NAT을 정적으로 구성
해결책2: Universal Plug and Play(UPnP) Internet Gateway Device(IGD) Protocol. 
UPnP 프로토콜을 사용하여 자동으로 NAT 포트 매핑 테이블을 생성하기
호스트가 가까운 NAT을 발견하고 동적으로 포트 매핑을 자동 설정하는 프로토콜
해결책3: Skype를 사용하여 전달(relaying)
NAT의 클라이언트와 릴레이로 연결을 설정
외부 클라이언트는 릴레이에 연결
릴레이가 두 연결 사이에 패킷을 중계
Skype에서 사용



 

ICMP: Internet control message protocol

호스트와 라우터 사이에서 network-layer 정보를 전달하는 데 사용
에러 보고: 호스트, 네트워크, 포트, 프로토콜에 도달하지 못함
echo request/reply (ping을 사용하여)
IP의 상위인 네트워크 계층:
IP에서 ICMP msg를 운반
ICMP 메시지: Type, code, 에러가 발생한 IP 데이터그램의 첫 8바이트
 

 

Traceroute and ICMP

UDP 세그먼트를 목적지에 보냄
첫 번째 SET은 TTL=1
두 번째 SET은 TTL=2
포트 번호 없음(?)
n번째 데이터그램 set이 n번째 라우터에 도착할 때:
라우터는 데이터그램을 버린다
출발지에 ICMP 메시지를 보냄 (type 11, code 0)
ICMP 메시지는 라우터의 이름과 IP 주소를 포함함
ICMP 메시지가 도착하면, 출발지는 RTT를 기록함
Stopping criteria(출발지가 멈추는 기준):
UDP 세그먼트는 결국 목적지 호스트에 도착함
목적지에서 ICMP "포트가 도착하지 않음" 메시지를 반환함
출발지는 stop!
 

 

IPv6

IPv6: motivation

초기 동기: 32bit 주소 공간이 곧 완전히 할당될 것이다. (남은 게 얼마 없음)
추가적인 동기:
헤더 포멧이 빠른 처리(processing)&전송(forwarding)을 도와줌
헤더는 QoS(Quality of Service)가 용이하도록 도와줌
IPv6 데이터그램 형식:
고정된 길이의 40byte 헤더
IPv4는 20byte
fragmentation 허용 안 함
 

 

IPv6 datagram format

priority: flow 안의 데이터그램 사이의 우선순위를 식별
flow label: 같은 flow 안의 데이터그램을 식별
next header: 데이터를 위한 상위 계층 프로토콜을 식별
IPv4로부터 변화
checksum: 각 hop에서 처리 시간을 줄이기 위해 전체 제거함
options: 허락하지만 헤더 밖에서만. "Next header" field로 나타냄
ICMPv6: ICMP의 새로운 버전
추가적인 메시지 타입. 예: "Packet too big"
multicast group management functions
 

 

 

IPv4에서 IPv6로의 변화

모든 라우터가 동시에 업그레이드될 수 없다.
no "flow days"
어떻게 IPv4와 IPv6를 섞어서 네트워크를 운영할 수 있을까?

 

 

Tunneling


 

 

 

 

 

 

 

IPv4 라우터들이 IPv6 데이터그램을 IPv4의 데이터 필드에 넣어 운반

 
Routing algorithms

 

routing algorithm은 네트워크에서 end-end 경로를 결정한다
forwarding table은 라우터에서 local forwarding을 결정한다.
 

 

그래프와 트리 차이

그래프는 cycling
트리는 acycling
 

다익스트라와 벨만포드 차이

다익스트라: 가중치는 항상 양수
벨만포드: 음의 가중치가 가능
 

Routing algorithm classification

Q: global or decentralized information?
global: 
모든 라우터가 완벽한 topology와 link cost 정보를 가진다.
"link state" 알고리즘
decentralized:
라우터는 물리적으로 연결된 이웃과, 그 이웃까지의 link cost를 안다
이웃과 정보를 교환하며 반복 계산 과정을 거친다
"distance vector" algorithm
Q: static or dynamic?
static:
시간이 지남에 따라 경로가 느리게 변화
라우터 포워딩 테이블을 직접 수정해야 함
dynamic:
빠르게 경로가 변화
정기적인 업데이트
link cost 변경에 대한 응답
 

 

 

Link-State Routing Algorithm

다익스트라(Dijkstra) 알고리즘
모든 노드에게 net topology와 link costs 정보가 알려짐
"link state broadcasting"을 통해 알려짐
모든 노드들은 같은 정보를 갖는다
하나의 노드(출발지)에서 다른 노드(도착지)까지 최소 비용 경로를 연산한다.
해당 노드들에 대해 포워딩 테이블을 제공
k번 반복 연산 후, k까지 가는 최소 비용 경로를 알게 됨
notation:
C(x,y): x에서 y로의 link cost
만약 바로 갈 수 있는 노드가 아니라면 ∞
D(v): 출발지에서 목적지까지 경로의 cost (현재까지 계산한 cost)
P(v): 출발지에서 경로로의 v까지의 경로에서 v의 이전 노드
N': 최소 비용 경로로 정의된 노드들의 집합

 



 
 

 

다익스트라 알고리즘의 complexity

n개의 노드가 있을 때, 모든 노드를 확인해야한다. -> n(n+1)/2번의 비교가 필요하므로 O(
n
2
)의 복잡도를 가진다.
더 효율적으로 구현하면 O(nlogn)이 가능하다.
 

 

 

Distance vector algorithm

벨만 포드 알고리즘 (dynamic programming)
d
x
(
y
)
: x에서 y까지의 최소 비용 경로의 cost
d
x
(
y
)
 = 
m
i
n
v
{c(x,v)+
d
v
(
y
)
}

key idea:
자신의 distance vector estimate를 이웃들에게 보낸다.
x가 이웃으로부터 새로운 DV를 받으면, B-F equation을 이용하여 자신의 DV를 업데이트한다.
Dx(y) ← min{c(x,v) + Dv(y)}  for each node y ∊ N
추정한 
D
x
(
y
)
는 실제 최소 비용인 
d
x
(
y
)
에 수렴한다.

 

iterative, asynchronous:
local link cost가 바뀔때 local iteration이 발생
이웃으로부터 DV 업데이트 메시지 받으면 업데이트
distributed:
각 노드들은 자신의 DV가 변경될 때 이웃에게 알림
 

 

 

 



Distance vector: link cost changes
link cost가 감소한 경우 업데이트가 빠름
t
0
: y가 link cost 변화를 탐지하고 자신의 DV를 업데이트한 후, 이웃들에게 이를 알림
t
1
: z가 y로부터 업데이트 정보를 받고, 자신의 테이블을 업데이트. x로의 최소 비용을 업데이트 한 후, 이웃들에게 자신의 DV 보냄
t
2
: y가 z로부터 업데이트된 정보로를 받고, 자신의 테이블을 업데이트. y의 최소 비용 테이블은 변하지 않았으므로 z에게 메시지를 보내지 않음 => 업데이트 끝!
link cost가 증가한 경우는 업데이트가 느림
z가 x로 갈 때, y를 통한 경로보다 x로 바로 가는 것이 cheap하다는 것을 깨달을 때까지 44번의 반복이 발생 -> 'count to infinity' 문제
poinson reverse를 이용해 문제 해결
Distance vector: poisoned reverse
만약 Z가 X를 얻기 위해 Y를 통해 간다면:
z에서 y 거리를 ∞ 주고 업데이트 하도록 함
즉, 업데이트된 곳 반대를 ∞로 설정해주고 업데이트하면 빠름
poisoned reverse가 infinity problem을 대부분 해결하기는 하나, 세 개 이상의 이웃 노드를 포함한 루프인 경우 감지하지 못한다.
 

 

 

LS와 DV 알고리즘 비교

message complexity
LS: 노드가 n개, 링크가 E개일 때 O(nE)
DV: 이웃끼리만 메시지 교환
수렴 속도
LS: O(
n
2
) 
DV: 수렴 속도 다양
라우팅 루프 발생 가능
count to infinity problem 발생 가능
 

 

 

Hierarchical routing

6억개의 목적지가 있다면?
모든 목적지를 라우팅 테이블에 저장할 수 없음
라우팅 테이블의 변경은 링크를 벅차게 함
administrative autonomy
internet = network of networks
각 네트워크 admin은 자신의 네트워크 내에서 라우팅을 컨트롤하기를 원한다.
라우터를 영역으로 통합, "autonomous systems(AS)"
AS: LG U+, SK, KT 같은 거 
같은 AS 내의 라우터는 같은 라우팅 알고리즘을 사용
"intra-AS" 라우팅 프로토콜
다른 AS에 있는 라우터는 다른 intra-AS 라우팅 프로토콜을 사용
gateway router: 
다른 AS의 라우터에 링크를 가짐 (직접 연결됨)
자신의 AS의 "edge"
 

Interconnected ASes

포워딩 테이블은 intra-AS와 inter-AS 라우팅 알고리즘에 의해 설정된다.
intra-AS은 내부 목적지 엔트리를 설정하고
inter-AS & intra-AS는 외부 목적지 엔트리를 설정한다.

 

 

 

 

 

 

Routing int the Internet

 

 

Intra-AS Routing

interior gateway protocols (IGP)라고도 알려짐
대부분의 흔한 intra-AS 라우팅 프로토콜:
RIP: Routing Information Protocol
OSPF: Open Shortest Path First  => 빠르고 정확
IGRP: Interior Gateway Routing Protocol
 

 

 

RIP

distance vector algorithm
이웃의 더 좋은 정보를 이용하여 업데이트 
RIP table processing
RIP 라우팅 테이블은 route-d라 불리는 application 계층 프로세스에 의해 관리된다.
advertisement는 주기적으로 반복해서 UDP 패킷을 보냄
OSPF

link state 알고리즘 이용 -> 다익스트라 알고리즘으로 경로 연산
OSPF advertisement는 이웃 당 하나의 엔트리를 전달
advertisements는 전체 AS에게 flood
TCP나 UDP 대신에 IP로 직접 OSPF 메시지 전달
IS-IS routing protocol: OSPF와 거의 동일
OSPF "advanced" features (not in RIP)
security: 모든 OSPF 메시지는 인증됨(authenticated) -> 악의적인 침입을 막기 위해
여러개의 같은 cost 경로를 허용 (RIP는 하나의 경로만 허용)
cost가 같은 경로 여러개이면 나눠서 보냄 => 속도↑
각 link에 대해 서로 다른 TOS에 대한 여러 cost 행렬 (예: best effort ToS에 대해 낮음으로 설정된 위성 링크 비용, 실시간 ToS에 대해 높음)
통합된 uni-cast 와 multicast 지원:
Multicast OSPF (MOSPF)는 OSPF 기반의 동일한 토포로지 데이터를 사용한다
계층적인 OSPF in large domains.
 

 

 

 

Hierarchical OSPF


 

two-level hierarchy: local area, backbone.
link-state advertisements는 영역 안에서만 일어남
각 노드에는 자세한 영역 토폴로지가 있다.
다른 지역은 net로 가는 방향(최단 경로)만 안다
area border routers: 자신의 영역 안의 nets까지의 거리를 요약하여 다른 영역 경계 라우터에게 알린다.
backbone routers: 백본으로 제한된 OSPF 라우팅을 실행
boundary routers: 다른 AS에 연결
 

 

Internet inter-AS routing: BGP

BGP(Border Gateway Protocol): 
 

 

 

Broadcast and multicast routing

출발지에서 모든 다른 노드에게 패킷 전달
source 중복은 비효율적:

source duplication: 어떻게 출발지는 수령자 주소를 결정하는가?
 

 

In-network duplication

flooding: 노드가 broadcast 패킷을 받으면, 카피본을 모든 이웃에게 보낸다.
문제: cycles & broadcast storm
controlled flooding: 전에 같은 패킷을 broadcast한 적이 없는 경우에만 패킷을 broadcast한다.
노드는 이미 broadcast한 패킷의 트랙을 저장한다.
또는 reverse path forwarding (RPF): 출발지와 노드 사이의 최단 경로에 도달한 경우에만 패킷 forward
spanning tree:
어떤 노드로부터 중복된 패킷을 받지 않는다.
 

 

* broadcasting: 나와 이전에 보낸 사람 제외하고 보냄 = controlled flooding

* flooding: 나를 제외한 나머지한테 보냄

 

 

 

Spanning tree

먼저 spanning tree 구성
노드는 스패닝 트리를 따라서만 카피하고 forward한다.
 

 

Multicast routing: problem statement

local multicast group members를 가지는 라우터를 연결하는 트리를 찾는다
tree: 사용하는 라우터 사이에 모든 경로가 아니다
shared-tree: 모든 그룹 구성원이 사용하는 같은 트리
source-based: 송신자에서 수신자로의 다른 트리 
