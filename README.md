# Agricultural-product-price-prediction
5대 농산물의 가격을 예측하는 프로젝트 입니다.  
5대 농산물 : 배추, 양파, 마늘, 무, 고추  
  
## 1. 데이터 수집
* 출처 : KATI농식품수출정보, 공공데이터포털, 기상자료개발포털, 우리은행, KOSIS

![데이터정리](https://github.com/Ryan0hwan/Agricultural-product-price-prediction/assets/158720833/cec365ac-c1c4-4834-9a56-d1e51384a5e2)  

* 11개의 독립변수로 1개의 종속변수(소매가)예측.

![데이터예시](https://github.com/Ryan0hwan/Agricultural-product-price-prediction/assets/158720833/7381fe57-50a8-4f12-997c-4d16892e62b0)  

## 2. 데이터 전처리
* 금액 단위 통합(원 & 달러 -> 원)
* 결측치 처리 : 결측치가 많은 열은 열 삭제, 결측치가 적은 열은 열 전체의 평균값으로 대체(채소별로 다름)
* 정규화(MinMaxScaler)
* 데이터 분할(window size = 미정)
  
## 3. 모델 선정
* RNN, LSTM, GRU, lasso, ARIMA기법으로 비교를 통해 모델을 선정.
  
## 4. 모델 학습
## 5. 교차 검증
## 6. 결과 해석
## 7. 한계점
