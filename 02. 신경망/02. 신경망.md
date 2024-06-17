## Sigmoid
$$y = \frac{1}{1+e^{-x}}$$


## ReLU
$$ y =
  \begin{cases}
    x  & \quad \text{(x > 0)} \\
    0  & \quad \text{(x $\leq$ 0)}
  \end{cases}
$$


## Softmax
$$y_k = \frac{e^{a_k}}{\displaystyle\sum_{i=1}^{n} e^{a_i}}$$
- 출력값의 총합이 1임
- Softmax 함수는 지수 함수를 사용함
- 이는 오버플로의 문제점을 야기함
  - 지수 함수로 인하여 매우 큰 값끼리 나눗셈을 하면 수치가 불안정해짐
- 따라서 분모, 분자에 $C$라는 임의의 정수를 곱해주고 지수 함수로 들어가 $logC$로 바꿔줌으로써 개선
  - $C = max(x)$ </br>
$$y_k = \frac{e^{a_k + C}}{\displaystyle\sum_{i=1}^{n} e^{a_i + C}}$$
