# project-fm-eval 🧪
> **Personal Research on Foundation Model Evaluation**
> 본 프로젝트는 개인적인 연구 목적으로 최신 LLM의 성능을 평가하고 분석하는 실험 공간입니다. 
> 다만, 실험의 설계와 지표 측정은 **엔터프라이즈급 파운데이션 모델 평가 기준(HELM, G-Eval 등)**을 엄격히 준수하여 진행되므로, 실제 기업용 LLM 도입 시 기술적 레퍼런스로 활용 가능합니다.

---

## 🌟 Project Purpose
1. [cite_start]**Personal Mastery**: 파운데이션 모델 평가 방법론(HELM, Prometheus)의 실제 구현 및 숙달[cite: 95, 97].
2. [cite_start]**Professional Reference**: 기업 환경에서 요구되는 '신뢰성 임계값'을 적용한 객관적 벤치마크 데이터 생성[cite: 7].
3. [cite_start]**Comparative Analysis**: Solar Pro 2와 글로벌 SOTA 모델(GPT-4o) 간의 실무 도메인 성능 비교[cite: 19, 63].

---

## 📈 Evaluation Architecture (Enterprise Standards)
본 실험은 개인 프로젝트임에도 불구하고 기업용 도입 시 즉시 참고할 수 있는 수준의 전문 평가 체계를 갖추고 있습니다.

### 1. 다차원 정량 지표 (Quantitative Metrics)
- [cite_start]**Quality**: Exact Match, F1-Score, ROUGE-L을 통한 도메인(금융/법률/의료) 성능 측정[cite: 25, 123].
- [cite_start]**Trust**: HaluEval 기반 환각율 측정 및 TruthfulQA를 통한 진실성 검증[cite: 27, 136, 137].
- [cite_start]**Safety**: OWASP LLM Top 10 기준 프롬프트 인젝션 저항성 테스트[cite: 106, 157].

### 2. 평가 방법론 (Methodologies)
- [cite_start]**HELM (Holistic Evaluation)**: 시나리오별 다차원 메트릭 평가 철학 적용[cite: 95, 119].
- [cite_start]**LLM-as-a-Judge**: GPT-4o를 Judge 모델로 활용한 **G-Eval** 및 **Prometheus-2** 기반 정성 지표의 수치화[cite: 51, 97].

---

## 🏗 Experiment Setup
- [cite_start]**Baseline Models**: Solar Pro 2, GPT-4o, Claude 3.5 Sonnet, HyperCLOVA X[cite: 19].
- [cite_start]**Custom Dataset**: 금융·법률·의료 도메인별 각 500문항의 SME(전문가) 검수 기반 Golden Dataset 구축 전략 채택[cite: 34, 36, 38].
- **Tools**: `Promptfoo`를 통한 벤치마크 자동화 및 `Claude Code` 기반의 실험 프로세스 제어.

---

## 📄 How to Use as a Reference
본 리포지토리의 실험 결과는 다음과 같은 비즈니스 의사결정에 참고될 수 있습니다.
- [cite_start]특정 도메인(금융/법률 등)에서의 모델별 **Performance-Latency Trade-off** 곡선 확인[cite: 8, 78].
- [cite_start]성능 향상 대비 비용 효율성(**Cost-Efficiency Index**) 산출 근거[cite: 29, 227].
- [cite_start]기업 보안 정책 수립을 위한 **Safety & Security** 리스크 지표[cite: 82, 155].

---

## 👤 Contact
- **Researcher**: [곽승연 / devfyoo2829-lab]
- **Email**: fyoo2829@gmail.com