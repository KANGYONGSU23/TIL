# 2계층에서 하는 일

하나의 네트워크 대역, 즉, 같은 네트워크 상에 존재하는 여러 장비들 중에서 어떤 장비가 어떤 장비에게 보내는 데이터를 전달

추가적으로 **오류제어**, **흐름제어** 수행

2계층은 하나의 네트워크 대역 LAN에서만 통신할 때 사용한다.

# MAC주소 - 2계층에서 사용하는 주소

LAN에서 통할 때 사용하는 주소 (물리적인 주소)

![image](https://github.com/user-attachments/assets/8fc5cfb6-5557-44c2-a8f0-fd582048ec7f)

**OUI**

- IEEE에서 부여하는 일종의 제조회사 식별 ID

**고유번호**

- 제조사에서 부여한 고유번호

# 2계층의 프로토콜

**Ethrenet 프로토콜**

![image](https://github.com/user-attachments/assets/986632be-3320-4dd5-987d-360ab50eeba4)


### Destination Address (목적지 주소)

= 받는 사람의 MAC주소 ( 6byte )

### Source Address (출발지 주소)

= 보내는 사람의 MAC주소 ( 6byte )

### Ethernet Type

= 페이로드안의 내용을 미리 알려주는 역할(2byte)

상위 프로토콜 타입 : IPv4(0x0800), ARP(0x0806)
