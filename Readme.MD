# Windows 11에 WSL2 및 Ubuntu 설치하기
---
### Linux용 Windows 하위 시스템, 가상머신 플랫폼 설치
* Power Shell을 관리자 권한으로 실행 후 다음 명령어 실행
```sh
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
* 설치 완료후 재부팅

### WSL 설치
* power shell을 관리자 권한으로 실행 후 다음 명령어 실행
~~~
wsl.exe --install # WSL 설치
wsl.exe --update # 최신 버전으로 업데이트
wsl --set-default-version 2 # WSL2을 기본 버전으로 설정
~~~

### Ubuntu 24 설치
* power shell을 관리자 권한으로 실행 후 다음 명령어 실행
~~~
# 설치 가능 목록 확인
wsl.exe --list --online


~~~
