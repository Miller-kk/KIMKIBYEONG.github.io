---
title: Blockchain 2
description: Blockchain 2
header: 친절한 Researchar와 함께 따라가는 Blockchain 이야기 2화
---

## 프롤로그

저번 1화에서는 블록체인 탄생 이야기를 비트코인과 더불어 얘기를 했죠. ( 앞으로 회차가 거듭날 수록 글을 보시는 분들에게 가까이 다가간다는 의미로 글도  말하는 어투를 쓸까합니다. ) 블록체인이 어떻게 나온건지 알게되었다면 블록체인 기술의 원리를 알아보기 전 현재 블록체인의 발전은 어느정도 하였고, 블록체인의 활용 가능성을 좀 알아볼까 합니다. 그러기 위해서는 블록체인들의 발전을 정확히 구분짓고 확실하게 알아야겠죠? 블록체인의 기술적 원리를 알기 전 블록체인의 계보를 한번 저와 함께 재미있게(?) 살펴봅시다 !

## 발전 계보도
![BlockchainGo](./BlockchainGo.png)  
**BlockChain 발전 버전업을 나태내는 Map**  
**(  Blockchain 1.0과 2.0은 IBM에서 쓰는 용어를 사용했습니다 )**

발전 계보도는 위와 같습니다. Blockchian 1.0 이란 용어를 맨 처음 IBM 측에서 사용을 했는데요 저같은 경우는 이런 버전을 나타내는 용어가 발전을 설명하는 것에 편하기에 블록체인 발전 계보도를 이렇게 나타냈습니다. 발전을 크게 4가지 단계로 설명할 예정인데요, 저의 주관적인 정리 방식으로 발전을 정리하다보니 발전이 아니라 블록체인을 다양하게 사용하는 용도로 보일 수도 있다는 점 생각해주시길 바랍니다. 아무래도 블록체인을 정확히 정의를 한 표준 문서가 없다보니 사람들 마다 견해의 차이가 좀 있습니다. 이 글의 내용 중 문제가 되는 부분이 있다면 메일을 통해 지적을 해주신다면 겸손하게 받아들이겠습니다  

## Blockchain 0.0  

Blockchain 0.0의 단계는 1화에서 설명드린 비트코인의 공개 장부 형태로 사용되는 Blockchain을 칭하는 것입니다. Blockchain을 다른 형태가 아닌 오직 금융 내역을 알 수 있는 장부 형태로만 쓰임으로써, 순수하게 화폐의 거래를 투명하게 관리해주기 위한 Blockchain이라고 볼 수 있습니다. 다르게 말하자면 비트코인에서 발표한 순수한 Blockchain의 형태라고 보시면 이해가 조금 더 와닿지 않을까 생각이드는데요. Blockchain 0.0에서는 모두에게 공개되는 형태인 Public Ledger ( 공개 장부 ) 형태라고 보시면 됩니다. Blockchain이라는 것은 말 그대로 일종의 정보들을 담는 Block들을 이어 붙인 형태라고 보시면 되는데요. 조금 더 와닿게 각각의 블럭에 돈을 보낸 사람과 돈을 받는 사람 그리고 보낸 돈의 양을 적은 영수증들을 확실하게 모두가 볼 수 있게 모아서 안전하게 넣어놓은 형태라고 보시면 됩니다.  
![Blockchain0](./Blockchain0.png)  
**Blockchain 속에 담겨진 금융 정보**  
위 그림과 같이 순수하게 서로의 돈을 주고 받는 정보들을 변조할 수 없는 Block 안에 넣고 모두 에게 보여줌으로써 공정한 장부형태로 사용되게 됩니다. ( 각각의 chain들 안에는 많은 정보들이 있지만 빠른 이해를 위해 은행에서 발급하는 형태의 장부가 중심적이라고 보시면 됩니다. )  
이렇게 비트코인의 탄생과 함께 나오게된 순수한 장부 형태의 Blockchain을 Blockchain 0.0이라고 칭하게됩니다. 당연히 이 좋은 기술을 장부에도 쓰일 수 있겠지만 다른 곳에도 쓰일 수 있는 가능성이 많겠죠 !  
![Coin](./coin.png)  
**Bitcoin에 이어서 수 없이 파생되어 나온 많은 암호화폐(Coin)들**

## Blockchain 1.0  
Blockchain 1.0의 단계에서는 단순히 금융 기록을 남기는 장부의 형태로만 Blockchain을 사용하기엔 아쉬운 점들이 많았습니다. 왜냐하면 데이터에 대한 위/변조 가능성에 대한 문제는 대부분의 산업들에게 고질적인 문제였기때문이죠. 최근에 정보 유출과 관련된 사건/사고들이 상당히 많았습니다. 그에 대한 이유들은 흔히들 말하는 중앙 집중형 보관방식, 즉 데이터베이스 보안에 관해서 많이들 언급을 합니다. 이와같이 한 곳에 데이터를 모아두니 관리는 쉬우나 해킹에 한번 노출이 되게 되면 모든 데이터가 날아가는 문제라던지, 데이터의 기밀성을 유지 하기가 여간 쉽지않았습니다.  
> 이러한 중요한 정보들의 변조의 가능성을 불가능에 가깝게 만든다면 ??

