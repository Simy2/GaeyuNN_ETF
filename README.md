# The data sets of stocks and etfs and gnn modeling of predicting etf price (krx사이트 기반 주식 데이터 및 etf 데이터)
이 데이터 셋 및 코드는 광운대학교 딥러닝 실습 수업 프로젝트를 위해 만들어진 것들입니다. <br>
These data sets and codes are made for 'deeplearning practice' lecture in kwangwoon university.

코드들은 중구난방으로 작성된 경향이 있어서 참고하실 분들은 번호대로 참고하시면 좋을 것 같습니다. <br>
These codes are written in a haphazard manner. So if you want to refer to these codes, you have to see codes in order of number.

코드에서 csv파일을 불러올때, 수정 전 파일 이름으로 불러오고 있는데 아래와 같이 수정해야합니다. <br>
When loading a CSV file in these codes, you need to update it to use the new file name as follows <br>

1. 날짜별 주식정보.csv -> data/2010~2024_marchLastDay_allStockInfo <br>
2. etf 수익률 및 1년간 코스피 관련 지표 -> data/2020~2024_marchLastDay_etfProfit_with_kospiProfit_and_kospiStd <br>
3. etf_with_stock -> 2020~2024_marchLastDay_stockInfo_in_etf <br>
4. etf가격정보 -> 2019~2024_marchLastDay_etfInfo <br>
5. stocks_with_value_index -> 2020~2024_marchLastDay_stocksInfo_with_valueIndex <br>
6. 날짜별etf정보 -> 2010~2024_marchLastDay_stockProportion_in_etf <br>
7. 표준코드 -> presentStockInfo <br>


## project overview(프로젝트 개요)
이 프로젝트는 etf와 etf를 구성하는 주식들의 정보를 모아 gnn을 통해 etf의 가격을 예측하는 프로젝트이다. <br>
This project is the project that predict the etf's price by using etf information and stock information that be contained in etf.

## Data Collection and Preparation(데이터 수집)

이 데이터 셋의 출처는 krx, 네이버, fnguide, yahoo finance입니다. ticker지표들은 krx를 통해 가져왔습니다. <br>
The source of these data sets is KRX, naver, fnguide, yahoo finance. The source of ticker data is KRX.

가치지표의 계산을 위해 데이터는 1년 단위로 되어있고, 기준 달은 3월로 정했다. <br>
For the calculation of the value indicator, the data is organized on an annual basis, and the base month has been set to March.

## Graph Construction(그래프 구축)

etf를 하나의 그래프로 보고, etf를 구성하는 각 종목들을 노드로 보았다.  <br>
I considered the ETF as a single graph, and each component stock as a node.

종목의 가치지표나 시가총액 등은 노드를 구성하는 요소이다. <br>
Metrics such as valuation indicators and market capitalization constitute the elements of the nodes.

그래프의 간선은 두 종목의 상관관계로 나타냈다. 상관관계가 0.3보다 적으면 간선이 없도록해 full connected가 되는 것을 방지했다. <br>
The edge of graph represent the correlation between two stocks. To prevent full connectivity when the correlation is less than 0.3, we ensured that such edges are absent.

etf의 가격을 예측하는 것이므로, gnn을 사용하여 graph prediction을 수행했다. <br>
The perpose is predicting the etf's price, so I used Gnn for graph prediction.

## Code overview(코드 설명)

5번코드로 데이터 수집과 전반적인 전처리가 진행되고, 6번코드로 gnn모델링을 진행합니다. <br>
The code of number 5 is data preprocessing and data collecting code, the code of number 6 is the modeling code.

나머지 코드들은 데이터를 수집하는 코드입니다. <br>
The codes of rest numbers are is data collecting code.

## Results and Discussion(결과 및 회고)

이 프로젝트의 아쉬운 점은 과거의 값을 통해 예측을 진행해서 예측이 잘되어야 하는 것이 당연했다. <br>
One disappointing aspect of this preject was the expectation that predictions would be accrate based on past values.

또한 데이터 수집에 관해서도 깔끔히 처리하지 못했고, gnn에 대한 지식이 부족해 모델링에 대한 한계가 있었다. <br>
Furthermore, I did not handle data collection cleanly, and my lack of knowledge about GNN limited the modeling capabilities.
