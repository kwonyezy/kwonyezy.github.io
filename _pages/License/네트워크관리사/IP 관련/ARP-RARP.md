---
title: "ARP/RARP"
tags:
    - License
    - 네트워크관리사
    - 필기
    - 이론
date: "2024-06-24"
thumbnail: ""
bookmark: true
---

\* IP 주소와 MAC 주소 간의 매핑을 관리하는 데 중요한 역할을 하는 프로토콜

# ARP
---

>\> Address Resolution Protocol
>\> IP 주소 => 호스트의 MAC 주소를 찾는 프로토콜
>   (네트워크에서 통신하기 위해서는 IP주소와 함께 MAC 주소(데이터링크계층) 필요)
>\> 예시 : 192.168.1.1에 패킷을 보내기 위해 ARP 요청을 보내고, 해당 호스트가 MAC 주소 00:1A:2B:3C:4D:5E를 응답


# RARP
---

>\> Reverse Address Resolution Protocol
>\> MAC 주소 => 호스트의 IP 주소를 찾는 프로토콜
>   (디스크 없는 워크스테이션이나 초기 부팅 과정에서 자신의 IP 주소를 모르는 경우 사용)
>\> 예시 : MAC 주소 00:1A:2B:3C:4D:5E를 RARP 서버에 보내고, 서버는 해당 MAC 주소에 할당된 IP 주소 192.168.1.1을 응답