위의 질문이 가능하다면 수 많은 것들을 할 수 있습니다. 자기 자신에 대한 기록들을 남겨서 일종의 범죄를 사전 차단하기 위한 알리바이로 사용할 수 있으며, 자기 자신을 증명할 수 있는 용도로도 쓸 수 있습니다. 그 외에도 많은 것들을 할 수 있다는거죠. 그렇게 사람들은 서서히 Blockchain을 장부의 형태가 아닌 정보를 담는 일종의 분산형 데이터 베이스로 사용하기 시작합니다. 데이터 베이스처럼 한 곳에 저장하지 않다보니 정보의 관리를 하는 알고리즘을 만드는 것에는 까다로울지 몰라도 분산형으로 저장하는 방식과 공개키 암호화 방식과 조합을 잘 시키면 각 블럭의 기밀성도 유지할 수 있으니 그렇게 큰 손해라고 생각하지 않는 은행들이 많아지기 시작합니다.  

![bank](./bank.jpg)  
**Blockchain  기술을 도입하기 시작하는 Bank 업계**  
많은 사람들은 이해가 안가기 시작합니다. Blockchain의 첫 번째 플랫폼인 비트코인의 모토가 **"중앙 신뢰 기관을 없애자"**임에도 불구하고, 오히려 은행들이 많이 사용하다니 이게 뭐야! 라구요. 하지만 경쟁력을 생각을 하면 Central 형태인 은행도 Blockchain을 무시할 수 없다는 의미입니다. Blockchain을 사용하지 않으면, 비트코인에 비해 경쟁력을 가지기가 쉽지않다는 거죠.  
> 호랑이를 잡으려면 호랑이 굴에 들어가야한다.  

위 속담과 유사하다고 보시면됩니다. Bank들은 장부는 비록 Central 형태로 보관할지라도 Blockchain을 굳이 장부의 형태가 아닌 그 사람에 대한 정보를 넣고 변조의 가능성을 현저히 낮춘 이후에 사람에 대한 인증의 용도로 사용하여, 경쟁력을 갖춘겁니다. 저는 이러한 현상을 보고 이제는 Bank도 더 이상 사람이 관리하는게 아닌 컴퓨터가 정보를 관리하는 시대가 열리면서 IT 기업에 가까운 모습을 보이고 있다고 봅니다.  
이렇게 Blockchain들에 사람에 대한 생체 정보나 변조가 되어서는 안되는 정보들을 넣고 보관을 하는 용도로 사용하는 발전 상태를 Blockchain 1.0이라고 칭합니다.  
![Blockchain1](./Blockchain1.png)  
**Blockchain 1.0 메커니즘**  

## Blockchain 2.0  
Blockchain 2.0부터는 조금 흥미 진진해집니다. 그 이유는 바로 ! Blockchain에 정보를 넣는 형태가 아닌 이제는 프로그래밍을 할 수 있는 Code가 들어간다는 거죠 !  
> Block에 Programming Languager가 들어간다는 개념은 Block에 일을 하는 사람이 들어간다는 개념과 동일하다.  

위의 말은 프로그래머가 아닌 이상 조금 와닿기 힘든 말일 수 있습니다. 일종의 Block들에 튜링완전언어를 넣을 수 있다는 것인데요, 튜링완전언어를 넣을 수 있다는 것은 차원이 다른 발전입니다. 단순히 Blockchain에 정보를 넣어 두는 보관함의 형태로 활용했던 것이 1.0이라고 한다면 2.0은 정보를 넣는다고 가정하면, Block들이 능동적으로 그 정보를 판단하고 분류를 할 수 있는 단계까지 갔다는 거죠. 쉽게 말해서 Block들 각각에 일을 할 수 있는 사람이 들어간다고 보시면 됩니다. 한 Block엔 정보를 판별하는 사람, 어떤 한 Block엔 돈을 다른 곳으로 보내기 위한 일을 하는 사람 등등 이런 식으로 해야할 일들을 분산해서 사람들을 넣는 것과 동일하게 보면 이해가 빠르겠죠?! ( 이해가 잘되길.. 하하)  
조금 더 와닿게 예를 들어서 설명드리면, 제가 스마트 냉장고를 하나샀다고 합시다. 이 냉장고 안에는 무시무시한(?) 블록체인 시스템이 도입되었다고 가정하죠. Blockchain 1.0이라고 하면 단순히 냉장고의 온도나 상태에 관해서 정보가 들어있는 것들만 볼 수 있는 상태입니다. 하지만 2.0이라고 하면 냉장고가 항상 있어야할 과일이 없다고 한다면, 능동적으로 인터넷에서 자동으로 과일을 구매하여 배송을 시키는 모습을 띄게 됩니다. 이 과정에서 사람이 아닌 사물이 능동적으로 화폐를 소비하기 시작하게되죠. 그래서 2.0에서 코드를 사용하는 것이 파급력이 큰 이유가 능동적이지 않았던 사물들도 IOT를 만나서 능동적으로 변한 것처럼 Blockchain을 만나게 되면 더욱 안전하게 능동적으로 화폐를 소비할 수 있는 의미가 생깁니다.  
> 사물이 돈을 주고  물건을 산다 ?!  

