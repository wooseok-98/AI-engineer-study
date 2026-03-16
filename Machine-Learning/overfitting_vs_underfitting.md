# 🖥 Overfitting vs Underfitting
---
## Overfitting
모델이 훈련 **데이터에 지나치게 맞춰져 학습된** 상태
- 모델이 데이터의 실제 패턴뿐만 아니라 **노이즈까지 학습**
- 훈련 데이터에서는 높은 성능 보이지만, **새로운 데이터에서는 성능 떨어짐**

---
### 특징
- Training error: 낮음
- Test error: 높음
- 모델이 너무 복잡함
- 데이터 변화에 민감하게 반응
- 예시:
    - 너무 깊은 Decision Tree
    - 적은 데이터를 학습한 복잡한 모델
---
## Underfitting
모델이 **데이터의 패턴을 충분히 학습하지 못한** 상태
- 모델이 너무 단순하여 **데이터 관계 제대로 표현 못함**
- **훈련, 테스트 데이터 모두**에서 성능 떨어짐
---
### 특징
- Training error: 높음
- Test error: 높음
- 모델이 너무 단순함
- 예시:
    - 복잡한 데이터를 Linear Regression으로 학습한 경우
---
## Bias-Variance와의 관계

Overfitting과 Underfitting은 Bias와 Variance와 밀접한 관계가 있다.

| 상태 | Bias | Variance |
|---|---|---|
| Underfitting | 높음 | 낮음 |
| Overfitting | 낮음 | 높음 |

---
## Overfitting의 원인

Overfitting은 다음과 같은 이유로 발생할 수 있다.

- 모델이 너무 복잡함
- 데이터가 부족함
- Feature 수가 너무 많음
- 데이터에 노이즈가 많음

---

## Curse of Dimensionality (차원의 저주)

Feature의 차원이 증가하면 **차원의 저주(Curse of Dimensionality)** 문제가 발생할 수 있다.

차원이 증가할수록 데이터 공간이 기하급수적으로 커지기 때문에  
데이터가 **희소(sparse)** 해지고 모델이 일반화하기 어려워진다.

이로 인해 모델이 데이터의 패턴보다는 **훈련 데이터에 과적합(overfitting)** 되는 문제가 발생할 수 있다.

예를 들어

- feature 수 증가
- 데이터 밀도 감소
- 모델 variance 증가

결과적으로 **Overfitting 가능성이 높아진다.**

---

## Overfitting 방지법

Overfitting을 방지하는 방법에는 여러 가지가 있다.

### 1. More Data

더 많은 데이터를 사용하면 모델이 데이터의 일반적인 패턴을 학습할 가능성이 높아진다.

### 2. Regularization

모델의 복잡도를 제한하여 과적합을 방지한다.

예

- L1 Regularization
- L2 Regularization

### 3. Feature Selection

불필요한 feature를 제거하여 모델의 복잡도를 줄인다.

### 4. Cross Validation

모델의 일반화 성능을 평가하기 위해 데이터를 여러 번 나누어 학습한다.

### 5. Early Stopping

모델이 과도하게 학습되기 전에 학습을 중단한다.

---
## 💡 핵심 정리
- **Overfitting**은 모델이 훈련 데이터에 과도하게 맞춰진 상태이다.
- **Underfitting**은 모델이 데이터 패턴을 충분히 학습하지 못한 상태이다.
- Overfitting은 **High Variance**, Underfitting은 **High Bias**와 관련이 있다.
- Feature 차원이 증가하면 **Curse of Dimensionality**로 인해 Overfitting이 발생할 수 있다.

---
# 📝 면접 예상 질문
<details>
  <summary>Q. Overfitting과 Underfitting의 차이는 무엇인가요?</summary>

Overfitting은 모델이 훈련 데이터에 과도하게 맞춰져 새로운 데이터에 대한 성능이 떨어지는 상태입니다.  
반면 Underfitting은 모델이 너무 단순하여 데이터의 패턴을 충분히 학습하지 못한 상태입니다.

</details>

<details>
  <summary>Q. Overfitting은 왜 발생하나요?</summary>

Overfitting은 모델이 너무 복잡하거나 데이터가 부족하거나 feature 수가 너무 많은 경우 발생할 수 있습니다.  
이 경우 모델이 데이터의 실제 패턴뿐 아니라 노이즈까지 학습하게 됩니다.

</details>

<details>
  <summary>Q. Overfitting을 해결하는 방법에는 무엇이 있나요?</summary>

Overfitting을 해결하기 위해서는 더 많은 데이터를 사용하거나, Regularization을 적용하거나, Feature Selection을 수행할 수 있습니다.  
또한 Cross Validation이나 Early Stopping 같은 방법도 사용할 수 있습니다.

</details>

<details>
  <summary>Q. Curse of Dimensionality란 무엇인가요?</summary>

차원의 저주는 feature의 차원이 증가할수록 데이터 공간이 급격히 커져 데이터가 희소해지는 현상을 의미합니다.  
이로 인해 모델이 일반화하기 어려워지고 Overfitting이 발생할 가능성이 높아집니다.

</details>

<details>
  <summary>Q. Training Error와 Test Error는 Overfitting에서 어떻게 나타나나요?</summary>

Overfitting이 발생하면 Training Error는 매우 낮지만 Test Error는 높게 나타납니다.  
이는 모델이 훈련 데이터에만 맞춰 학습되었기 때문입니다.

</details>
