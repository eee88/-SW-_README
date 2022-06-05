# git_README

__top__

|Linux 명령어|설명|
|:---:|:---:|
|top|시스템의 상태를 전반적으로 가장 빠르게 파악 가능(CPU, Memory, Process)|


|top 실행 후 명령어|설명|
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
