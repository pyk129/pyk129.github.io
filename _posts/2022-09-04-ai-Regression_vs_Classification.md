---
title: Regression vs Classification
author: 
date: 2022-09-05 00:00:00
categories: AI
---

# 1. Regression(회귀)와 Classification(분류)의 개념?

## 회귀(Regression)란?
------------
여러개의 독립변수(x)와 종속변수(y)의 상관관계를 통해 연속성(Continuous)을 지니고 실수로 표현되는 종속변수(y)를 예측하는 방법
- 독립변수는 Feature, 종속변수는 Label로 표현
- 연속성이란 연속적으로 분포되는 값을 뜻함, 공부시간, 온도, 자동차속도, 나이와 같이 끊어지지 않고 연속적으로 그릴수 있는 성질을 연속성이라 함
- 회귀분석이란 종속변수 Label에 해당하는 여러 개의 Feature값을 찾는 목표로하는 분석기법으로 현재의 데이터를 통해 미래를 예측 하기위한 머신러닝 기법
- Feature(편의시설 거리, 지하철역 거리), Label(집 가격)을 통해 집값의 상승률(실수)을 예측


## 분류(Classification)란?
------------
여러개의 독립변수(x)와 종속변수(y)의 상관관계를 통해 독립변수에 대응하는 값들이 어떤 이산값(Discrete)값을 가지는 클래스(y)에 속하는지 예측하는 방법  
- 분류의 개수에 따라 이진 분류(Binary classification) 다중 븐류로(Multi-class classification) 구분
- 이진 분류의 예로 스팸 메일이 존재, 스팸 인지(YES)? 아닌지(NO) 총 2가지로 분류 하는 방법이 이진분류
- 다중 분류의 예로 감정분석이 존재, 입력 텍스트(x)에 대해 좋음, 중립, 나쁨 등 3가지 이상으로 분류하는 방법이 다중분류


# 2. Regression(회귀)와 Classification(분류) 개념도 및 상세 비교
------------

## 가. Regression(회귀)와 Classification(분류) 개념도

![Github_Logo](/assets/img/2022-09-05-ai-01-regression_vs_classification.png)
*Regression vs Classification*

## 나.  Regression(회귀)와 Classification(분류) 상세 비교




<table>
<colgroup>
<col width="20%" />
<col width="40%" />
<col width="40%" />
</colgroup>
<thead>
<tr class="header">
<th>구분</th>
<th>Regression</th>
<th>Classification</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">예측값</td>
<td markdown="span">- 연속값</td>
<td markdown="span">- 이산값</td>
</tr>

<tr>
<td markdown="span">목적</td>
<td markdown="span">- 데이터의 예측(학습된 데이터 기준)</td>
<td markdown="span">- 데이터의 분류(학습된 데이터 기준)</td>
</tr>

<tr>
<td markdown="span">알고리즘</td>
<td markdown="span">- 선형 회귀(Linear Regression)</td>
<td markdown="span">- 로지스틱 회귀(Logistic Regression)</td>
</tr>

<tr>
<td markdown="span">비용함수</td>
<td markdown="span">
- 평균 절댓값 오차 (MAE : Mean absolute error)<br>
- 평균 제곱 오차 손실 (MSE : means squared error)<br>
- 평균 제곱근 오차 (RMSE : Root mean squared error)<br>                  
</td>

<td markdown="span">
- Cross-Entropy<br>
- KL Divergence(Kullback-Leibler Divergence)<br>
- Softmax
</td>
</tr>

<tr>
<td markdown="span">사용예</td>
<td markdown="span">- 키에 따른 몸무게 BMI 예측<br>
- 공부시간에 따른 성적 변화 예측 
</td>
<td markdown="span">- 환자가 암인지 아닌지 분류<br>
- 메일이 스팸인지 정상 메일인지 분류  
</td>
</tr>


</tbody>
</table>



# 3. Reference
[참고] - [https://www.simplilearn.com/regression-vs-classification-in-machine-learning-article](https://www.simplilearn.com/regression-vs-classification-in-machine-learning-article)
