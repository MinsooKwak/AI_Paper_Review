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
 

  
---
<!---
1. Intro까지 살펴봄
--->
### 
