## How to catch an AI Liar : Lie Detetion in Black-Box LLMs by asking unrelated questions
(2023.09.26)

Keyoword : `lie detector` `hallucination` `LLM`

- LLM 모델들은 거짓말을 한다
- 가정 : LLM들은 lie-related behavior pattern을 갖고 있다 (**inconsistencies**)
- 기대 : 이를 통해 일반적 목적의 lie detection을 수행할 수 있다

- 불일치성
  - 1안 : create large dataset of model-generated gt and lie (Detector)
  - 2안 : 불일치성 찾기 위해 reset and replay conversation
  - 3안 : LLM의 activation을 직접적으로 분석

 
- 데이터셋 확보
  - 프롬프트를 통해 lie 할 수 있는 상황을 만들어 데이터셋을 확보


### 전개
**[ 1280개 인스턴스에 대한 Dataset ]**
  - Dataset : WikiData와 같은 소스에서 20,000개 이상의 질문과 해당 답변 목록 작성 / 말도 안되는 질문 포함 
  - 거짓말 유도 프롬프트(CoT) + yes/no 답
    ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/9994a74f-1bc1-4624-b798-26ee67d2ae47)


### Simple Lie Detector 

**[ lie detector generalised ]**
  - lie detector가 일반화되었음
    ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/efce26f1-e8e5-4ff7-9f7d-b6140d471ab4)

**[ blackbox lie detector ]**
  - 예/아니오 답변을 통해 진실성 또는 거짓에 대한 점수를 매기게 됨
    ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/eb7ab926-e70e-416e-a05c-8dc7b76921b8)

### 실험
- H0 : 거짓말 한 뒹 더 많은 거짓말 할 것
- 실험 : 48개 질문, 3개 카테고리
  - lie-related (n=24)
  - factual (n=10)
  - ambiguous (n=14)

- Test
  - train : test = 70 : 30
  - 추가적으로 작은 train set에도 잘 작동함
![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/a7156960-ad03-4499-9605-0e25f51614e4)


### 결과
- 평가 : mean AUC (area under the receiver operating characteristic curve) 
  ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/324f387b-5a78-490b-ae64-6b223fcc8aac)

