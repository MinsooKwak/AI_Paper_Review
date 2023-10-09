## Who's Harry Potter? Approximate unlearning in LLMs
(2023.10.4, microsoft Research, microsoft Azure)

- paper : [link](https://browse.arxiv.org/pdf/2310.02238.pdf)

- contribution :
  - LLM 훈련 이후 별도의 **학습 없이 특정 데이터를 지울 수** 있게 되었다
  - 의도하지 않았지만 관련된 주제에 대한 일반 지식 또한 잊어버리는 것을 확인
  - 미세조정을 통해 조율 가능하다
 
- 활용 모델 : Llama2-7b
- HuggingFace : [microsoft/Llama2-7b-WhoIsHarryPotter](https://huggingface.co/microsoft/Llama2-7b-WhoIsHarryPotter)

---

### Summary
저작권, 편향성 등의 이유로 학습된 데이터에서 특정 데이터들을 배제해야 하는 경우가 있다. <br>
2023년 10월 Microsoft에서 발표한 "Who's Harry Potter? Approximate unlearning in LLMs" 논문에서는 별도의 학습 없이 특정 학습 요소를 지우는 시도를 한다.
Fine Tuning시 하나의 GPU로 1시간 정도만 투자하면 원하는 대상에 대한 제거가 가능하다.
Llama2-7b 모델을 활용하였고, 실험을 통해 잊어야 하는 대상을 제외하고는 성능이 일관되게 유지되는 것을 확인하였다. <br><br>


### Finetuned Llama-7b 결과
- Prompt를 주었을 때 기존 Llama의 경우 Harry Potter와 연관된 이야기를 결과값으로 반환한다.
- 기존 LLM들의 고유한 특성으로 허구적인 실체에 대한 질문을 받았을 때 응답을 생성하고 있지만 <br>
  Finetuned한 실험에서 Harry Potter에 대한 Prompt를 던졌을 때 관련 기억이 없어진 것을 확인할 수 있다. <br>
  ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/dea7919a-00f3-4ba2-b05f-783c6abaedfb) <br><br>

### 일반 성능 유지
- Harry Potter에 대해서는 잊지만 일반 Benchmark에서의 성능은 일관되게 유지되고 있다.
  ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/5f7b0461-ec0a-45ca-95ab-861261b665b4)

---
