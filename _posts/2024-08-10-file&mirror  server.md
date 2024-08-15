---
title: '우분투 APT미러서버 구축'
date: 2024-08-10
permalink: /posts/2024/08/LAB/
tags:
  - ubuntu 20.04LTS
  - APT Mirror server
  - FIle
  - NETWORK
---
해당 미러서버의 구축 요인은 시스코 3750G 스위치의 nat 미지원으로 인해 ios 라우터를 이용하였지만 속도저하가 심하여 파일의 다운로드나 apt update의 속도가 매우 저하되어 구축하게 되었다. 

opnsense나 리버스프록시를 이용하려고도 생각해보았지만 임시적으로 해당 방법을 이용하여 임시적으로 해결하려한다. 또한 임시적으로 라우터에 부여된 공인ip를 해당 서버에 부여하여 이용하였다.

해당 설치환경은 dell R630서버 / ubuntu server 20.04.06LTS 이다.

[launchpad.net](https://launchpad.net/) 에서 unbuntu -> cd / archive mirror 선택

파티셔닝의 경우 총500G로 /에 20G부여 /var(apt mirror data)에 480G부여 로 진행하였다.


[ubuntu.com](https://ubuntu.com/server/docs/configuring-networks) 를 참고해 ip를 부여했다.
```bash
```
```bash
sudo apt update  
sudo apt upgrade -y
```
최신화를 시켜준다
```bash
sudo apt install apt-mirror
```
미러링을 쉽게 도와주는 도구를 설치한다. 해당 깃허브이다. 
[apt-mirror.github](https://apt-mirror.github.io/)

```bash
sudo vi /etc/apt/mirror.list
```
미러서버 리스트를 바꿔준다. 빠른곳으로
[askubuntu.com](hhttps://askubuntu.com/questions/401941/what-is-the-difference-between-security-updates-proposed-and-backports-in-etc) 이글을 참고해 주석처리된 부분을 수정할지 결정하였다.(간단하게 proposed는 베타기능 backports는 호환성무시 최신업데이트이다.)
src의 경우 소스패키지에 직접 접근하는 건데 이는 미러서버 이용자가 이러한 부분이 필요한 경우 살려놓도록 하자.

```bash
set base_path /var/spool/apt-mirror
sudo apt-mirror
```
설치를 원하는 경로를 지정하고 apt mirror를 가동시키자.
<br/><img src='/images/mirror.png'>

```bash
sudo vi /etc/apt/sources.list
```
설치완료후 이용할 클라이언트에서 수정해주면 된다.

정기적으로 업데이트하려고 할시 cron을 추가적으로 설정해주면되는데 이설정은 따로 하지않았다. 방법은 아래와 같다.
```bash
sudo crontab -e
# 아래 명령어는 2시에 실행해 달라는 명령어이다. 필요시 추가하자
0 2 * * * /usr/bin/apt-mirror >& /var/spool/apt-mirror/var/cron.log
```


