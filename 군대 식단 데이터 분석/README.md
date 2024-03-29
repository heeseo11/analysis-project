# 1. 군대 식단 데이터 분석

- data

  - [육군 훈련소 병영 표준 식단 정보 데이터 월별](https://opendata.mnd.go.kr/openinf/openapiview2.jsp?infId=OA-9547)

순번	| 날짜	| 조식	| 중식	| 석식
|---|---|---|---|---|
1|	2016-01-02|	밥	|카레밥	|밥
2	|2016-01-02	|감자양파찌개	|시금치된장국	|북어채국
3	|2016-01-02	|비엔나소시지케찹볶음	|돈가스	|두부김치
4	|2016-01-02	|맛김	|김장김치|	콩나물무침
5	|2016-01-02	|김장김치|		김장김치
6	|2016-01-03	|밥	|햄야채볶음밥|	잡곡밥
7	|2016-01-03	|쇠고기미역국	|계란국|	버섯쇠고기찌개
8	|2016-01-03	|버섯호박볶음	|맛김|	잡채
9	|2016-01-03	|감자조림	|김장김치	|고등어순살튀김
10|	2016-01-03|	김장김치|		김장김치|

- 식단 메뉴 언급량
  - bar 차트

![image](https://user-images.githubusercontent.com/61724682/135229635-d80b74d3-7bee-40af-8b1f-90d29dca7208.png)

  - 워드클라우드
![image](https://user-images.githubusercontent.com/61724682/135230263-d7b3da46-d6a0-4cb0-b8a8-bee3cedd527b.png)


- 장바구니 분석
  - 지지도, 신뢰도, 향상도 
      - support 지지도 : X와 Y가 함께 발생할 확률

      - confidence 신뢰도 : X가 나왔을 때 Y가 나올 확률

      - lift 향상도 : X,Y가 독립으로 가정했을 때 X와 Y가 함께 일어난 사건을 X와 Y가 서로 독립인 사건일 때 이렁난 사건으로 나눈 것 

          - lift가 1이면 두 제품은 독립

          - 1보다 크면 우연적 기회보다 높은 확률 / 1보다 작으면 우연적 기회보다 낮은 확률 

          - lift가 큰 것을 추천

- 네트워크 생성
  - [vis Network 활용](https://visjs.github.io/vis-network/examples/)

    - [Custom Scaling 사용](https://jsfiddle.net/api/post/library/pure/)

  - 메뉴 키워드별 네트워크 생성

