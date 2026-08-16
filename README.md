# Hugging Face를 활용한 금융 업무 문의 자동 분류

## 1. 프로젝트 소개

Hugging Face의 사전학습 언어 모델을 활용하여 금융 업무 관련 문의를
업무 유형별로 분류하는 미니 프로젝트입니다.

별도의 모델 학습 없이 Zero-shot Classification을 적용하여,
사용자가 입력한 금융 문의를 미리 정의한 업무 유형과 비교하고
가장 적합한 업무 유형을 예측하도록 구현했습니다.

### 프로젝트 목적

- Hugging Face Hub의 사전학습 모델 활용 경험
- Transformers `pipeline()` 사용
- Zero-shot Classification 이해
- 자연어 입력을 실제 업무 분류 문제에 적용
- 모델의 예측 결과와 한계 분석

---

## 2. 사용 기술

- Python 3.12
- Hugging Face Transformers
- Hugging Face Zero-shot Classification
- PyTorch 기반 사전학습 모델
- Pandas
- Google Colab

사용 모델:

`MoritzLaurer/mDeBERTa-v3-base-mnli-xnli`

다국어 자연어 추론(NLI) 기반 모델을 Zero-shot Classification에 활용했습니다.

---

## 3. 문제 정의

금융 업무에서는 고객 문의의 내용을 파악하여
담당 업무나 문의 유형을 분류하는 과정이 필요합니다.

예를 들어:

```text
"해외 송금 수수료가 궁금합니다."
              ↓
            송금
