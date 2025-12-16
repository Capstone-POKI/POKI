# Capstone-POKI💚

## 🎯 프로젝트 소개

- **프로젝트명**: PitchCoach
- **주제**: 예비·초기 창업자를 위한 멀티모달 AI 기반 IR 피칭 준비 통합 코칭 플랫폼
- **트랙**: 산학
- **기간**: 2025.09 ~ 2026.06
- **지도교수**: 윤명국 교수님

이 저장소는 **Team 20 POKI**가 진행하는 졸업 프로젝트 *PitchCoach*의 전체 소스 코드, 기술 문서, 서비스 기획 자료를 포함합니다. PitchCoach는 투자 유치, 정부 지원 사업, 창업 경진대회 등 다양한 IR 환경에서 **창업자의 피칭 준비 전 과정을 하나의 흐름으로 통합**하여, 보다 전략적이고 전문적인 발표 준비를 돕는 **올인원 AI 코칭 플랫폼**을 목표로 합니다.

---

## 🧩 프로젝트 개요

### 무엇을 만들고자 하는가

PitchCoach는 예비·초기 창업자의 IR 피칭 준비 전 과정

(**공고 분석 → IR Deck 분석 → 리허설(음성) 분석 → AI 리포트 → 수정 가이드 → 예상 Q&A 훈련**)을

단절된 개별 작업이 아닌 **하나의 연속된 워크플로우**로 연결하는 멀티모달 AI 코치입니다.

이를 통해 창업자는

- 1분 엘리베이터 피칭
- 투자 유치 피칭
- 창업 경진대회 발표

등 다양한 상황에 맞춰 **데이터 기반의 반복 훈련과 객관적인 피드백**을 받을 수 있습니다.

---

## 🎯 고객 및 문제 정의

### 고객

- 투자 유치 또는 정부·공공 지원 사업 선발을 준비 중인 **예비·초기 창업자**

### Pain Point

1. **평가 기준의 불확실성**
    - 사업 공고마다 시장성·팀 역량·기술성 등 평가 비중이 상이하여 전략적인 발표 준비가 어려움
2. **훈련 환경의 제약**
    - 시간 관리, 발표 자료 균형, 발화 습관 등을 객관적으로 측정할 수 있는 도구 부족
3. **실전 경험 부족**
    - 실제 투자자·심사위원 앞에서의 발표 및 돌발 질문 대응 경험 부족

---

## 🚀 주요 기능

- **공고·IR Deck 통합 분석**
    - 지원 사업 및 경진대회 공고의 평가 기준 자동 추출
    - IR Deck과 매칭하여 누락·부족 영역 진단 및 시각화
- **음성 분석 기반 리허설 코칭**
    - 발화 속도, 억양, 말버릇 등 전달력 요소 정량 분석
    - 발표 음성과 슬라이드 내용 간 맥락 일치 여부 점검
- **AI 리포트 · Q&A 훈련**
    - 발표 결과 점수화 및 항목별 강·약점 분석
    - 심사 기준을 반영한 예상 질문 자동 생성
    - 투자자 관점의 실전형 Q&A 피드백 제공

---

## 🛠 기술 스택 및 사용 시나리오

### 사용 소프트웨어 패키지 및 용도

1. **OpenAI Whisper**
    - 리허설 발표 음성 업로드 → 텍스트 전사 생성
    - 다국어 음성 인식(ASR) 기반 발표 스크립트 추출
2. **librosa**
    - 전사된 발표 음성 분석
    - 말 빠르기(WPM), 억양, 발음 명료도 등 음향 특징 추출
3. **LLM (Gemini)**
    - 공고문 요약 및 IR Deck 매칭
    - 부족 섹션 강조 및 IR 예상 질문 자동 생성
4. **LLM Fine-tuning**
    - 예상 질문에 대한 답변 평가
    - 답변의 간결성·정확성·논리 구조 분석
5. **LayoutLM**
    - 문서 레이아웃 파싱
    - IR 표준 항목 자동 라벨링 및 구조 분석
6. **LIME / SHAP**
    - AI 리포트 점수 산출 근거 설명
    - 점수에 영향을 준 문장·슬라이드 하이라이트 제공 (Explainable AI)

![image.png](attachment:ea1952f7-dce2-4e48-8fcc-25bf6d300781:image.png)

---

## 🔗 사용 라이브러리 및 공식 URL

- OpenAI Whisper: https://github.com/openai/whisper
- librosa: https://librosa.org/
- LLM (Gemini): https://platform.openai.com/
- HuggingFace Transformers (Fine-tuning): https://huggingface.co/transformers/
- LayoutLM: https://github.com/microsoft/unilm/blob/master/layoutlmv3/README.md
- LIME: https://github.com/marcotcr/lime
- SHAP: https://github.com/shap/shap

---

## 👥 팀원

- **강민경**: 백엔드, AI(Q&A 생성 및 AI 리포트)
- **김예린**: 프론트엔드, AI(음성 분석)
- **장현서**: 백엔드, AI(공고문·IR Deck 분석)

---

## 🤝 팀 그라운드룰

[GroundRule](https://github.com/Capstone-POKI/POKI/blob/main/GroudRuld.MD)

---

## 📜 라이선스

- MIT / Apache 2.0 등 (추후 확정)
