--
title: Private BlockChain
description: How to make private blockchain
header: BlockChain Application 구축하기
--
thereum Ether 전송하는 웹 어플리케이션 만드는 순서
# Web3.js로 웹 어플리케이션을 만들기 위한 환경 구축하기
방법이 여러 가지가 있어서 여러 가지 방법으로 설명하겠습니다.
1. https://github.com/ethereum/web3.js 에서 dist에 있는 web3.js를 따로 작업하는 폴더에 다운받아서 HTML 작업 시에 자바스크립트 src로 참조를 해서 스크립트 작성을 한다.
2. node.js로 환경구축 시 node.js 명령 프롬프트를 켜서 npm install web3를 쳐서 install
을 쳐서 web3.js를 다운받아 환경 구축을 한다.
( Git 설치 필수입니다 !! )
3. bower로 install 시에 bower install --save web3 명령어를 이용하여 web3.js를
다운받아 환경 구축을 한다.
# GETH(Go-ethereum) 환경 구축
참조 사이트 : [Building Ethereum](https://github.com/ethereum/go-ethereum/wiki/Building-Ethereum)
1. Private Network 구축을 위해서는 Geth(Go-Ethereum)이 필요한데, Geth 인스톨 시
다양한 환경이 존재합니다. 여기서는 VMware로 돌리는 ubuntu linux 환경의 기준으로
설명하겠습니다. ( 그 외 Mac OS X 와 Windows 등 다른 환경은 참조 페이지에 있습니다 )
1. 먼저 Ethereum을 우분투 리눅스 환경에 설치를 합니다.
	* 설치시 쓰는 명령어:
		```
		sudo apt-get install software-properties-common
		sudo add-apt-repository -y ppa:ethereum/ethereum
		sudo add-apt-repository -y ppa:ethereum/ethereum-dev
		sudo apt-get update
		sudo apt-get install ethereum
		```
2. Geth를 Building 해줍니다.
	* 선택한 directory에 geth 복사하는 명령어:
		```
		git clone https://github.com/ethereum/go-ethereum
		```
	* 최신 Go 버전이 없을 시에 인스톨 하는 명령어:
		```
		sudo apt-get install golang
		```
	* Go 설치 이후에 GOPATH 와 PATH 설정하기.
		- GO로 적절하게 작업하기 위해서는 두가지 환경변수를 설정해주어야 한다.
		- go folder를 만든다.
	 		```
			mkdir -p ~/go; echo "export GOPATH=$HOME/go" >> ~/.bashrc  
			```
		- path를 업데이트 시켜준다
			```
	 		echo "export PATH=$PATH:$HOME/go/bin:/usr/local/go/bin" >> ~/.bashrc
			```
3. geth에 필요한 외부 라이브러리를 설치한다.
	```
	sudo apt-get install -y build-essential libgmp3-dev golang
	```
4. geth 프로그램을 빌드한다.
	```
	cd go-ethereum
	make geth
	```
5. 이제 build/bin/geth를 실행해서 당신의 노드를 시작한다
# 본격 Private Network / Block Chain 만들기 및 ETHER 전송
1. genesis block을 만들기 위해 양식에 맞게 json 파일을 만든다.
	* genesis.json 기본 양식
	```
	{
	“nonce" : "0x0000000000000042",
	"timestamp" : "0x0",
	"parentHash"
	: "0x0000000000000000000000000000000000000000000000000000000000000000",
	"extraData": "0x0",
	"gasLimit": "0x8000000",
	"difficulty": "0x400",
	"coinbase": "0x3333333333333333333333333333333333333333", << 방금 만든 지갑 주소
	"alloc": {
	 “방금 만든 지갑 주소 “: {
	“balance" : " 넣고싶은 Ether의 양 ”
	    }
	}
	```
2. 작성한 json 파일을 이용해 Geth 명령어로 genesis block으로 만들어 줍니다.
	```
	$ geth --datadir <some/location/where/to/create/chain> init genesis.json
	```
( 파일 이름이 genesis.json이라고 가정하자 )
4. 본격적으로 Geth로 Private Network 구축을 위해 명령어를 넣어줍니다.
	```
	$ geth --rpc --rpcaddr "자신의 ip 주소" --rpcport "http 포트번호" --port "Listening Port번호" --rpccorsdomain "*" --nodiscover console
	```
	--rpc : 당신의 노드가 RPC interface를 사용하도록 합니다.
	--rpcapi "db,eth,net,web3": RPC에 접근하게 허가하는 api를 지정합니다. (default는 db,eth,net,web3. miner가 필요한 경우에는 추가.)
 	--rpcaddr : 연결하려는 네트워크 ip를 지정합니다.
	--rpcport : 당신의 네트워크에 open하려는 port 지정 ( default : 8545 )
	--port : network listening port를 지정합니다.
	--rpccorsdomain : 당신의 RPC instance에 연결을 허락하는 URl(domain) 지정
	--nodiscover: 당신의 노드가 모르는 블록체인에 추가되어 블록들이 Import되지않게 합니다.
	--datadir : 당신의 private chain 데이터를 보관할 폴더 지정
	--maxpeers : 당신의 체인에 연결하는 peer의 제한 갯수
	--identity : 당신의 node를 식별하는 name 지정
	```
	$ geth --identity "PrivAlgot" --datadir "~/testnet/" --port 30305 --ipcapi "admin,db,eth,debug,miner,net,shh,txpool,personal,web3" --autodag --networkid 1901 --nodiscover --maxpeers 0 --rpcapi "db,eth,net,web3,miner" --rpc --rpcaddr "10.0.0.101" --rpcport 8545 --rpccorsdomain "*" console
	```
	5. 자바스크립트 콘솔이 뜨면 , 새로운 어카운트 1개를 더 개설합니다.
	```
	> personal.newAccount(passwd)
	```
6. Account Mining 작업을 해줍니다.
	```
	> miner.start(n);                     * n은 블록 갯수
	  admin.sleepBlocks(n);
	  miner.stop();
	```
7. 이더를 소비해서 돈을 보내는 지갑 주소를 UNLOCK 해줍니다.
	```
	personal.unlockAccount("지갑 주소")
	```
8. 만들어놨던 HTML 페이지로 새로 만들었던 어카운트로 Transaction을 전송합니다.
9. 콘솔창에 eth 명령을 통해서 transaction이 잘 전송되었는지 확인 합니다.
10. 잘 전송이 되었다면 다시 한번 최종 mining을 해줍니다.
11. 전송 완료 !!
참조 사이트
1.
https://github.com/ethereum/go-ethereum/wiki/JavaScript-Console#personalnewaccount
2.
https://github.com/ethereum/go-ethereum/wiki/Managing-your-accounts
3.
https://souptacular.gitbooks.io/ethereum-tutorials-and-tips-by-hudson/content/private-chain.html

