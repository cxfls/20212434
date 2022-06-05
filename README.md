# 리눅스 명령어

**1) top**

리눅스 우분투에서 top 명령어를 사용하여 시스템 사용량을 실시간으로 확인할 수 있다.
옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여줌

<img width="701" alt="스크린샷 2022-06-05 오후 4 20 49" src="https://user-images.githubusercontent.com/106877669/172040467-b4250756-1004-4da1-b03f-16a92936f342.png">


**사용 구문**

top [옵션]

**사용 예시**

-b 옵션을 사용해 순간의 정보를 확인할 수 있다.

<img width="618" alt="스크린샷 2022-06-05 오후 4 35 08" src="https://user-images.githubusercontent.com/106877669/172040507-6bfc3faf-075f-428f-88f3-00b7b59a5ead.png">

-n 옵션을 사용하여 top 실행 주기를 2번 반복하도록 한다.

<img width="618" alt="스크린샷 2022-06-05 오후 4 35 32" src="https://user-images.githubusercontent.com/106877669/172040510-bce8565f-980d-480b-b1cb-1c8fbaab315f.png">

**top 실행 후 명령어**

shift + p : CPU 사용률 내림차순

shift + m : 메모리 사용률 내림차순

shift + t : 프로세스가 돌아가고 있는 시간 순

a : 메모리 사용량에 따라 정렬

b : Batch 모드로 작동

1 : CPU Core별로 사용량 보여줌

**2) ps**

리눅스 우분투에서 ps명령어를 사용하면 현재 실행중인 프로세스 목록을 확인할 수 있다.
여기서 ps는 'process status'의 약자이다.

<img width="618" alt="스크린샷 2022-06-05 오후 4 31 50" src="https://user-images.githubusercontent.com/106877669/172040411-89d1ecd6-ac10-4929-be13-e7b30d67cc67.png">

**사용 구문**

ps [옵션]

**사용 예시**

ps : pid, cmd 등 프로세스의 기본적인 내용만 출력

ps -e : 모든 프로세스 출력

<img width="618" alt="스크린샷 2022-06-05 오후 4 40 05" src="https://user-images.githubusercontent.com/106877669/172040715-6c3dff90-9747-4846-88bf-921c902ded02.png">

ps -f : 풀 포맷으로 출력

ps -l : 긴 포맷으로 출력

ps -p 1 : 프로세스 번호가 1인 프로세스 출력

ps -ef | more : 모든 프로세스를 풀 포맷으로 출력, more 명령어를 이용하여 페이지 단위로 출력

<img width="618" alt="스크린샷 2022-06-05 오후 4 41 41" src="https://user-images.githubusercontent.com/106877669/172040717-e74bc178-cd6a-4179-862c-7ca54bcb0209.png">

**ps와 top의 차이점**
ps는 ps한 시점에서 proc에서 검색한 cpu **사용량**을 출력한다.

top은 proc에서 일정 주기로 합산해 cpu **사용율**을 출력한다.
 
