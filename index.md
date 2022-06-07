# Network packet analysis 


### 들어가기 앞서
이 홈페이지는 제가 이번 VMT 과제를 진행하면서 조사한 네트워크 패킷 분석 방법과, 제 나름대로의 분석 결과를 포함하고 있는 결과물입니다.
글이 전문적이지 않을 수도 있고 **틀린 정보가 포함되어 있을 수도 있습니다.**

### 패킷이란
패킷은 한번에 전송되는 데이터의 단위입니다. 
> 왜 패킷을 사용해야만 할까요?

100MB크기의 데이터를 전송하고자 할때 분할된 형태가아닌 파일 통째로 보냈다고 가정해봅시다. 

100MB크기의 파일을 아무런 오류없이 전송이 되었다면 다행이겠지만, 전송도중 잘못된 데이터가 1개만 끼어도 오류가 발생하기 때문에 처음부터 다시 100MB를 전송해야 합니다. 

하지만 이 패킷을 이용해 파일을 1MB씩 나누어 전송하면, 1번 패킷 전송 - 수신 체크 2번 패킷전송 - 수신체크 이러한 과정을 100번하게 되는데 만일 중간에 오류가 나면 그 번호의 패킷만 재전송하면 되므로 전자에훨씬 효율적이라고 할 수 있습니다.

### wireshark
가장 범용적으로 사용되는 네트워크 패킷 분석 툴 입니다.
[홈페이지](https://www.wireshark.org/download.html)

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/haengryong/haengryong.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
