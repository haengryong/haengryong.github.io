# Network packet analysis 
> generate and matain by 김행룡

### 0. 들어가기 앞서
이 홈페이지는 제가 이번 VMT 과제를 진행하면서 조사한 네트워크 패킷 분석 방법과, 제 나름대로의 분석 결과를 포함하고 있는 결과물입니다.
글이 전문적이지 않을 수도 있고 **틀린 정보가 포함되어 있을 수도 있습니다.**

### 1. 패킷이란
패킷은 한번에 전송되는 데이터의 단위입니다. 
> 왜 패킷을 사용해야만 할까요?

100MB크기의 데이터를 전송하고자 할때 분할된 형태가아닌 파일 통째로 보냈다고 가정해봅시다. 

100MB크기의 파일을 아무런 오류없이 전송이 되었다면 다행이겠지만, 전송도중 잘못된 데이터가 1개만 잘못 되어도 오류가 발생하기 때문에 처음부터 다시 100MB를 전송해야 합니다. 

하지만 이 패킷을 이용해 파일을 1MB씩 나누어 전송하면, 1번 패킷 전송 - 수신체크 이러한 과정을 100번하게 되는데, 만일 중간에 오류가 나면 그 번호의 패킷만 재전송하면 되므로 전자에훨씬 효율적이라고 할 수 있습니다.

### 2. wireshark
가장 범용적으로 사용되는 네트워크 패킷 분석 툴 입니다.
[홈페이지](https://www.wireshark.org/download.html)

![This is an image](https://www.wireshark.org/assets/theme-2015/images/wireshark_logo.png)

### 2-1. wireshark 사용법

![1번 이미지](https://t1.daumcdn.net/cfile/tistory/994F0C3E5AAB2FA005)

분석 하고자 하는 네트워크를 클릭한 뒤 **start** 버튼을 누르면 실시간으로 패킷 정보를 확인할 수 있습니다.

![2번 이미지](https://t1.daumcdn.net/cfile/tistory/9916D4385AAB30482F)

빨간색 버튼을 누르면 패킷 캡쳐가 멈추게 됩니다.

![3번 이미지](https://t1.daumcdn.net/cfile/tistory/99AB1D385AAB304835)

중지한 패킷을 다시 캡쳐하고 싶을땐 초록색 버튼을 누르면 됩니다.

![4번 이미지](https://t1.daumcdn.net/cfile/tistory/99EC1B395AAB32F20B)

이 영역은 Packet Details 영역으로 전송되는 패킷의 세부 정보들을 볼 수 있습니다.

![5번 이미지](https://t1.daumcdn.net/cfile/tistory/9989B43D5AAB333433)

해당 영역은 Packet bytes 로 패킷의 내용을 16진수로 표현한 것 입니다.

![6번 이미지](https://t1.daumcdn.net/cfile/tistory/9915F6465AAB374C18)

HTTP 를 선택합니다.

![7번](https://t1.daumcdn.net/cfile/tistory/99316F4E5AAB379407)

HTTP Objects list를 보면 Content Type에 무슨 파일인지 확장자가 적혀있기때문에 분석시에 유용합니다.

![](https://t1.daumcdn.net/cfile/tistory/9915F6465AAB374C18)

HTTP를 선택합니다.

![](https://t1.daumcdn.net/cfile/tistory/99316F4E5AAB379407)

HTTP Objects list를 보면 Content Type에 무슨 파일인지 확장자가 적혀있기때문에 분석시에 유용합니다.

