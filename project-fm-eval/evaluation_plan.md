# 🧪 Enterprise-Grade Foundation Model Evaluation Plan
> **Project**: Comparative Analysis of Solar Pro 2 vs. Global SOTA in Finance & Medical Domains
> **Researcher**: [devfyoo2829-lab]

[cite_start]본 계획서는 개인 연구 목적으로 최신 파운데이션 모델의 성능을 탐구하되, **엔터프라이즈급 평가 기준(HELM, G-Eval 등)**을 준수하여 실제 기업 도입 시 기술적 레퍼런스로 활용 가능한 수준의 데이터를 도출하는 것을 목표로 합니다. [cite: 92, 95]

---

## 1. 실험 목적 및 가설 (Objective & Hypothesis)

### 1.1 실험 목적
* [cite_start]**도메인 특화 성능 검증**: 금융 및 의료 도메인에서 모델의 전문성 및 신뢰성을 정량화합니다. [cite: 1, 94]
* [cite_start]**의사결정 근거 마련**: 환각 위험, 운영 비용, 지연 시간을 동시에 분석하여 최적의 배포 전략을 수립합니다. [cite: 6, 94]

### 1.2 핵심 가설
* [cite_start]**H-01 (도메인 우위)**: 도메인 특화 모델은 범용 LLM 대비 Domain F1 Score에서 **8%p 이상의 우위**를 보일 것이다. [cite: 10, 99]
* [cite_start]**H-02 (신뢰성)**: 기업용 신뢰성 임계값인 **Hallucination Rate < 5%**를 만족하는 모델이 존재할 것이다. [cite: 7, 132]
* [cite_start]**H-03 (효율성)**: 동일 품질 수준에서 Solar Pro 2는 GPT-4o 대비 높은 **비용 효율성(CEI ≤ 1.5)**을 보일 것이다. [cite: 29, 103]

---

## 2. 평가 대상 모델 (Baseline Models)

| 역할 | 모델명 | 특징 | 비고 |
| :--- | :--- | :--- | :--- |
| **🏆 Champion** | **Solar Pro 2** | 70B+, 128k Context | [cite_start]주 평가 대상 [cite: 19, 110] |
| **📌 Baseline A** | **GPT-4o** | 글로벌 SOTA 모델 | [cite_start]성능 기준점 [cite: 19, 112] |
| **📌 Baseline B** | **Claude 3.5 Sonnet** | 장문 처리 및 추론 강점 | [cite_start]비교군 [cite: 19] |
| **📌 Baseline C** | **HyperCLOVA X** | 국내 도메인 경쟁 모델 | [cite_start]한국어 특화 비교 [cite: 19] |

---

## 3. 정량적 평가 지표 (KPIs)

### 3.1 성능 및 안전성 (Quality & Safety)
* [cite_start]**Performance**: Domain F1-Score (≥ 0.82), Exact Match (EM), G-Eval Score (5축 평가). [cite: 25, 121-127]
* [cite_start]**Reliability**: **Hallucination Rate (< 5%)**, Truthfulness Score (≥ 0.70). [cite: 27, 132-137]
* [cite_start]**Safety**: Toxicity Score (≤ 0.05), **PII Leakage Rate (< 0.1%)**. [cite: 27, 138-142, 158]

### 3.2 운영 효율성 (Efficiency)
* [cite_start]**Latency**: TTFT P95 ≤ 800ms, TPS ≥ 40. [cite: 29, 145-148]
* [cite_start]**Cost**: Cost-Efficiency Index (CEI) ≤ 1.5 (GPT-4o 대비 성능 향상률/비용 증가율). [cite: 29, 227-231]

---

## [cite_start]4. 도메인 특화 데이터셋 전략 (Dataset Strategy) [cite: 30-33, 164-165]

### 4.1 금융 도메인 (Finance)
* [cite_start]**재무제표 분석**: 수치 추출 및 해석 (CPA 검수 정답지 활용). [cite: 35]
* [cite_start]**규정 해석**: 금융감독원 가이드라인 기반 법령 적용 판단. [cite: 35]

### [cite_start]4.2 의료 도메인 (Medical) - 개인 데이터 활용 [cite: 173-174]
* [cite_start]**의무기록 요약**: 개인 의료 내역 사본을 활용한 **SOAP 형식** 요약 품질 평가. [cite: 39]
* [cite_start]**임상 가이드라인**: 대한의학회 가이드라인 기반 근거 중심 의학(EBM) 판단. [cite: 39]
* [cite_start]**약물 상호작용**: 복용 약물 간 위험도 설명 생성 및 이진 분류. [cite: 39]

---

## 5. 개인정보(PII) 마스킹 전략 (Data De-identification)

개인 의료 데이터를 안전하게 사용하기 위해 아래 단계를 준수합니다.

1. **자동 마스킹**: 정규표현식(Regex) 또는 마스킹 전용 라이브러리(Presidio 등)를 사용하여 이름, 전화번호, 주민번호, 주소 등을 비식별화합니다.
2. [cite_start]**합성 데이터 혼합**: 실제 데이터의 구조는 유지하되 세부 정보는 **Template-based synthetic data**로 대체하여 실험합니다. [cite: 183-184]
3. [cite_start]**검증**: 실험 전 `PII Leakage Test`를 수행하여 민감 정보 재현률을 0%로 유지합니다. [cite: 158]

---

## [cite_start]6. 결과 분석 및 보고 양식 [cite: 59-60, 218-220]
* [cite_start]**Executive Summary**: 종합 순위 및 Go/No-Go 판정 결과. [cite: 61, 85, 221-223]
* [cite_start]**Confidence vs Accuracy**: 모델의 확신도와 실제 정답률 간의 캘리브레이션 분석. [cite: 72-74, 233-234]
* [cite_start]**Error Analysis**: 오답 유형(환각, 지시 누락, 계산 오류 등)을 분류하여 개선 로드맵 제안. [cite: 76-77, 237-244]

---
[cite_start]**"Measure everything. Trust nothing anecdotal. Ship what the data proves."** [cite: 91]