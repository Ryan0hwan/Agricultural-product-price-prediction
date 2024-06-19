# Compare_RNN_LSTM_GRU
RNN, LSTM, GRU 중 어떤 인공신경망 모델이 농산물 가격을 가장 잘 예측하는지를 비교하는 프로젝트입니다.  
농산물 : 배추, 양파, 마늘, 무, 고추(5대 농산물)  
  
## 1. 데이터 수집
* 출처 : KATI농식품수출정보, 공공데이터포털, 기상자료개발포털, 우리은행, KOSIS

![데이터정리](https://github.com/Ryan0hwan/Agricultural-product-price-prediction/assets/158720833/cec365ac-c1c4-4834-9a56-d1e51384a5e2)  

* 11개의 독립변수로 1개의 종속변수(소매가)예측.

![데이터예시](https://github.com/Ryan0hwan/Agricultural-product-price-prediction/assets/158720833/7381fe57-50a8-4f12-997c-4d16892e62b0)  

## 2. 데이터 전처리
* 금액/무게 단위 통합(원 & 달러 -> 원 / t, g -> kg)
* 결측치 처리 : 결측치가 많은 열은 열 삭제, 결측치가 적은 열은 열 전체의 평균값으로 대체(채소별로 다름)
* 정규화(MinMaxScaler)
* Feature값 선정(f_regression, SFS, rfe, rfecv 이렇게 4가지 방법을 사용하여 나온 변수들 중, 최소 2가지 방법에서 나온 변수를 feature로 선정)
  
## 3. 모델 학습
* 파라미터와 함수 설정([LSTM 네트워크를 활용한 농산물 가격 예측 모델(2018.11)](https://scienceon.kisti.re.kr/commons/util/originalView.do?cn=JAKO201809469053682&oCn=JAKO201809469053682&dbt=JAKO&journal=NJOU00292001) 참고)
![parameter](https://github.com/Ryan0hwan/Compare_RNN_LSTM_GRU/assets/158720833/c122686a-6720-4e22-b028-bd1a7c03d7da)

## 4. 결과 해석
![1](https://github.com/Ryan0hwan/Compare_RNN_LSTM_GRU/assets/158720833/8d01f6ca-6814-4bc6-9f3c-e28cf29cd232)
![2](https://github.com/Ryan0hwan/Compare_RNN_LSTM_GRU/assets/158720833/11cb354e-41e3-4971-ad69-e43db1ed3e34)
![3](https://github.com/Ryan0hwan/Compare_RNN_LSTM_GRU/assets/158720833/cffd7d2a-ed40-4b8c-a387-756a1beb8413)



## 6. 한계점
* LSTM모델을 통해, 가격 예측까지는 가능한 것으로 보이나, LSTM모델 자체의 한계로 어떤 변수가 가장 큰 영향을 끼치는지는 알 수 없음.
* 모델의 평가지표 중 MAPE값이 높게 형성되어 있어 보완이 필요함. 


