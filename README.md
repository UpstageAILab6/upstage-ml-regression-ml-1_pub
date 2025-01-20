[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/pjJxrz8e)
# MOASIS
## Team

| <img src="img/cat.png" alt="김솔하" width="160"> | <img src="img/upa.png" alt="전종훈" width="160"> | <img src="img/dog.png" alt="심원형" width="160"> | <img src="img/ori.png" alt="김지혜" width="160"> | <img src="img/yong.png" alt="김용욱" width="160"> |
| :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: |
|            [김솔하](https://github.com/usershkim)             |            [전종훈](https://github.com/Jackjack5922)             |            [심원형](https://github.com/Shimwonhyung)             |            [김지혜](https://github.com/bebe217)             |            [김용욱](https://github.com/wizporter7)             |
|                   팀장, 전체과정참여/조율                             |                            모델선택/모델 학습                             |                            전처리/모델 학습                             |                            모델학습/PPT작성                             |                            인사이트제공/PPT작성                             |

## 0. Overview
### Environment
- Jupyter Notebook
- Ubuntu
- VScode
- python
- numpy, pandas
- sklearn
- matplotlib, seaborn

### Requirements
- catboost==1.2.7
- eli5==0.13.0
- numpy==1.23.5
- optuna==4.1.0
- pandas==1.5.3
- scikit-learn==1.0.2
- scipy==1.15.0
- seaborn==0.12.2

## 1. Competiton Info

### Overview

- 서울시 아파트 실거래가 매매 데이터를 기반으로 아파트 가격을 예측하는 대회

### Timeline

- 2024.12.23 - Start Date
- 2025.01.07 - Final submission deadline

## 2. Components

### Directory

- 중심 아이디어 및 전처리 데이터를 토대로 각자 학습을 맡아 하였기에 정해진 공통된 구조는 딱히 없습니다.

## 3. Data descrption

### Dataset overview

- 매매 거래 기록
- 주소, 아파트명, 전용면적, 기타 아파트 정보 칼럼 존재
- 2000년대 자료부터 존재


### EDA

- 결측치가 75%이상인 칼럼 다수 존재
- 아파트명, 좌표 x, 좌표y 결측치 존재

### Data Processing

- 외부 Geo 데이터를 활용해 좌표 결측치 입력
- 좌표 정보로 지하철과의 거리 계산하여 역세권 여부 추가
- 외부 주담대 금리 데이터 추가
- 외부 공시지가 데이터 추가
- 중요도 낮은 항목 제거
- 전용면적 IQR 이상치 제거
- 레이블 인코딩 및 결측값 보강

## 4. Modeling

### Model descrition

여러가지 모델을 돌려보고 좋은 결과의 모델로 선택

- LASSO, ElasticNet - 선형 모델로 선정
- RandomForest - 기본 제공된 학습 코드
- XGBoost - 성능이 좋은 모델
- LightGBM - 빠르고 성능도 좋은 모델

### Modeling Process

![score](img/result.png)

## 5. Result

### Leader Board

![score](img/score.png)
- 6등/ 29306.6490

### Presentation

- [발표자료](https://docs.google.com/presentation/d/1nTcL5LJ_7hDxfTjB61SsPNEJOHDtLycrnbwKzs_Omrc/edit?usp=drive_link)

## etc

### Meeting Log

- [Team Notion](https://www.notion.so/1-_MOASIS-538dbce2050d491bb806b56a610387e9?pvs=4)
