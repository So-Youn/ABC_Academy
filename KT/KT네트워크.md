# KT 네트워크

```markdown
# 역사
1885 한성정보총국 개국

1971 장거리 자동 전화 개통

1986 TDX 자동식 교환기 개통

1994 KORNET 서비스 개시

1996 CDMA 상용화

1997 PCS 상용화

2008 IPTV 상용화 개시

2009 국내 최초 스마트폰 도입(아이폰)

2011 LTE 이동통신 서비스 개시

2014 기가 인터넷 서비스 개시

2016 평창 올림픽 5G 서비스 시범 운영

2018 국내최초 10GiGA 인터넷 상용화

2019 세계최초 5G 서비스 상용화
```

## Domestic Network Hierarchy : 인터넷

* OTT 접근하기

  > ​	HOME 	  - >  		OUT SIDE     ->   Office      ->   Long Distance   ->   OTT
  >
  > 노트북     -    ONT   -     L2 SW     -    OLT  - SER	- 	KORNET   - 		Data Server 
  >
  > ​					[모뎀]	[포트 집약]

* 5G 고도화

  | 구분     | 3.5GHz  | 28GHz   |
  | -------- | ------- | ------- |
  | 대역폭   | 100MHz  | 800MHz  |
  | 다운로드 | 1.6Gbps | 5Gbps   |
  | 업로드   | 75Mbps  | 600Mbps |

## Domestic Network Hierarchy : OSP

```markdown
KT 국사 (코어 시설) - 통신구 - KT 국사  - 통신구 - 맨홀 - KT 액세스 시설(인터넷/무선 기지국)
------ 선과 선을 연결하기 위해 전국에 통신 국사(전화국)
- peer to peer로 광케이블이 연결되어 있어야 한다. 
```



* 우리나라 산간/도서 지방은 `Micro Wave`로 통신 - *(케이블이 연결될 수 없을 때 무선으로 쏜다)*
  * Zone 단위로 `Micro Wave` 통신망을 가지고 있다.

* **11 Level ACM** (Adaptive Coding and Modulation)
  * 전파가 바다에서 반사가 되면 페이딩 발생한다. 또한 비가 오면 주파수 사이클에 영향이 갈 수 있다
  * 이렇게 상태가 좋지 않을 때 대역폭을 줄여서 통신이 이어지게 하는 기술이 **11 Level ACM**이다.

## :star: NMS

> **NMS (Network Management System)**
>
> 네트워크 설계, 구축, 운용 및 유지보수 업무 전 영역에 AI 적용하여 자동화/지능화 확대
>
> 모니터링 - (빅데이터) - AI 관제 - (장애조치) - 자동제어



* Satellite(인공위성) : 대역폭이 적어서 트래픽 처리량이 작다. 
  * KT가 5, 6, 8, 5A, 7호 가지고 있음
* Submarine Cable : 글로벌 인터넷 트래픽의 99%를 해저 케이블로 관리
  * 글로벌  Traffic 허브 역할 수행(트래픽 처리 118.4T 세계 최고 수준)
  * 해저 케이블 건설 선박