## 오픈소스SW개론 과제2 (컴퓨터공학과 20212434 이채린)

---
**리눅스 명령어**



**1) top**

    리눅스 우분투에서 top 명령어를 사용하여 시스템 사용량을 실시간으로 확인할 수 있다.
    옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여준다.

<img width="701" alt="스크린샷 2022-06-05 오후 4 20 49" src="https://user-images.githubusercontent.com/106877669/172040467-b4250756-1004-4da1-b03f-16a92936f342.png">



**사용 구문**

    top [옵션]


**사용 예시**

* -b 옵션을 사용해 순간의 정보를 확인할 수 있다.

<img width="618" alt="스크린샷 2022-06-05 오후 4 35 08" src="https://user-images.githubusercontent.com/106877669/172040507-6bfc3faf-075f-428f-88f3-00b7b59a5ead.png">

* -n 옵션을 사용하여 top 실행 주기를 2번 반복하도록 한다.

<img width="618" alt="스크린샷 2022-06-05 오후 4 35 32" src="https://user-images.githubusercontent.com/106877669/172040510-bce8565f-980d-480b-b1cb-1c8fbaab315f.png">


**top 실행 후 명령어**

|명령어|설명|
|----|----|
|shift + p|CPU 사용률 내림차순|
|shift + m|메모리 사용률 내림차순|
|shift + t|프로세스가 돌아가고 있는 시간 순|
|a|메모리 사용량에 따라 정렬|
|b|atch 모드로 작동|
|1|CPU Core별로 사용량 보여줌|

---

**2) ps**

    리눅스 우분투에서 ps명령어를 사용하면 현재 실행중인 프로세스 목록을 확인할 수 있다.
여기서 ps는 'process status'의 약자이다.

<img width="618" alt="스크린샷 2022-06-05 오후 4 31 50" src="https://user-images.githubusercontent.com/106877669/172040411-89d1ecd6-ac10-4929-be13-e7b30d67cc67.png">


**사용 구문**

    ps [옵션]


**사용 예시**

|명령어|설명|
|----|----|
|ps| pid, cmd 등 프로세스의 기본적인 내용만 출력|
|ps -e|모든 프로세스 출력|

<img width="618" alt="스크린샷 2022-06-05 오후 4 40 05" src="https://user-images.githubusercontent.com/106877669/172040715-6c3dff90-9747-4846-88bf-921c902ded02.png">

|명령어|설명|
|----|----|
|ps -f|풀 포맷으로 출력|
|ps -l|긴 포맷으로 출력|
|ps -p 1|프로세스 번호가 1인 프로세스 출력|
|ps -ef \ more|모든 프로세스를 풀 포맷으로 출력, more 명령어를 이용하여 페이지 단위로 출력|

<img width="618" alt="스크린샷 2022-06-05 오후 4 41 41" src="https://user-images.githubusercontent.com/106877669/172040717-e74bc178-cd6a-4179-862c-7ca54bcb0209.png">


**ps와 top의 차이점**
* ps는 ps한 시점에서 proc에서 검색한 cpu **사용량**을 출력한다.

* top은 proc에서 일정 주기로 합산해 cpu **사용율**을 출력한다.

---

**3) jobs**

    현재 세션의 작업 상태를 출력한다.

<img width="612" alt="스크린샷 2022-06-05 오후 6 23 19" src="https://user-images.githubusercontent.com/106877669/172044093-16fc8be9-b7c2-426f-a25c-bc6f2d7bab18.png">


**사용 구문**

    jobs [옵션] [jobID]


**사용 예시**

|명령어|설명|
|----|----|
|-l|프로세스 그룹 ID를 state 필드 앞에 출력한다.|
|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력한다.|
|-p|각 프로세스 ID에 대해 한 행씩 출력한다.|
|command|지정한 명령어를 실행한다.|

---
 
**4) kill**

    리눅스 우분투에서 kill 명령어는 대게 프로세스를 죽일 때 사용한다. 그러나 kill은 원래 내부적으로는 프로세스에 시그널을 보내 원하는 작엽을 하게 하는 명령어이다.


**사용 구문**

    kill [옵션] [pid]

    예를 들어 실행중인 특정 프로세스를 죽이고 싶다면 ps 명령어를 통해 해당 프로세스의 pid를 얻고 kill 명령어의 파라미터로 넘겨 실행하면 프로세스를 종료시킬 수 있다.

<img width="612" alt="스크린샷 2022-06-05 오후 6 24 15" src="https://user-images.githubusercontent.com/106877669/172044099-083116f0-2381-402a-ba14-bd584f1ec346.png">


**사용 예시**

* pid가 '12345'인 프로세스를 종료

>kill 12345

* pid가 '12345'인 프로세스를 강제 종료

>kill -9 12345 또는 kill -SIGKILL 12345

* kill 명령어에서 지원하는 시그널 목록을 출력
>kill -l

---

**vim 에디터에서 매크로 활용방법**


* **매크로 저장하기**

   사전 조건 : [Normal / Command 모드]

q<저장할 매크로 문자>

<img width="612" alt="스크린샷 2022-06-05 오후 5 15 50" src="https://user-images.githubusercontent.com/106877669/172041843-29b5ee78-a848-42b3-adb7-663d4c59c0f9.png">

<img width="612" alt="스크린샷 2022-06-05 오후 5 15 41" src="https://user-images.githubusercontent.com/106877669/172041846-d5dfe489-e0c1-42b3-ac84-8638b8f693b3.png">

-동작 수행-

**q**

    ex) a문자에 매크로 내용을 기록하기 : qa -> 매크로 작성 -> q

---

* **매크로 사용하기**

**1) 특정 문자에 저장한 매크로 실행**

    @<저장한 매크로 문자>

**2) 매크로 반복 실행**

    반복실행@<저장한 매크로 문자>

**3) 마지막에 수행한 매크로 실행**

    @@

---

* **파일에 저장하기(재사용)**

**1. 현재 편집중 내용을 저장 후 ~/.vimrc를 열기(:e 또는 :r)**

    :w

    :e~/.vimrc

**2. insert모드 전환 후 저장할 매크로 이름을 변수로 하여 사용한 매크로 저장하기**

    i / a

    let@<변수명>='cntl + r ctrl + r <마지막 사용 매크로 문자>'

<img width="612" alt="스크린샷 2022-06-05 오후 5 25 26" src="https://user-images.githubusercontent.com/106877669/172042102-1056960e-042d-4de9-a045-5bc108747eb6.png">

    :wq! 또는 x

    *주의 : let@변수명='임의의 문자 - 사용자가 해석할 수 없음'