![Smart](./smart.png)  
**소비를 주체적으로 할 수 있는 냉장고의 탄생**  
위의 말을 다르게 해석하면 예전에는 보안의 문제로 컴퓨터가 할 수 있는 일들이 제한되었다면, 발목을 잡았던 보안성을 Blockchain이 상당 부분 해결해줌으로써 컴퓨터가 능동적으로 제약없이 일들을 처리할 수 있게 되었다는 것입니다. 위와 같이 물건도 사는 것처럼 사물이 점점 사람이 하는 영역을 하나 둘씩 따라간다는 점에 주목할 수 있습니다.  
> 어떤 사람들은 4차 산업 혁명은 거품이라고 말합니다. 물론 거품일 수 도 있지만 이 기술들을 멋지게 융합하고 발전시킨다면 컴퓨터가 할 수 있지만 보안의 이유로 제약 받았던 일들을 해결하면서 IT의 발전 속도가 예전보다 다르다는 것을 확실히 말할 수 있습니다.  

![Bussiness](./Bussiness.jpg)  
출처:<http://www.etoday.co.kr/news/section/newsview.php?idxno=1493984>  
**Blockchain 2.0에 뛰어들기 시작하는 대기업들 ( 삼성도 동참 )**

## Blockchain 3.0  
Blockchain 3.0부터는 제가 2.0까지 IBM에서 쓰던 용어를 한 단계 발전시켜 만든 용어입니다. ( 지극히 개인적인 주관으로 발전 3.0을 썼다는 점 참고해주세요. ) 2.0까지는 각각의 Chain들 하나하나에 집중을 했었다면 3.0부터는 Chain들의 연결성( Connection )에  집중을 하기 시작합니다. 최근에 권위 있는 단체인 R3에서 Blockchain 2.0의 선두 주자로 달리고있는 Ethereum의 개발자 Vitalic이 발표한 자료인 Chain interoperability의 문서에서 언급되었으며, Blockchian을 더 이상 단일한 chain으로 제 각각 사용하지말고 chain들끼리 유기적으로 연결될 수 있도록 호환성을 높여보자는 시도입니다. Blockchain 들이 기반으로 하고 있는 프로그램들이 제각각 틀린 탓에 Blockchain들끼리 유기적으로 연결한다던지 함께 호환성을 높여서 작동을 하기가 쉽지않습니다. 하지만 interoperability 문서에서 언급된 이후로 미국 cornell 대학교 Blockchain 랩실에서는 Chain들 간의 유기적으로 연결할 수 있는 알고리즘을 연구하고 있으며, init이라고 하는 세계 Blockchain 연구 단체도 chain들 간의 호환성을 높일 수 있는 방법을 연구하기 시작하고 있습니다.  
> Chain들간의 연결이 가지는 의미 ? meaning ?  

Chain들 간의 연결을 할 수 있게되면 자유도(Free)의 정도가 틀려지게 됩니다. 자유도란 무엇이냐하면 Blockchain 2.0 까지는 그 Blockchain에 Block에 각각 Code를 넣어 지정한 일들까지만 할 수 있다고 한다면 Chain들 간의 호환성이 높아져 Chain들 간의 연결성이 완벽하게 보장된다고 한다면 각 Chain들 마다 각각 할 일들이 정해져있는 상황에서 Chain들을 합치는 과정에서 Chain들이 할 수 있는 일들을 협엽을 시키면서 할 수 있는 새로운 일들이 나올 수 있다는 것입니다. 자유도(free)라는 말은 문서에서 본 단어는 아니고, 일종의 보안에서 사용하는 용어인데 여기서 쓰기에 적합한 용어이기에 인용을 했습니다.  
사실 Chain들끼리 단순히 연결한다는 의미가 아니라 예를 들어 변호사 연합과 사업가 연합이 있다고 가정을 하면 이 두 연합이 합쳐서 유기적으로 일을 한다면 시너지를 낼 수 있는 점들이 많겠죠. 이 처럼 제각각 하는 역활이 있는 chain들을 호환성을 높여 연결한다는 것은 단순히 정보를 교환하는 의미를 넘어 새로운 일을 할 수 있다는 것을 시사합니다.  
![connection](./connection.png)  
**Blockchain을 대표하는 Bitcon(0.0) Ethereum(2.0)의 connection**  

![sidechain](./sidechain.png)  
**Blockchain들 간의 연결을 해주는 Blockchain의 시도 Sidechain**  

**To be Continue...**  
이번 화에서 블록체인의 진화 과정을 한번 보았다면 ! 다음 화에서는 간단하게 블록체인의 종류가 두 가지가 있는데 이것을 한번 간결하게 분료해보겠습니다. 아마 생소한 개념이라 어려우실지몰라도 계속해서 생각해보신다면 이해가 가시는 순간이 훅 오게된답니다  





 