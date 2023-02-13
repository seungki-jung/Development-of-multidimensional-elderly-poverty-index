# 노인빈곤격차지수 개발을 통한 사회적 돌봄가치 실현


#### 프로젝트 기간 : 2022.07.27 ~ 2022.08.19
#### 사용한 분석 도구 : Python, QGIS
#### 참여자 : 채정연, 이지호, 이한빈, 정승기, 최보미, 함승완

#### ※Term Definition
<img src="https://user-images.githubusercontent.com/76424262/217400021-5f6663a1-ff0c-4289-b4c0-f816c9c14443.PNG">

## 1. Object
<img src="https://user-images.githubusercontent.com/76424262/217398017-fc055399-c85b-4bcf-a0f5-a56638857a81.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217398125-689290af-bcf8-4cfd-be9c-f26e90868387.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217399947-e08fb682-526b-4ebe-b947-2d6eb24b1987.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217400096-ba61e72b-2110-4441-bce6-b191ba316ae6.PNG">

## 2. Modeling Process
<img src="https://user-images.githubusercontent.com/76424262/217400141-06e3a259-c1a0-4f14-b1e8-0957b72f6606.PNG">

## 3. Summary

### Index Definition
<img src="https://user-images.githubusercontent.com/76424262/217400200-3da58d4d-40f4-499f-9291-71b852b40fee.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217400253-61611783-5531-4b87-8564-7cfa8a8db225.PNG">

- '노인빈곤'과 밀접한 키워드, 논문 조사를 통해 노인빈곤격차를 5개의 지표('복지', '일자리', '소득', '만족도', '인구학적 특성')로 정의
- 각 요인 데이터의 특성에 따라 각각 상관분석, 회귀분석, 군집분석을 수행하여 가중치 산정. 상관분석 지수의 경우 편차 감소를 위해 표준화
- 최종 지수 산출식 = 연금 + 인구학적 특성 + 복지 - 만족도 - 일자리

#### (1) 일자리, 연금, 인구학적 특성
<img src="https://user-images.githubusercontent.com/76424262/218348123-215f20c3-71d5-439d-9bc9-cd1907e8c56f.PNG">
<img src="https://user-images.githubusercontent.com/76424262/218348165-37c76be4-58b2-4a70-8213-19bc3869a96b.PNG">

#### (2) 만족도
<img src="https://user-images.githubusercontent.com/76424262/218348192-8afe0fa8-5455-422f-9166-65cd097fb7d7.PNG">
<img src="https://user-images.githubusercontent.com/76424262/218348238-3fecf8fc-dc0c-45d6-99b5-e22fb156b58a.PNG">
<img src="https://user-images.githubusercontent.com/76424262/218348283-97bb2799-e9ea-4002-aebd-1ecffba75292.PNG">
<img src="https://user-images.githubusercontent.com/76424262/218348322-19a6867e-6516-46fc-9644-2802115410c8.PNG">

- 일부 변수 간 상관성이 높아 PCA를 통해 차원 축소 
- 차원 축소 후 회귀분석 실시 (VIF를 통해 다중공선성 체크, 회귀분석의 4가지 가정 체크)  
- 논문을 참고하여 회귀계수를 이용한 가중치 산정식(각 변수의 회귀계수 ÷ 회귀계수의 합)에 대입, 최종 만족도 지수를 만듦

#### (3) 복지
<img src="https://user-images.githubusercontent.com/76424262/218348373-dd79b6b8-1d34-4cb2-9d3b-bff0483ac21e.PNG">

- 상관분석 결과 모든 변수에서 상관성이 무의미하였기 때문에 유사성을 보고자 하였고 군집분석 실시
- AgglomerativeClustering, K-means Clustering 군집 2-5개를 대상으로 실루엣 계수를 본 결과 K-means Clustering 군집이 3일 때 실루엣 계수가 가장 높았으므로 k=3으로 하여 K-means 분석 실시
- K-means Clustering 후 산점도 행렬을 통한 군집의 특성 검토

### Modeling Results
<img src="https://user-images.githubusercontent.com/76424262/217400339-5c881b64-33f4-43b1-8092-7ea6d635f918.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217400491-26c2c743-cf94-4d5e-a2cd-b7413ca08173.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217400557-34c6bda7-a2b7-4aaf-8f3e-1552a5cb6e55.PNG">

## 4. Conclusion
<img src="https://user-images.githubusercontent.com/76424262/217403475-d2135e90-a83d-4c8c-a28b-a15ea1a40c23.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217403545-926b46df-79b9-41ee-be17-60c02938c664.PNG">
