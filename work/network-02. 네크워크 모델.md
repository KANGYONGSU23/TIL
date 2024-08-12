# TCP/IP 모델
![image](https://github.com/user-attachments/assets/e9e416a5-36c6-49d1-9228-edc29fa1b709)

# OSI 7계층
![image](https://github.com/user-attachments/assets/42440765-b793-45f7-9cd6-f7c9fc22855e)

## 공통점

- 계층적 네트워크 모델
- 계층간 역한 정의

## 차이점

- 계층의 수 차이
- OSI는 역할 기반, TCP/IP는 프로토콜 기반
- OSI는 통신 전반에 대한 표준
- TCP/IP는 데이터 전송기술 특화

---

# 패킷

네트워크 상에서 전달되는 **데이터를 통칭하는  말**. 네트워크에서 전달하는 데이터의 형식화된 블록이다. 패킷은 제어 정보와 사용자 데이터로 이루어지며 사용자 데이터는 페이로드라고도 한다.
![image](https://github.com/user-attachments/assets/d4504f6d-5a9f-4b15-88d8-4706f633b0db)

## 1. 패킷을 이용한 통신과정

### 캡슐화

여러 프로토콜을 이용해서 최종적으로 보낼 때.

![image](https://github.com/user-attachments/assets/e78e6006-c6e6-445f-9c03-fc2d0f6fb8a2)


### 디캡슐화

여러 프로토콜을 이용해서 최종적으로 받을 때.

![image](https://github.com/user-attachments/assets/0b55059a-8c2e-449b-8ae5-cc4df74e9eab)


## 2. 계층별 패킷의 이름 PDU

*PDU : Protocol Data Unit

**세그먼트**

- 4계층의 PDU ( TCP + 패킷의 형태)

**패킷**

- 3계층의 PDU (IPv4 + 패킷의 형태)

**프레임**

- 2계층의 PDU (Ethernet + 패킷의 형태)
