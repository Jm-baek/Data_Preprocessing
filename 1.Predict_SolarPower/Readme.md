# Project 1. 태양광 발전량 예측
정말 많은 것을 배울 수 있었고 한편으로는 아쉬움이 남는 프로젝트이다.

## 1. Data description 

  1-1) 수집 데이터 사이트 <BR/>
  
      기상자료개방포털: https://data.kma.go.kr/cmmn/main.do (독립 변수 수집) 
      공공데이터포털 : https://www.data.go.kr/ (종속변수 수집) 

  1-2) Data summary <BR/>
   + 기상 관측데이터 <BR/>
     + 장점 <BR/>
     > 기상 관측소에서 측정한 데이터로 다양한 기상 요소 데이터를 수집할 수 있으며, 데이터의 정확도에 대해 신뢰를 할 수 있다. 

     + 단점 <BR/>
     > 현재시간에 대해 기상 데이터를 가지고 있다.(다시 말하면, 필요한 미래의 시간이 없다.) 
            
   + 기상 예보데이터(초단기예보, 단기예보) <BR/>
     + 장점 <BR/>
     > 미래 시간을 가지고 있어 미래 시간의 태양광 발전량을 예측할 수 있다. <BR/>
     + 단점 <BR/>
     > 기상의 변동성(variability), 불확실성(uncertainty)으로 데이터의 quality 문제로 모델 정확도 성능에 영향을 준다. <BR/>
     > (다시 말하면, 기상이 다양한 이유로 시간이 흐르면서 항상 변하기 때문에 정확한 미래의 기상 데이터를 얻기 어렵다.) <BR/>
   + 파생 변수(Derived variable <BR/>
     + Data Column으로 부터 time을 추출 <BR/>
  
## 2. Data Preprocessing <BR/>
위 사이트에서 데이터를 다운받아보면 바로 사용할 수 없게 데이터가 구성이 되어있다. <BR/>
가급적 외국의 잘 되어 있는 기상 데이터를 사용하기를 추천한다.(전반적으로 데이터의 quality(결측치,정확도 등) 문제와 전처리 시간이 많이 소요된다.) <BR/>

  2-1) Missing data imputation  <BR/>
데이터 전처리를 하며 결측값이 상당히 많은 것을 알 수 있었고 해결하기 위해 논문을 찾아 보았다. <BR/>
데이터 결측값 처리에 대해서 정말 많은 논문들이 있다. 아마도 데이터 결측값의 처리 방법에 따라 모델의 성능에 많은 영향을 줄 수 있기 때문에으로 생각된다. <BR/>
가장 기본적인 0값으로 처리, 결측값 제거, 평균(mean), 중앙값(median), 최빈값(mode)에서부터 보간법(interpolation) 등 외에도 더 심화된 방법들이 있다. <BR/>
> 본 연구에서는 linear interpolation 으로 처리를 했다.
> !!! linear interpolation에 대해 설명을 조금 더 작성이 필요.!!!!!



## 3. Models
태양광 발전량의 예측하는 방법에는 전체적으로 세 가지 방법이 있다. (
3-1) 
 
 
 
 
 
 4. 예측 결과
      

**Reference literature(참고 문헌)** <BR/>
JCR web을 통해 학회 수준을 확인할 수 있다.(Elsevier에 있는 학회 논문에 실려진 논문들이 좋다) <BR/>
Review 논문은 선행 연구들의 연구 방향(흐름)과 사용 모델 및 데이터 등에 대해 요약을 해놓은 논문이다. <BR/>

[1] Sobri, S., Koohi-Kamali, S., & Rahim, N. A. (2018). Solar photovoltaic generation forecasting methods: A review. Energy Conversion and Management, 156, 459-497. <BR/>
[2] Antonanzas, J., Osorio, N., Escobar, R., Urraca, R., Martinez-de-Pison, F. J., & Antonanzas-Torres, F. (2016). Review of photovoltaic power forecasting. Solar Energy, 136, 78-111. <BR/>
[3] Sangrody, H., Sarailoo, M., Zhou, N., Tran, N., Motalleb, M., & Foruzan, E. (2017). Weather forecasting error in solar energy forecasting. IET Renewable Power Generation, 11(10), 1274-1280. <BR/>
[4] Carrera, B., Sim, M. K., & Jung, J. Y. (2020). PVHybNet: a hybrid framework for predicting photovoltaic power generation using both weather forecast and observation data. IET Renewable Power Generation, 14(12), 2192-2201. <BR/>

     
