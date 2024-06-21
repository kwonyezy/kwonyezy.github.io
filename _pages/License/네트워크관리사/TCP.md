---
title: "TCP"
tags:
    - License
    - 네트워크관리사
    - 필기
    - 이론
date: "2024-06-19"
thumbnail: ""
bookmark: true
---


# TCP/UDP
---

## TCP 헤더 영역

<table>
  <tr>
    <th>0 ~ 3</th>
    <th>4 ~ 9</th>
    <th>10</th>
    <th>11</th>
    <th>12</th>
    <th>13</th>
    <th>14</th>
    <th>15</th>
    <th>16 ~ 31</th>
  </tr>
  <tr>
      <td colspan="8">Source Port <br> 송신쪽 포트 번호</td>
      <td>Destination Port <br> 목적지 포트 번호</td>
  </tr>
  <tr>
      <td colspan="9">Sequence Number <br> 송신용 순서 번호</td>
  </tr>
  <tr>
      <td colspan="9">ACK <br> 응답 확인 번호 <br> 수신 측에 맞춰 송신 측에서 데이터의 크기를 적절하게 조절하는 필드 <br> Sliding Window </td>
  </tr>
  <tr>
      <td>HLEN (Data Offset) <br> 헤더의 길이</td>
      <td>Reserved <br> 예약</td>
      <td colspan="6">플래그비트</td>
      <td>Window Size <br> 한번에 전송할 수 있는 크기</td>
  </tr>
  <tr>
      <td colspan="8">Checksum <br> TCP헤더와 데이터가 제대로 전송됐는지 검사하는 영역</td>
      <td>Urgent Pointer <br> 긴급 전송 시 사용</td>
  </tr>
  <tr>
      <td colspan="9">Option <br> 선택 가능</td>
  </tr>
  <tr>
      <td colspan="9"> DATA </td>
  </tr>
</table>


## TCP와 UDP 비교 정리

| |TCP|UDP|
|-|---|---|
| |양방향 전송|단방향 전송 (일반향성)|
| |수신 측의 인증 필요 (수신 도착 시 패킷을 순서대로 재조정, 에러 있을 경우 송신자에게 재전송 요구)|수신 측의 인증 불필요|
| |UDP에 비해 오버헤드가 높음|최소한의 오버헤드를 갖는 작은 헤더를 가짐|
|목적|대량의 데이터 및 중요 데이터 전송 시 사용|단순 메시지 전송|
|신뢰성|있음 (속도느림)|없음 (속도빠름)|
|연결|논리적 연결 (연결형 서비스)|비논리적 연결 (비연결형 서비스)|
|전송기능|Byte Stream|Datagram|
|응용계층|FTP(21), Telnet(23), SMTP(25), HTTP(80)|DNS(53), SNMP(161), TFTP(69), NFS|

