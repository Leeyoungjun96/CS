# 실제 운영체제의 이해
#### 리눅스 운영체제
* 리눅스 커널(운영체제) + 시스템 프로그램(쉘) + 응용 프로그램
![linux1](../img/linux1.png)
![linux1](../img/linux2.png)

#### 쉘 종류
* 쉘(shell) : 사용자와 컴퓨터 하드웨어 또는 운영체제간 인터페이스
  * 사용자의 명령을 해석해서, 커널에 명령을 요청해주는 역할
  * 관련된 시스템콜을 사용해서 프로그래밍이 작성됨
* 쉘 종류
  * Bourne-Again Shell (bash) : GNU 프로젝트의 일환으로 개발, 리눅스 거의 디폴트
  * Bourne Shell (sh)
  * C Shell (csh)
  * Korn Shell (ksh) : 유닉스에서 가장 많이 사용됨


* process management
  * 응용 프로그램은 여러개의 prcoess로 관리됨 (멀티 프로그래밍)
  * process scheduler
    * process 실행, 종료 관리
    * 인터럽트 처리 관리
* memory management
  * 가상 메모리
    * page 기반 메모리 관리
* IO device management
  * VFS(Virtual File System)
  * file, Device drivers, Network 관리


#### 시스템 프로그램
* 핵심은 쉘
  * bash(Bourne-again shell)
  * 내부는 시스템콜을 호출하도록 구현
* 각 프로그래밍 언어 / 라이브러리 / 시스템 콜
  * 필요시 해당 운영체제의 시스템콜 호출

