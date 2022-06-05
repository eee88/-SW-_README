# git_README

__top__

|Linux 명령어|설명|
|:---:|:---:|
|top|시스템의 상태를 전반적으로 가장 빠르게 파악 가능(CPU, Memory, Process)|


|top 옵션|설명|
|:---:|---|
|shift + p|CPU 사용률 내림차순|
|shit + m|메모리 사용률 내림차순|
|shift + t|프로세스가 돌아가고 있는 시간 순|
|-k|kill. k 입력 후 PID 번호 작성. signal은 9|
|-a|메모리 사용에 따라 정렬|
|-b|배치 모드에서 시작|
|-c|명령어 대신 명령어 라인을 보여줌|
|-d|업데이트 간격을 조정|
|-h|도움말|
|-H|모든 개별 쓰레드가 보여짐|
|-i|좀비(zombie) 또는 Idle 상태의 것들은 무시됨|
|-m|VIRT 대신 USED를 보고|
|-M|메모리 유닛(K/M/G)을 보여줌|
|-n|반복의 최대 수를 지정|
|-P|지정된 프로세스 ID들만 보여줌|
|-s|보안 모드로 시작|
|-S|누적 시간 모드로 시작. 활성화되면 각 프로세스는 CPU를 사용한 시간과 함께 출력|
|-u|지정된 유효 사용자에 의한 프로세스만 보여줌|
|-U|지정된 사용자에 의한 프로세스만 보여줌. 사용자는 실제, 유효한, 저장된 및 파일시스템 UID를 의미|
|-v|프로그램 라이브러리 버전을 출력|


![linux_top](https://user-images.githubusercontent.com/102000890/172051703-09952ee2-2a7c-410b-b8ea-ab402ea7179a.png)


##### 설명

21:59:40 : 현재 서버의 시간

10:59 : uptime(켜져 있는 시간)

0 users : 유저

load average : 현재 시스템이 얼마나 일을 하고 있는지 1분, 5분, 15분 단위로 실행/대기 중인 프로세스 수를 나타내고 있음

Tasks : 프로세스 개수



##### 프로세스 상태 정보

PID : 프로세스 ID (PID)

USER : 프로세스를 실행시킨 사용자 ID

PRI : 프로세스의 우선순위 (priority)

NI : NICE 값. 일의 nice value값이다. 마이너스를 가지는 nice value는 우선순위가 높음.

VIRT : 가상 메모리의 사용량(SWAP + RES)

RES : 현재 페이지가 상주하고 있는 크기(Resident Size)

SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.

S : 프로세스의 상태 [S(sleeping), R(running), W(swapped out process), Z(zombies)]

%CPU : 프로세스가 사용하는 CPU의 사용율

%MEM : 프로세스가 사용하는 메모리의 사용율

COMMAND : 실행된 명령어

---

__ps__

|Linux 명령어|설명|
|:---:|:---:|
|ps|현재중인 프로세스의 목록을 보는 명령어|


|ps 옵션|설명|
|:---:|---|
|-e|모든 프로세스를 출력해 준다|
|-f|풀 포맷으로 보여준다(UID, PID 등)|
|-l|긴 포맷으로 보여준다|
|p, -p|특정 PID의 프로세스를 보여준다|
|-u|특정 사용자의 프로세스를 보여준다|


![linux_ps](https://user-images.githubusercontent.com/102000890/172053999-88c7edba-682f-42ab-bb43-1644111546b3.png)


pid, cmd 등 기본적인 내용만 출력된다. 옵션 없이는 잘 사용하지 않는다.

---

__jobs___

|Linux 명령어|설명|
|:---:|:---:|
|jobs|리눅스/유닉스 시스템에서, 백그라운드로 실행되고 있는 프로세스를 조회하는 명령어|


|ps 옵션|설명|
|:---:|---|
|-l|프로세스 그룹 ID를 state 필드 앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
|-p|각 프로세스 ID에 대해 한 행씩 출력|
|command|지정한 명령어를 실행|


|상태|설명|
|:---:|---|
|Running|작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임을 뜻한다|
|Done|작업이 완료되어 0을 반환하고 종료했음을 뜻한다|
|Done (code)|작업이 정상적으로 완료했으며, 0이 아닌 코드를 반환했음을 뜻한다|
|Stopped|작업이 일시 중단됨을 뜻한다|
|Stopped (SIGTSTP)|SIGTSTP 신호가 작업을 일시 중단했음을 뜻한다|
|Stopped (SIGSTOP)|SIGSTOP 신호가 일시 중단했음을 뜻한다|
|Stopped (SIGTTIN)|SIGTTIN 신호가 작업을 일시 중단했음을 뜻한다|
|Stopped (SIGTTOU)|SIGTTOU 신호가 작업을 일시 중단했음을 뜻한다|

---

__kill__

|Linux 명령어|설명|
|:---:|:---:|
|kill|프로세스에 시그널을 보내 원하는 작업을 하게 하는 명령어|


|kill 옵션|설명|
|:---:|---|
|SIGHUP(HUP)|hang up의 약자. 프로세스를 재시작시키는 시그널|
|SIGINT(INT)|인터럽트. 실행을 중지시킨다|
|SIGQUIT(QUIT)|키보드의 종료|
|SIGKILL(KILL)|무조건 종료. 강제종료시키는 시그널|
|SIGTERM(TERM)|Terminate의 약자로 가능한 정상 종료시키는 시그널|
|CONT|Continue. STOP 등에 의해 정지된 프로세스를 다시 실행|
|STOP|무조건적, 즉각적 정지|
|TSTP|실행 정지 후 다시 실행을 계속하기 위하여 대기시키는 시그널|
