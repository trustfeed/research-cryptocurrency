# blockchain terms
### proxy re-encryption
<https://en.wikipedia.org/wiki/Proxy_re-encryption>

### PUF 기술
<http://m.boannews.com/html/detail.html?idx=67363>

+ PUF는 찾아보니 물리적인 칩셋이며, sha256같은 hash function을 하드웨어 적으로 지원합니다. 
+ 하드웨어가 지원하므로, Public/Private 키에서 Private 키값이 존재하지 않고, 하드웨어 자체가 Private 키 역할을 하는듯합니다. 
+ 기존 블록체인은 SHA-256, SHA-3등 여러 해시함수를 사용하는데, 애초에 PUF 기기는 임베디드/IOT를 타겟으로 해서 생산되는듯 하니 직접적인 경쟁자는 IOTA 코인이 될듯합니다. 
+ 여타 블록체인은 기사와는 다르게 당장 영향을 받기는 어려우며 향후에 어떻게 영향을 받을지는 현재로써는 예측하기 어려운듯합니다. 
+ 합의지연, 처리속도 지연은 알고리즘을 수행하는 속도의 문제라기보다는 기본적으로 public blockchain의 탈중앙화를 위한 trade-off적 성격인거라, PUF를 도입한들 관련이 없어보이며, 
+ 사용자 인증은 난제가 아닙니다. 기본적으로 비트코인 anonymous를 추구하는 방향이며, 소프트웨어적인 방법으로도 충분히 사용자 인증이 가능합니다.

결론 : 기사에 나온대로 실제 구현이 정말 제대로 된거라면 의미는 있으나, IOT외에는 영향력이 미미할듯함

2005년 Nick Szabo는 소유주 권한을 통한 재산권 보장이라는 글에서 정주(homesteading), 불범점유, 지공주의(Georgism) 등의 개념을 포함한 정교한 틀을 설계해 누가 어떤 땅을 가지고 있느냐라는 등기 문제를 블록체인 기반 시스템으로 처리할 수 있음을 보였다. 하지만 효과적인 파일 복제 시스템이 없었다.


### 퍼블릭,프라이빗 퍼미션레스 구분
<https://drive.google.com/open?id=1A9MkGlBj3QiK4z5ttQhjIohCk5Hhfejo>

### 비트코인 스크립트
<https://en.bitcoin.it/wiki/Script>

### 타원곡선암호 ECC
<https://ko.wikipedia.org/wiki/%ED%83%80%EC%9B%90%EA%B3%A1%EC%84%A0_%EC%95%94%ED%98%B8>

### 머클트리
<http://nacamp.tistory.com/16>

### 패트리샤 트리
검색에 용이, 데이터 압축
- Uses : 이더리움, 텐더민트, 리플
<https://github.com/ethereum/wiki/wiki/Patricia-Tree>
<https://medium.com/basecs/compressing-radix-trees-without-too-many-tears-a2e658adb9a0>
<https://easythereentropy.wordpress.com/2014/06/04/understanding-the-ethereum-trie/>

### CryptoNote
+ Application layer protocal
+ Uses : Bytecoin(BCN), Monero(XMR)
+ CryptoNote currencies use a distributed public ledger that records all balances and transactions
+ CryptoNote's transactions cannot be followed through the blockchain in a way that reveals who sent or received coins
+ CryptoNote uses memory bound function CryptoNight, which cannot be easily pipelined

### 세그윗 (Segregated Witness)
BIP(Bitcoin Improvement Proposal)로 제안됨
증인분리 (거래서 내역에서 서명을 비트코인 1M범위 밖으로 따로 분리)

1. 블록사이즈 증가효과
2. 이중지출 해킹 방지

### 라이트닝 네트워크
일반 신용카드, 체크카드 결제보다도 빠른 시간안에 컨펌이 완료될 수 있음, 크로스 스왑

### dApp
<https://medium.com/@BARBIEBUYSDIPS/cryptocurrency-vs-dapp-a91c8cc8b5b8>

### dag
<http://new93helloworld.tistory.com/182>

### daico
<https://docs.google.com/presentation/d/1vcFjuHobwt2Q7A_wQOTUakkujWqh-8lGGsFBoARCusk/edit#slide=id.p3>

### IPFS
<https://steemit.com/kr/@kblock/27-ipfs-interplanetary-file-system-2-ipfs-filecoin>

### SWAP vs 0x
#### SWAP protocol 
+ 이더리움 개발 커뮤니티 Consensys에서 프로토콜 개발
+ 이더리움 블록체인에서 토큰을 트레이딩하기위한 프로토콜
+ 기존 거래소에 있는 주문서(order-book)가 없이 자산거래 진행
+ 가격과 주문을 설정할수 있음
+ 간략요약 -> 오프체인에 오더북이 아닌 인덱서란 이름으로 오더북을 사용해 호가등을 공개하지 않고 트레이딩하겠다.

#### Ox protocol
+ 이더리움 블록 체인에서 분산된 교환을 위한 개방향 프로토콜
+ 유사 프로토콜 - EtherDelta
+ 거래를 원활하게 하기 위해 주문서를 사용하며, 공공 오더북에서 트레이딩 - 오프체인 오더북을 사용
+ 간략요약 -> 수수료가 적은 오프체인에 오더북을 이용해서 트레이딩하겠다

### [비트코인]마이닝풀 작동방식 
+ 채굴자는 스트라텀(STM), GetBlockTemplate(GBT)등의 채굴 프로토콜을 사용해서 풀 서버에 접속
+ STM과 GBT는 후보블록 헤더의 쳄플릿을 담고있는 블록 템플릿을 만듬
+ 채굴풀은 실제 풀어야할 문제를 나누어서, 낮은 난이도의 문제를 만듬 
+ 각 채굴자가 풀어야 할 난이도는 실제 비트코인 네트워크의 난이도보다 낮으며, 각 채굴자는 각각 다른문제를 풀게됨 
+ 채굴자는 자신의 문제를 풀면 채굴풀을 통해 보상을 받고, 채굴풀은 이결과값들중 실제 비트코인 네트워크의 문제를 푸는 결과값을 얻어올수 있음