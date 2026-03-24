# 💧 i-LMS 기반 지능형 누수 판별 및 삼중 분류 모델 구축

본 프로젝트는 IoT 누수 감시 시스템(i-LMS)의 음압 데이터를 활용하여 누수 여부를 자동으로 판정하고, 판정의 신뢰도를 지수화하는 머신러닝 기반 솔루션입니다.

## 🚀 주요 성과
- **데이터 규모**: 약 15,000개의 히스토그램 데이터 통합 및 분석
- **판정 논리**: 3단계 누수 판단 로직(지속성, 음압, 분포) 정립
- **모델 성능**: **Recall(재현율) 99%** 달성 (위험군 탐지 특화)
- **핵심 지표**: 누수 신뢰지수(Reliability Score) 개발을 통한 2단계 검증 체계 수립

## 🧠 3단계 누수 판단 로직
1. **지속성(Consistency)**: 시간대별 상관계수(Avg_Corr) 분석
2. **음압(Amplitude)**: 기저 소음 및 최빈값(Daily_Peak) 분석
3. **분포(Distribution)**: 에너지 밀집도(Peak_Ratio) 분석

## 📁 파일 구성
- `01_data_merging.py`: 데이터 통합
- `02_feature_extraction.py`: 3단계 로직 지표 산출
- `04_data_labeling.py`: 통계 기반 삼중 분류(0,1,2)
- `05_model_training.py`: Random Forest 모델 학습
- `06_model_evaluation.py`: 성능 평가 및 신뢰 지수 산출
