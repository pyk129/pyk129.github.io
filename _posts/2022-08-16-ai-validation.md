---
title: Cross Validation(교차검증)
author: 
date: 2022-08-22 01:00:00 -0500
categories: AI
---

# 1. CrossValidation(교차검증)이란?
## 가. Unseen데이터셋 검증, CrossValidation 정의
Hold-out, k-fold기법을 사용해서 데이터셋에 대한 모델 퍼포먼스 향상과 과적합을 피하기 위한 목적으로 머신러닝 모델을 신뢰성 있게 평기하기 위한 검증기법

## 나. CrossValidation필요성


|필요성| 설명|
|:--:|:--:|
|unseen데이터 테스팅| unseen데이터에 대한 모델 검증을 수행함으로서 신뢰도 있는 모델 검증 |
|과적합 회피|Traning Set, Test Set등 하나의 데이터셋을 여러개의 데이터셋으로 나누어 모델을 검증함으로서 특정 데이터셋에 과적합 되는것을 방지|
|하이퍼파라미터 튜닝| CrossValidation 검증 수형 결과를 통해 최적화된 하이퍼 파라미터를 도출|


# 2. 머신러닝 파이프라인 내 CrossValidation와 유형설명
## 가. 머신러닝 파이프라인 내 CrossValidation

![Github_Logo](/assets/img/2022-09-02-ai-02-aivalidataion.png)
*머신러닝 학습 파이프라인 내 CrossValidation 유형*

## 나. CrossValidation 유형설명

<table>
<colgroup>
<col width="20%" />
<col width="50%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th>유형</th>
<th>개념도</th>
<th>설명</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">홀드아웃 방법(Holdout method)</td>
<td markdown="span">![Github_Logo](/assets/img/2022-09-02-ai-02-aivalication-holdout.png) </td>
<td markdown="span">데이터셋을 고정으로 분리해서 성능 검증 수행하는 검증 방식, 홀드아웃에 사용되는 데이터셋은 Train Set, Test Set의 2개로 나누거나 Train Set, Validation Set, Test Set등 3개로 분할해서 사용</td>
</tr>
<tr>
<td markdown="span">k-겹 교차검증(k-fold cross validation)</td>
<td markdown="span">![Github_Logo](/assets/img/2022-09-02-ai-02-aivalication-kfold.png) </td>
<td markdown="span">데이터셋을 k개의 서브셋으로 분리, k개의 데이터중 1개의 데이터만 테스트에 사용하고 나머지 k-1개의 데이터는 훈련에 사용하는 방법을 K번 반복해서 테스트 수행하는 검증 방식. 
                    검증에 사용된 성능 결과는 최종적으로 평균내어 사용</td>

</tr>
<tr>
<td markdown="span">리브-p-아웃 교차검증(Leave-p-out cross validation)</td>
<td markdown="span">![Github_Logo](/assets/img/2022-09-02-ai-02-aivalication-leave-p-out.png)</td>
<td>전체 데이서 셋 중에서 p개의 샘플을 선택해서 모델 검증에 사용하는 방법, k-겹 교차검증과의 차이는 k-겹 교차검증은 데이터셋을 k로 동일하게 분리후 1개의 샘플을 테스트셋으로 모델 검증에 사용하나 리브-p-아웃 교차검증은 전체 데이터 셋 중에서 p개의 샘플을 선택 후 선택된 p샘플로 모델 검증에 사용</td>
</tr>
</tbody>
</table>
- Holdout, k-fold는 비소모적 교차 검증 밥식, 리브-p-아웃 교차검증은 소모적 교차 검증 방식으로 구분
- CrossValidataion수행 후 훈련 모델 성능이 기대치에 달성 못할 경우 하이퍼 파라미터 조절을 통해 모델 훈련 재수행


# 3. Reference
[참고] - [https://m.blog.naver.com/ckdgus1433/221599517834](https://m.blog.naver.com/ckdgus1433/221599517834)
[참고] - [https://scikit-learn.org/stable/modules/cross_validation.html](https://scikit-learn.org/stable/modules/cross_validation.html)
