## 1주차 BE wil
## 웹과 HTTPS, REST API

### 1. 학습내용
#### 웹
전 세계 컴퓨터와 기기를 연결하는 글로벌 네트워크인 *인터넷* 위에서 동작하는 *웹* 서비스

웹에서 컴퓨터 간의 통신이 이루어지는 대표적인 방식 중 하나는 **클라이언트 - 서버 모델**
클라이언트는 요청을 보내고, 서버는 요청을 받아 처리하고 응답을 보낸다.

**URL**: 웹 상에서 특정 자원의 위치를 나타내는 주소
> http(scheme)://www.example.com(Host):5883(Port)/(path)(?Query)

scheme(protocol): 데이터를 주고받는 통신 규약 <br>
host: 리소스가 위치한 서버의 IP주소 혹은 도메인 <br>
port: 서버의 특정 네트워크 포트번호 <br>
path: 원하는 리소스의 경로 <br>
query: ? 뒤로 따르는 key-value 형식의 추가 정보 <br>

#### HTTP
**HTTP 요청**
start line + headers + body 

주요 메서드 <br>
*GET*: 리소스 조회 <br>
*POST*: 리소스 추가 등록 <br>
*PUT*: 리소스 교체, 없으면 생성 <br>
*PATCH*: 일부를 수정 <br>
*DELETE*: 삭제 <br>

#### API/REST API
**API**: 한 프로그램이 다른 프로그램의 기능이나 데이터를 사용할 수 있도록 정해둔 규칙(클라이언트와 서버의 요청과 응답 방식을 미리 정해 둔 규칙과 기능의 목록)<br>

**REST**: HTTP의 장점을 최대한 활용할 수 있는 네트워크 아키텍쳐 스타일
>구성요소
1. 자원(URI): 모든 자원은 고유한 ID를 가지며, 이 ID는 HTTP URI이다.
2. 행위(Method): 자원을 조작하기 위해 HTTP메서드를 사용한다.
3. 표현: 서버와 클라이언트가 데이터를 주고받는 형식, 일반적으로 JSON형식

>REST API: 레스트를 기반으로 설계한 API


### 2. 에러페이지 스크린샷
![screenshot](./becap2.png)

### 3. API 명세서 

>상품기능

1. 상품 정보등록<br>
HTTP Method: POST <br>
URI: /item
2. 상품 목록 조회<br>
HTTP Method: GET<br>
URI: /item
3. 개별 상품 정보 상세 조회<br>
HTTP Method: GET<br>
URI: /item/{itemId}
4. 상품 정보 수정<br>
HTTP Method: PATCH<br>
URI: /item/{itemId}
5. 상품 삭제<br>
HTTP Method: DELETE<br>
URI: /item/{itemId}

>주문 기능
1. 주문 정보 생성<br>
HTTP Method: POST<br>
URI: /order
2. 주문 목록 조회<br>
HTTP Method: GET<br>
URI: /order
3. 개별 주문 정보 상세 조회<br>
HTTP Method: GET<br>
URI: /order/{orderId}
4. 주문 취소<br>
HTTP Method: PATCH<br>
URI: /order/{orderId}