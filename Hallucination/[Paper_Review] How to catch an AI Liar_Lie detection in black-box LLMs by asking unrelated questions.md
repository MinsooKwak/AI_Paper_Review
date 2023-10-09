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
  
---
<!---
2번까지 리딩 / p4부터 봐야 함
--->
### Simple Lie Detector 
- black box lie detector를 만들고 고정되게 yes/no로 대답하는 "elicitation question" 적용 <br>
  : LLM의 activation 비허용

  **[ lie detector generalised ]**
  ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/efce26f1-e8e5-4ff7-9f7d-b6140d471ab4)

