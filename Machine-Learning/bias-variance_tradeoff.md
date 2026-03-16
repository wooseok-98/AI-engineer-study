# 🖥 Bias-Variance Tradeoff
지도학습 모델에서 **오류를 최소화**하기 위해 **편향(Bias)과 분산(Variance) 사이의 균형**을 맞추는 현상

---
## Bias (편향)
모델이 너무 **단순**하여 데이터의 **실제 패턴을 학습하지 못하는** 정도

### 특징
- 모델이 너무 단순함
- 데이터 패턴을 충분히 학습하지 못함
- Underfitting
- 예시: 복잡한 비선형 데이터에 대해 **선형 회귀 모델**을 사용하는 경우
---

## Variance (분산)
모델이 너무 **복잡**하여 **데이터가 조금만 바뀌어도 모델 결과가 크게 변하는** 정도

### 특징
- 모델이 너무 복잡함
- 훈련 데이터에 지나치게 맞춤
- Overfiiting
- 예시: 깊이가 **너무 깊은 Decision Tree**

---

## Bias-Variance Tradeoff
Bias와 Variance는 서로 **Tradeoff 관계**에 있다.
- 모델이 단순하면 → **Bias 증가 / Variance 감소**
- 모델이 복잡하면 → **Bias 감소 / Variance 증가**

![Alt text](https://images.velog.io/images/cleansky/post/ae6b13fb-03e4-41ea-abf3-ddc77c328498/image.png)

---
## 💡 핵심 정리
| 특징 | Bias | Variance | 상태 |
|---|---|---|---|
| 모델이 너무 단순 | 높음 | 낮음 | Underfitting |
| 데이터에 과적합 | 낮음 | 높음 | Overfitting |

--- 
# 📝 면접 예상 질문
<details>
  <summary>Q. Bias와 Variance의 차이는 무엇인가요?</summary>

Bias는 모델이 너무 단순해서 데이터의 실제 패턴을 제대로 학습하지 못할 때 발생하는 오차입니다.  
Variance는 학습 데이터가 조금만 바뀌어도 모델의 결과가 크게 변하는 정도를 의미합니다.  
Bias는 보통 underfitting과 연결되고, variance는 overfitting과 연결됩니다.

</details>

<details>
  <summary>Q. Bias-Variance Tradeoff란 무엇인가요?</summary>

Bias-Variance Tradeoff는 모델의 복잡도에 따라 bias와 variance가 서로 반대 방향으로 변하는 관계를 의미합니다.  
모델이 단순하면 bias는 커지고 variance는 작아지며, 모델이 복잡하면 bias는 작아지고 variance는 커집니다.  
좋은 모델은 이 두 요소의 균형을 잘 맞춘 모델입니다.

</details>

<details>
  <summary>Q. Overfitting과 Underfitting은 Bias와 Variance와 어떤 관계가 있나요?</summary>

Underfitting은 모델이 너무 단순하여 데이터 패턴을 학습하지 못하는 상태로 높은 bias를 가지는 경우가 많습니다.  
Overfitting은 모델이 훈련 데이터에 과도하게 맞춰져 새로운 데이터에 대한 일반화 성능이 떨어지는 상태로 높은 variance를 가지는 경우가 많습니다.

</details>

<details>
  <summary>Q. Variance를 줄이는 방법에는 어떤 것들이 있나요?</summary>

Variance를 줄이는 방법에는 더 많은 데이터를 사용하는 방법, 모델을 단순하게 만드는 방법, regularization을 적용하는 방법, ensemble 방법을 사용하는 방법 등이 있습니다.

</details>

<details>
  <summary>Q. Bias를 줄이는 방법에는 어떤 것들이 있나요?</summary>

Bias를 줄이기 위해서는 더 복잡한 모델을 사용하거나 더 많은 feature를 사용하고, 충분한 학습을 수행하는 방법이 있습니다.

</details>

<details>
  <summary>Q. Bias-Variance Decomposition 식을 설명해보세요.</summary>

예측 오차는 Bias² + Variance + Irreducible Error로 분해할 수 있습니다.  
Bias²는 모델의 단순성 때문에 발생하는 오차이고, Variance는 데이터 변화에 민감해서 발생하는 오차입니다.  
Irreducible Error는 데이터 자체의 노이즈로 인해 줄일 수 없는 오차입니다.

</details>
