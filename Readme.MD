# Windows 11에 WSL2 및 Ubuntu 설치하기
---
### Linux용 Windows 하위 시스템, 가상머신 플랫폼 설치
* 윈도우의 화면 아래쪽의 '검색' 필드에 '제어판'을 입력하여 '제어판'을 실행
* 프로그램 및 기능 화면으로 이동 후 'Windows 기능 켜기/끄기' 실행 
* 'Linux용 Windows 하위 시스템'과 'Virtual Machine Platform' 체크 후 확인
  - 이미 되어 있다면 Uncheck 후 확인하고 재부팅 후 다시 시도
  - '필요한 파일 다운로드' 화면이 나타나면 '다운로드'를 진행함
* Power Shell을 관리자 권한으로 실행 후 다음 명령어 실행
* 설치 완료후 재부팅

### WSL 설치
* 다음과 같이 wsl 업데이 사이트에 설치 파일을 다운로드 받아 실행함
  - https://github.com/microsoft/WSL/releases
  - 위의 사이트에서 최신 버전의 Assets 에서 x64 용 msi 설치 파일을 다운로드받아서 실행- 파일명 예: wsl.2.5.7.0.x64.msi 
* power shell을 관리자 권한으로 실행 후 다음 명령어 실행
```sh
wsl.exe --install # WSL 설치
wsl.exe --update # 최신 버전으로 업데이트
wsl --set-default-version 2 # WSL2을 기본 버전으로 설정
```

### Ubuntu 24 설치
* power shell을 관리자 권한으로 실행 후 다음 명령어 실행
```sh
# 설치 가능 목록 확인
$ wsl.exe --list --online

NAME                            FRIENDLY NAME
AlmaLinux-8                     AlmaLinux OS 8
AlmaLinux-9                     AlmaLinux OS 9
AlmaLinux-Kitten-10             AlmaLinux OS Kitten 10
Debian                          Debian GNU/Linux
FedoraLinux-42                  Fedora Linux 42
SUSE-Linux-Enterprise-15-SP5    SUSE Linux Enterprise 15 SP5
SUSE-Linux-Enterprise-15-SP6    SUSE Linux Enterprise 15 SP6
Ubuntu                          Ubuntu
Ubuntu-24.04                    Ubuntu 24.04 LTS
archlinux                       Arch Linux
kali-linux                      Kali Linux Rolling
openSUSE-Tumbleweed             openSUSE Tumbleweed
openSUSE-Leap-15.6              openSUSE Leap 15.6
Ubuntu-18.04                    Ubuntu 18.04 LTS
Ubuntu-20.04                    Ubuntu 20.04 LTS
Ubuntu-22.04                    Ubuntu 22.04 LTS
OracleLinux_7_9                 Oracle Linux 7.9
OracleLinux_8_7                 Oracle Linux 8.7
OracleLinux_9_1                 Oracle Linux 9.1

$ wsl.exe --install -d Ubuntu-24.04
```


