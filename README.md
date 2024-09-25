# 데이콘 물류 유통량 예측 AI 경진대회
2021-DACON-Logistics-Distribution-Volume-Prediction-Competition

<br/>

## 1. 배경 & 목적

- 코로나 19는 경제, 사회 분야의 구조적 변화를 촉발하여 비대면화와 디지털 전환을 가속화 시키고 있으며, 비대면 거래의 증가에 따라 2020년 택배 물량은 약 30억 건으로 전년 대비 21% 급증하였음.
- 제주시 내 택배 운송 데이터를 이용하여 운송량 예측 AI 개발
- 평가 지표: RMSE

<br/>

## 2. 주최/주관 & 참가 대상 & 성과

- 주최/주관: 국토연구원 / DACON
- 참가 대상: 일반인, 학생 등 누구나
- 성과: 상위 6%

<br/>

## 3. 대회 기간

- 제출마감: 2021년 12월 20일
- 코드 평가 마감 및 최종순위 발표: 2020년 12월 29일

<br/>

## 4. 내용
- 송하인_격자공간고유번호, 수하인_격자공간고유번호, 택배_카테고리로 구성된 데이터로 운송장 건수(Regression)을 예측하는 문제임.
- 전국 시/도 격자공간 데이터를 추가적으로 활용하였음.
- 송,수하인 격자공간고유번호를 활용하여 일치여부 Feature를 생성하였음.
- 지역별 집계피처를 활용하였음.
- 범주형 변수가 대부분임을 고려하여 Catboost를 사용하였음.
- 이외, ExtraTrees, Tabnet을 사용하여 일반화 성능을 최적화하고자 하였음.

<br/>

## 5. Process

### ch.1 Feature Engineering

- EDA
- Only Categorical Features
- Match or Not Feature
- Aggregation Feature

---

### ch.2 Preprocessing
- Aggregation by Region
- One-hot Encoding

---

### ch.3 Modeling

- ExtraTrees
- Catboost
- Tabnet

---

### ch.4 Ensemble

- Weighted Ensemble
- Tabnet 5 : ExtraTrees 2 : Catboost 3

<br/>

## 6. 참고자료

[데이콘 물류 유통량 예측 AI 경진대회 사이트](https://dacon.io/competitions/official/235867/overview/description)
