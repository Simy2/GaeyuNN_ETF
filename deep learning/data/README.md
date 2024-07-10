## 데이터 셋들의 구성은 아래와 같습니다 <br>
The composition of the datasets is as follows:

### 1. 2010~2024_marchLastDay_allStockInfo

2024년부터 2010년까지 모든 주식 종목들의 3월 마지막 날의 종가를 가지고 옴 <br>
Data containing the closing prices of all stock items on the last day of March from 2010 to 2024.

종목코드+날짜 : <br>
 종목코드와 날짜의 조합 ex)095570/20240329 == 24년 3월 29일의 095570종목의 종가 <br>
 Combination of stock code and date (e.g., 095570/20240329 == Closing price of stock 095570 on March 29, 2024).

종목명 : <br>
 종목명 <br>
 Stock name.

시장구분 :  <br>
 kospi, kosdaq <br>
 Market division (kospi, kosdaq).

업종명 : <br>
 섹터 <br>
 Sector.

종가 : <br>
 가격 <br>
 Closing price.

대비 : <br>
 전날 대비 가격 변화량(1년단위가 아님) <br>
 Price change from the previous day (not yearly).

등략률 : <br>
 전날 대비 가격 변화 퍼센트(1년단위가 아님) <br>
 Percentage change from the previous day (not yearly).

시가총액 : <br>
 시가총액 <br>
 Market capitalization.

### 2. 2020~2024_marchLastDay_etfProfit_with_kospiProfit_and_kospiStd

2024년부터 2020년까지 3월 말의 krx에 있는 모든 etf종목들의 1년 단위 수익률 정보 및 1년간 코스피 수익률 및 1년간 코스피 표준편차 <br>
Yearly profit information of all ETF items listed on KRX from 2020 to 2024, as of the end of March, along with yearly returns of Kospi and Kospi's standard deviation.

etf코드 : <br>
 etf코드 <br>
 ETF code.

날짜 : <br>
 날짜 <br>
 Date.

수익률 : <br>
 etf의 1년대비 수익률 <br>
 Yearly profit percentage of the ETF.

1년간 코스피 수익률 : <br>
 1년대비 코스피의 변화률 <br>
 Yearly percentage change of Kospi.

1년간 코스피 std : <br>
 1년 대비 코스피의 표준편차 <br>
 Standard deviation of Kospi over the year.

### 3. 2020~2024_marchLastDay_stockInfo_in_etf

2024부터 2020년까지 3월 말의 krx에 있는 모든 etf종목들의 구성 항목들을 보여줌 <br>
Composition details of all ETF items listed on KRX as of the end of March from 2020 to 2024.

구성 비중 : <br>
 etf를 구성하고 있는 항목의 비중 <br>
 Composition ratio of items in the ETF.

etf코드 : <br>
 etf코드 <br>
 ETF code.

종목코드 : <br>
 etf를 구성하고 있는 항목의 종목 코드 <br>
 Stock code of items in the ETF.

날짜 : <br>
 해당 날짜 <br>
 Date.

시장구분 : <br>
 kospi, kosdaq, 현금 <br>
 Market division (kospi, kosdaq, cash).

업종명 : <br>
 섹터와 현금 <br>
 Sector and cash.

시가총액 : <br>
 시가총액 <br>
 Market capitalization.

주식 종류 : <br>
 보통주, 우선주, 현금 <br>
 Stock type (common stock, preferred stock, cash).

per, pbr, pcr, psr : <br>
 현금은 다 0임 <br>
 Value indicators (cash is all 0).

종가 : <br>
 현금은 1임 <br>
 Closing price (cash is 1).

종목 자산액 : <br>
 etf를 구성하고 있는 항목의 자산액수 <br>
 Asset amount of items in the ETF.

로그 수익률 : <br>
 etf를 구성하고 있는 항목의 1년간 로그 수익률 <br>
 Log return of items in the ETF over the year.

### 4. 2019~2024_marchLastDay_etfInfo

2019년부터 2024년까지의 etf정보들 <br>
ETF information from 2019 to 2024.

단축코드 : <br>
 etf의 단축코드 <br>
 ETF's abbreviation code.

시가총액 : <br>
 etf의 시가총액 <br>
 ETF's market capitalization.

날짜 : <br>
 날짜 <br>
 Date.

표준코드 : <br>
 etf의 표준 코드 <br>
 ETF's standard code.


### 5. 2020~2024_marchLastDay_stocksInfo_with_valueIndex

2024년부터 2020년까지의 3월 마지막날의 주식 종목들의 정보를 보여줌 <br>
Information of stocks listed on KRX as of the end of March from 2020 to 2024.

시장 구분 : <br>
 kospi, kosdaq <br>
 Market division (kospi, kosdaq).

업종명 : <br>
 섹터 <br>
 Sector.

시가총액 : <br>
 시가총액 <br>
 Market capitalization.

종목코드 : <br>
 종목코드 <br>
 Stock code.

날짜 : <br>
 날짜 <br>
 Date

주식 종류 : <br>
 보통주, 우선주 <br>
 Stock type (common stock, preferred stock).

per,pbr,pcr,psr : <br>
 가치지표 <br>
 Value indicators.

### 6. 2010~2024_marchLastDay_stockProportion_in_etf

2024년부터 2010년까지의 3월 마지막날의 etf의 날짜 별 종목코드 보여줌 <br>
ETF's date-wise stock codes as of the end of March from 2010 to 2024.

종목코드_날짜 : <br>
 etf를 구성하고 있는 종목코드와 해당 날짜를 보여줌 <br>
 Displays the stock code and the date of the ETF's components.

구성비중 : <br>
 etf를 구성하고 있는 종목의 구성비중을 보여줌 <br>
 Displays the composition ratio of the ETF's components.

etf코드 : <br>
 etf의 표준코드 <br>
 ETF's standard code.

### 7. presentStockInfo

현재 kospi와 kosdaq 모두의 주식 정보를 보여줌 <br>
Displays current stock information for both KOSPI and KOSDAQ.

표준코드 : <br>
 종목의 표준코드 <br>
 Stock's standard code.

단축코드 : <br>
 종목의 단축코드 <br>
 Stock's abbreviation code.

한글 종목명 <br>
Korean stock name.

한글 종목 약명 <br>
Korean stock abbreviation.

영문 종목명 <br>
English stock name.

상장일 : <br>
 증권이 언제 상장되었는지 <br>
 Listing date of the security.

시장구분 : <br>
 kospi, kosdaq <br>
 Market division (kospi, kosdaq).

증권구분 : <br>
 '주권', '부동산투자회사', '주식예탁증권', '외국주권', '사회간접자본투융자회사', '투자회사' <br>
 Security type ('주권', '부동산투자회사', '주식예탁증권', '외국주권', '사회간접자본투융자회사', '투자회사').

소속부 : <br>
 중견기업부 등등 <br>
 Affiliation (중견기업부 등등).

주식 종류 : <br>
 '보통주', '구형우선주', '신형우선주', '종류주권' <br>
  Stock type ('common stock', 'preferred stock (old type)', 'preferred stock (new type)', 'preferred shares').

상장 주식수 : <br>
 몇개의 주식이 상장되어 있는지  <br>
 Number of shares listed.
