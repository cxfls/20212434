# 리눅스 명령어

**1) top**

리눅스 우분투에서 top 명령어를 사용하여 시스템 사용량을 실시간으로 확인할 수 있다.
옵션 없이 입력하면 interval 간격(기본 3초)으로 화면을 갱신하며 정보를 보여줌

[Uploading 스크린샷 2022-06-05 오후 4.20.49.png…]()

**top 실행 전 옵션**
-b 옵션을 사용해 순간의 정보를 확인할 수 있다.
-n 옵션을 사용하여 top 실행 주기를 2번 반복하도록 한다.

**top 실행 후 명령어**
shift + p : CPU 사용률 내림차순
shift + m : 메모리 사용률 내림차순
shift + t : 프로세스가 돌아가고 있는 시간 순
a : 메모리 사용량에 따라 정렬
b : Batch 모드로 작동
1 : CPU Core별로 사용량 보여줌
