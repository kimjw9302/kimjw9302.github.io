---
title: "2019 빅스비 캡슐 챌린지 시즌 2 - 알뜰살뜰 캡슐 제작"
date: 2019-10-29
categories:
  - Project
  - Bixby
last_modified_at: 2019-03-09T12:45:25-05:00
---


### 2019 빅스비 캡슐 챌린지 시즌 2 !


![빅스비](/images/bixby_1.jpg)
![빅스비](/images/bixby_2.jpg)

[빅스비캡슐챌린지 설명 보러가기](https://bixby.developer.samsung.com/newsroom/ko-kr/%EA%B3%B5%EC%A7%80-%E2%80%98%EB%B9%85%EC%8A%A4%EB%B9%84-%EC%BA%A1%EC%8A%90-%EC%B1%8C%EB%A6%B0%EC%A7%80-%EC%8B%9C%EC%A6%8C2-%EC%B0%B8%EA%B0%80-%EC%8B%A0%EC%B2%AD-%EC%A0%91%EC%88%98-%EC%8B%9C%EC%9E%91-%EB%8B%A4%EC%8B%9C-%EB%8F%84%EC%A0%84%ED%95%98%EC%84%B8%EC%9A%94)

#### 인원 : 4명
#### 툴 : Bixby Developer , Eclipse , MySQL
#### 개요 :
알뜰살뜰은 사용자의 위치 및 발화한 지역을 기준으로 농수산물의 가격 제공 및 가격 비교를 해주어 사용자로 하여금 알뜰살뜰한 소비를 하도록 도와주는 Capsule입니다.
알뜰살뜰은 한국농수산식품유통공사(이하 kamis)에서 제공하는 API를 활용하여 유통되는 농수산물의 최근 30일간의 데이터를 비교하여 현재 가격, 최근 동향, 평균 가격, 최고가 및 최저가, 그래프를 사용자에게 보여줘 알뜰살뜰한 소비 생활을 도와주는 캡슐입니다. 또한, 카카오 API를 통해 현재 사용자 위치에 기반한 정보를 제공해줍니다. 모든 정보는 제작한 API 서버로부터 전처리 후에 캡슐에 보내지게 됩니다.

####  제공가능한 품목 :  
식량작물(7품목 : 8품종)  
쌀, 찹쌀, 콩(백태국산), 팥(국산), 녹두, 고구마(밤), 감자(수미, 대지마)  
  
채소(32품목：45품종)  
배추(봄, 고랭지, 가을, 월동), 양배추, 시금치, 상추(적, 청), 얼갈이배추, 수박, 참외, 오이(가시, 다다기, 취청), 호박(애호박, 쥬키니), 토마토, 방울토마토(방울토마토, 대추방울토마토), 딸기, 무(봄, 고랭지, 가을, 월동), 당근(무세척), 열무, 건고추(화건, 양건), 풋고추, 청양고추, 꽈리고추, 붉은고추, 깐마늘(국산), 양파, 대파, 쪽파, 생강(국산), 미나리, 깻잎, 피망(청), 파프리카, 멜론, 갓, 고춧가루(국산, 수입)

특용작물(7품목：11품종)
참깨(국산백색, 중국, 인도), 땅콩(국산, 수입), 느타리버섯(느타리버섯, 애느타리버섯), 팽이버섯, 새송이버섯, 호두(수입), 아몬드(수입)

과실(15품목：30품종)
사과(후지, 쓰가루, 홍로), 배(신고, 원황), 복숭아(백도), 포도(캠벨얼리, 거봉, MBA, 샤인머스켓, 레드글로브 칠레, 레드글로브 페루, 톰슨 미국, 톰슨 호주), 감귤(노지, 시설), 감(단감), 바나나(수입), 오렌지(네이블 미국, 네이블 EU, 네이블 호주, 발렌시아 미국), 레몬(수입), 체리(수입), 건포도(수입), 건블루베리(수입), 참다래(국산, 수입), 파인애플(수입), 망고(수입)

축산물(5품목：19종류)
쇠고기(한우 : 갈비, 등심, 설도, 양지, 안심, 수입육[미국산 : 갈비(bone-in short rib), 갈비살(boneless short rib), 설도(bottom round)], [호주산 : 갈비, 등심, 설도]), 돼지고기(삼겹살[국산, 수입], 목살, 갈비, 앞다리살), 닭고기(도계), 계란, 우유

수산물(16품목：22품종)
고등어(국산[생선, 냉동, 염장], 수입냉동), 꽁치(수입냉동), 갈치(생선, 냉동), 명태(냉동), 물오징어(생선, 냉동), 건멸치, 건오징어, 김(마른김, 얼구운김), 건미역, 굴, 새우젓, 멸치액젓, 굵은소금, 조기(수입부세), 전복, 새우(수입흰다리냉동)


####  조사 지역 :  
서울, 부산, 대구, 인천, 광주, 대전, 울산, 세종, 수원, 의정부, 춘천, 청주, 전주, 순천, 포항, 안동, 창원, 제주
위의 18개 도시와 더불어 고성, 속초 양양, 여수, 익산 등 '시' 이름으로 발화하면 가까운 대표 도시의 정보를 보여줍니다.
근처에서, 우리 동네에서와 같은 발화에서도 위도·경도를 기반으로 현재 위치를 특정하고, 가장 가까운 대표 도시를 기준으로 정보를 보여줍니다.

#### 에러 처리 : 
NotFoundData : 농수산물 이름이 데이터베이스에 존재하지 않는 경우  
NotFoundLocation : 미리 지정한 지역 범주(vocab) 외의 지역을 입력받는 경우  
NotFoundItem : 해당 농수산물의 최근 정보가 없는 경우  
NoParameter : 발화 정보가 부족한 경우  
Unknown_Error : 서버에 에러가 발생한 경우  	


####  Capsule의 상세 화면 
사용자 발화 : 부산에서 닭고기 가격 알려줘
![빅스비] (/images/bixby_find_2.jpg)	
사용자 발화 : 배추 가격 알려줘 
![빅스비](/images/bixby_find_2.jpg)	


# 사용할 수 있는 기능 
+ 내 지역 농수산물 가격 탐색
* 농수산물의 10일간 가격변동
- 농수산물의 30일간 최대 최소 가격

```bash
빅스챌린지 알뜰살뜰
```
