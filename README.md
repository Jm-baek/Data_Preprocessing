# Project 1. 태양광 발전량 예측

Tip : 논문 검색시, Review 논문을 통해 연구하고자 하는 분야의 Summary와 흐름을 파악하는 것이 도움이 된다.
      Review 논문은 선행 연구들의 연구 방향(흐름)과 사용 모델 및 데이터 등에 대해 요약을 해놓은 논문이다.

Reference literature(참고 문헌)
JCR web을 통해 학회 수준을 확인할 수 있다.(Elsevier에 있는 학회 논문에 실려진 논문들이 좋다)

[1] Sobri, S., Koohi-Kamali, S., & Rahim, N. A. (2018). Solar photovoltaic generation forecasting methods: A review. Energy Conversion and Management, 156, 459-497.
[2] Antonanzas, J., Osorio, N., Escobar, R., Urraca, R., Martinez-de-Pison, F. J., & Antonanzas-Torres, F. (2016). Review of photovoltaic power forecasting. Solar Energy, 136, 78-111.
[3] Sangrody, H., Sarailoo, M., Zhou, N., Tran, N., Motalleb, M., & Foruzan, E. (2017). Weather forecasting error in solar energy forecasting. IET Renewable Power Generation, 11(10), 1274-1280.
[4] Carrera, B., Sim, M. K., & Jung, J. Y. (2020). PVHybNet: a hybrid framework for predicting photovoltaic power generation using both weather forecast and observation data. IET Renewable Power Generation, 14(12), 2192-2201.


1. 데이터 수집
  기상 관측데이터와 기상 예보데이터는 특징 차이가 있다.
  기상 관측데이터는 기상 관측소에서 측정한 데이터로 다양한 기상 요소 데이터를 수집할 수 있으며, 데이터의 정확도에 신뢰를 할 수 있다.
  기상 예보데이터는 기상 관측데이터를 사용하여 예측된 데이터로 가장 큰 단점으로는 기상의 변동성(variability), 불확실성(uncertainty)으로 인한 모델 정확도 성능에 영향을 준다.
  

  1) 수집 데이터 사이트
  
    기상자료개방포털: https://data.kma.go.kr/cmmn/main.do (독립 변수 수집)
    공공데이터포털 : https://www.data.go.kr/ (종속변수 수집)

  2) Data summary
  
독립 변수(input/dependent/explanatory variable) :  
 
 모델 생성을 위한 데이터, 미래 시간에 대한 태양광 발전량 예측을 위한 기상 예보 데이터
  
  2-1) 기상 예보 데이터
  
    - 초단기(forecast 1 hour ahead) 
    
      Date(target_time),	Time(Derived variable), Temperature, WindSpeed,	WindDirection, Humidity,	Cloud amount (tgt_time은 인덱스 외, 총 6개 변수)
   
    - 단기(forecast 4, 7, 13, 22 hour ahead)

      Date(target_time),	time(Derived variable),	Temperature, WindSpeed,	WindDirection, Humidity,	SkyType (tgt_time은 인덱스 외, 총 6개 변수
    
기상 관측 데이터
  
  
  
  파생 변수(Derived variable) : Time column(시간)
  
  종속 변수(Output, independent variable) : 전라남도 영암 태양광 발전량


2. 탐색적 데이터 분석(EDA)
