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


