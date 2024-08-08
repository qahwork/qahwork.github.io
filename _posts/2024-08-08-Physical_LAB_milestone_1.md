---
title: 'Physical LAB milestone part1'
date: 2024-08-08
permalink: /posts/2024/08/CCNA_FEEDBACK_1/
tags:
  - MILESTONE PROJECT 1
  - Dell R630
  - cisco catalyst 3750
---
## 서론
이번 마일스톤 프로젝트는 물리 장치에 익숙해짐과 동시에 현실적인 랩 실험을 달성하기 위해 진행되었습니다. 이 프로젝트에서는 Dell R630 서버와 Cisco Catalyst 3750G 스위치를 사용하여 서버를 운용해보고자 합니다.

## LAB Architecture
LAB Architecture<br/><img src='/images/Drawing1.png'>
위의 다이어그램은 LAB 아키텍처를 보여줍니다. 각 구성 요소의 역할은 다음과 같습니다:
- **Dell R630(MAIN SWITCH)**: 전체적인 네트워크를 통합적으로 관리합니다.
- **Cisco Catalyst 3750(SW3)**: 
- **Dell R630(SERV3)**: ESXI및 각종 어플리케이션을 동작시키려합니다.

## 구현 단계
1. **설치 및 설정**: 
선은 서버의 구성에 맞춘 길이로 재단하기 위해 직접 5e utp cable을 이용하여 제작하였습니다. TIA/EIA-568-B.1-2001 T568A Wiring, TIA/EIA-568-B.1-2001 T568B Wiring 두가지 형식을 이용하였고. 양측이 A타입인 다이렉트 케이블 5개와 A와B타입인 크로스케이블 2개를 제작하였습니다. 각각 스위치 서버와 스위치 스위치 간의 연결을 위해 이용했습니다.

2. **네트워크 구성**: VLAN 설정 및 IP 주소 배정 방법을 상세히 설명합니다.
3. **테스트 및 검증**: 설정 후 수행한 테스트와 결과를 공유합니다.

## Troble shooting


## 결론
Dell R630 서버와 Cisco Catalyst 3750G 스위치를 이용하여 서버를 구성하고 기본적인 설정을 완료하였습니다. 이후 ESXI와 추가적인 설정을 하려합니다.

## 참고 자료
- [\[참고 링크 1\]](https://en.wikipedia.org/wiki/Category_5_cable)
- [참고 링크 2]