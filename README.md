# GaeyuNN_ETF

<div style="text-align: center;">
    <img src="DALL·E 2024-07-11 12.50.45 - A simple and clean illustration representing a project on predicting ETF prices using Graph Neural Networks (GNN). The image should include a basic gr.webp" alt="alt text" width="300"/>
</div>

<div style="text-align: center;">
    <img src="https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter Notebook"/>
    <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" alt="Python"/>
    <img src = "https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white"/>
</div>



## The data sets of stocks and etfs and gnn modeling of predicting etf price<br>(krx사이트 기반 주식 데이터 및 etf 데이터)
These data sets and codes are made for 'deeplearning practice' lecture in kwangwoon university.

These codes are written in a haphazard manner. So if you want to refer to these codes, you have to see codes in order of number.

When loading a CSV file in these codes, you need to update it to use the new file name as follows <br>

1. 날짜별 주식정보.csv -> data/2010~2024_marchLastDay_allStockInfo
2. etf 수익률 및 1년간 코스피 관련 지표 -> data/2020~2024_marchLastDay_etfProfit_with_kospiProfit_and_kospiStd <br>
3. etf_with_stock -> 2020~2024_marchLastDay_stockInfo_in_etf <br>
4. etf가격정보 -> 2019~2024_marchLastDay_etfInfo <br>
5. stocks_with_value_index -> 2020~2024_marchLastDay_stocksInfo_with_valueIndex <br>
6. 날짜별etf정보 -> 2010~2024_marchLastDay_stockProportion_in_etf <br>
7. 표준코드 -> presentStockInfo <br>


## project overview(프로젝트 개요)
This project is the project that predict the etf's price by using etf information and stock information that be contained in etf.


## Main feature(주요기능)
1. Data Collection, end of March from 2020 to 2024.
2. Graph Engineering
3. Model Building
4. Performance Evaluation

## Data Collection and Preparation(데이터 수집)

The source of these data sets is KRX, naver, fnguide, yahoo finance. The source of ticker data is KRX.

For the calculation of the value indicator, the data is organized on an annual basis, and the base month has been set to March.

## Graph Construction(그래프 구축)

I considered the ETF as a single graph, and each component stock as a node.

Metrics such as valuation indicators and market capitalization constitute the elements of the nodes.

The edge of graph represent the correlation between two stocks. To prevent full connectivity when the correlation is less than 0.3, we ensured that such edges are absent.

The perpose is predicting the etf's price, so I used Gnn for graph prediction.

## Code overview(코드 설명)

The code of number 5 is data preprocessing and data collecting code, the code of number 6 is the modeling code.

The codes of rest numbers are is data collecting code.

## Results and Discussion(결과 및 회고)

One disappointing aspect of this preject was the expectation that predictions would be accrate based on past values.

Furthermore, I did not handle data collection cleanly, and my lack of knowledge about GNN limited the modeling capabilities.
