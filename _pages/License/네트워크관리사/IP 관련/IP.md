---
title: "IP"
tags:
    - License
    - 네트워크관리사
    - 필기
    - 이론
date: "2024-06-19"
thumbnail: ""
bookmark: true
---


# IP
---
IP주소란 TCP/IP 네트워크 모델 구조에서 컴퓨터를 식별하기 위해 사용하는 것


## IP 헤더

<table>
  <tr>
    <th>0 ~ 3bit</th>
    <th>4 ~ 7bit</th>
    <th>8 ~ 15bit</th>
    <th>16 ~ 18bit</th>
    <th>19 ~ 31bit</th>
  </tr>
  <tr>
    <td>Version (VER) <br> IP 프로토콜 버전</td>
    <td>Header Length (HLEN) <br> 헤더의 길이</td>
    <td>Type of Service (TOS) <br> 서비스 등급 유형</td>
    <td colspan="2">Total Length <br> 헤더 + 데이터의 전체 크기</td>
  </tr>
  <tr>
    <td colspan="3">Identification (식별자) <br> 상위 계층으로 데이터 전달 시 참고하는 정보</td>
    <td>Flags DF, MD <br> 패킷 분할 관련</td>
    <td>Fragment offset (분할간격) <br> 몇번째 분할인지 기억</td>
  </tr>
  <tr>
      <td colspan="2">Time to live (TTL) <br> 패킷 지속 시간</td>
      <td>Protocol <br> 상위 프로토콜의 정보 표시</td>
      <td colspan="2">Header Checksum <br> 헤더 검사 영역 <br> 하위 데이터의 문제 확인, IP헤더의 완전성 검사, 필드를 '0'으로 하여 계산</td>
  </tr>
  <tr>
      <td colspan="5">Source IP Address <br> 송신 측 IP 주소 (32bit)</td>
  </tr>
  <tr>
      <td colspan="5">Destination IP Address <br> 수신 측 IP 주소 (32bit)</td>
  </tr>
  <tr>
      <td colspan="5">Options (IP Option) <br> 보안, 패킷을 전달하는 방식 등 다양한 옵션 지정 영역</td>
  </tr>
  <tr>
      <td colspan="5"> DATA </td>
  </tr>
</table>



## IP 주소 체계
주소 체계에 따라 IPv4와 IPv6로 구분되며, Internet Protocol Version의 약어

|IPv4|IPv6|
|----|----|
|브로드캐스트, 유니캐스트, 멀티캐스트|애니캐스트, 유니캐스트, 멀티캐스트|
|브로드캐스트는 과부하를 많이 발생 시킴|애니캐스트로 대체하여 과부하 저하|
| |IETF(국제 인터넷 표준화 기구)에서 채택 <br> IP 주소의 확장, 호스트 주소 자동 할당 <br> 등급별, 서비스별로 패킷을 구분할 수 있어 품질보장이 용이|
|예시 : 192.168.100.100 <br> 8비트씩 4부분 (32비트) 으로 10진수로 표시 <br> 0~255까지 표현|예시 : 2001:0230:abcd:ffff:0000:0000:ffff:1111 <br> 16비트씩 8부분 (128비트) 으로 16진수로 표시|

