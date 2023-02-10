# 노인빈곤격차지수 개발을 통한 사회적 돌봄가치 실현

#### 참여자 : 채정연, 이지호, 이한빈, 정승기, 최보미, 함승완
#### 프로젝트 기간 : 2022.07.27 ~ 2022.08.19
#### 사용한 분석 도구 : Python, QGIS

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

### Modeling Results
<img src="https://user-images.githubusercontent.com/76424262/217400339-5c881b64-33f4-43b1-8092-7ea6d635f918.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217400491-26c2c743-cf94-4d5e-a2cd-b7413ca08173.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217400557-34c6bda7-a2b7-4aaf-8f3e-1552a5cb6e55.PNG">

## 4. Conclusion
<img src="https://user-images.githubusercontent.com/76424262/217403475-d2135e90-a83d-4c8c-a28b-a15ea1a40c23.PNG">
<img src="https://user-images.githubusercontent.com/76424262/217403545-926b46df-79b9-41ee-be17-60c02938c664.PNG">
