🦊 라우팅 프로토콜 : 라우터가 경로 정보를 조합하기 위해 사용하는 여러 프로토콜

* 외부 라우터 : 자율 시스템의 정보를 다른 자율 시스템과 교환할 수 있도록 설계됨
  * 

* `BGP` : AS 간 트래픽을 라우팅하는 데 사용되는 프로토콜
  * AS 내의 내부 프로토콜로도 사용된다.

# 링크 상태 라우팅

> Link- State Routing
>
> 링크 상태 정보를 모든 라우터에 전달하여 최단 경로 트리를 구성하는 라우팅 프로토콜 알고리즘

| 장점                               | 단점                                                       |
| ---------------------------------- | ---------------------------------------------------------- |
| Topology 변화에 빠른 반응          | * 내부 리소스 소모가 많다. <br /> * 잦은 SPF 알고리즘 수행 |
| SFP 알고리즘에서 Routing Loop 방지 | Network Topology 정보 관리 필요                            |
| 계층에 따라 Network 확장성 보장    |                                                            |



# OSPF

* [OSPF](https://www.netmanias.com/ko/post/blog/5476/ip-routing-network-protocol-ospf-shortest-path-tree/ospf-basic-part-1-build-of-shortest-path-tree-topology) 이해하기
* Link- State Routing 프로토콜로 **SPF**(Short Path First) 알고리즘 사용한다.
* AS 내부의 라우터끼리 (**IGP**) 라우팅 정보를 교환하는 라우팅 프로토콜.

![image-20210127000626459](C:\Users\sec\AppData\Roaming\Typora\typora-user-images\image-20210127000626459.png)

> 모든 IP 라우터(AR, ER, CR, DCR, PR, ASBR)는 `OSPF`나 `IS-IS`와 같은 IGP 프로토콜이 돌아서 IP 망 토폴로지 정보를 서로간에 주고 받고, shortest path tree 토폴로지를 구성

*  `OSPF`는 Cost가 작은 경로를 최적의 경로(Shortest Path)로 인식

# RIP

> 라우팅 정보 프로토콜 
>
> :: 일반적인 거리 벡터 내부 라우팅 프로토콜

* 홉 카운트로 목적지에 도달하는 최상의 경로를 결정한다.

## 