# Gradient Descent 基礎筆記

## 一句話總結
> Gradient Descent 是一種「用導數找最低點」的方法，類似你蒙著眼睛，靠著坡度往山谷方向走。

---

##  基本概念

在機器學習中，我們的目標是「最小化成本函數 (Loss Function)」，例如：

$$
J(\theta) = \text{損失函數}(\theta)
$$

Gradient Descent 會幫我們找到讓 $J(\theta)$ 最小的參數 $\theta$。

---

##  更新公式

> 每次參數更新，都是往「梯度的反方向」走一步：

$$
\theta := \theta - \eta \cdot \nabla J(\theta)
$$

- $\theta$：參數（weights / biases）
- $\eta$：學習率（learning rate）
- $\nabla J(\theta)$：成本函數對 $\theta$ 的梯度（即導數）

---

##  視覺化圖（建議插圖位置）

建議附圖：
- 一個 U 型曲線，人在坡上，箭頭往下（方向＝負梯度）
- 每一步越來越接近底部

> 可參考圖：[Gradient Descent 圖解（Wiki）](https://upload.wikimedia.org/wikipedia/commons/1/1b/Gradient_descent.svg)

---

##  為什麼學習率很重要？

| 學習率（η） | 結果             |
|-------------|------------------|
| 太小        | 收斂太慢         |
| 太大        | 跳來跳去、甚至發散 |

---

##  常見問題 Q&A

### Q1: 為什麼要走「負的梯度方向」？
因為梯度代表「上坡方向」，要最小化損失，我們就要往反方向走。

---

### Q2: 要算幾次？
通常會跑很多次（稱為迭代 / epochs），直到損失函數夠小，或達到最大次數。

---

### Q3: 為什麼叫 descent？
Descent = 下降；因為我們是在「下降成本函數」的值。

---

##  延伸變體（簡介）

| 方法            | 特點 |
|----------------|------|
| **Batch GD**     | 每次用整筆資料更新參數 |
| **Stochastic GD (SGD)** | 每次只用一筆資料更新 |
| **Mini-batch GD** | 每次用小部分資料（最常見）|

---

##  小結

Gradient Descent 是深度學習的核心演算法之一，它提供了一種數學方法，幫助我們一步步調整模型參數，最終得到預測準確度高的模型。

---
