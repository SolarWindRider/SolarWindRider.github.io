# Sigmoid & SoftMax

Sigmoid and Softmax are both probability related functions. They produce results between 0 and 1. However, the are not the same. In this note, I learn further about their differences.

## 1. Formula

As for binary classification, let's define input as $x_1$:
$$
Sigmoid(x_1) = \frac{e^{x_1}}{1+e^{x_1}} = \frac{1}{1+e^{-x_1}}  \qquad (1)
$$

$$
SoftMax(x_1) = \frac{e^{x_1}}{e^{x_1}+e^{x_2}} = \frac{1}{1+e^{-(x_1-x_2)}} \qquad (2) \\
SoftMax(x_2) = \frac{e^{x_2}}{e^{x_1}+e^{x_2}} = \frac{1}{1+e^{x_1-x_2}} \qquad (3)
$$


As for multi-classification, we get:
$$
Sigmoid(x_1) = \frac{e^{x_i}}{1+e^{x_i}} = \frac{1}{1+e^{-x_i}}  \qquad (4)
$$
 
$$
SoftMax(x_i) = \frac{e^{x_i}}{\displaystyle\sum\limits_{j=0}^n{e^{x_j}}} \qquad (5)
$$




Seems that sigmoid always takes an $x$ as 0 .

Second, the sum of Sigmoid only in binary classification equals 1, but sum of Softmax is always equal to 1 .