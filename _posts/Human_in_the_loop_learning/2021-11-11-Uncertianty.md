# Human In The Loop Learning



## 1. Introduction

A working flow of Human-In-The-Loop Learning

![](https://img-blog.csdnimg.cn/20181226162945108)

The learning model itself returns annotator a series of unlabeled data which seems "hard" to distinguish. The annotator then give these data right label to train again, making the model more accurate.

And, obviously human-in-the-loop learning is also a practical and convenient way to annotate dataset, because model can help annotators do lots of work.

The key step of human-in-the-loop learning is returning uncertain data near **decision boundary** to annotator. Then here come some questions: **How to describe the uncertainty?** or more professionally speaking, **What's the proper algorithm for Uncertainty Sampling?**

![](https://gitee.com/solarwindrider/SolarWindRider/raw/main/_posts/Human_in_the_loop_learning/uncertainty_sampling.png)



## 2. Uncertainty Sampling

According to this book, there are 4 kinds of method for uncertainty sampling:

*Least Confidence Sampling*

*Margin of Confidence Sampling*

*Ratio of Confidence Sampling*

*Entropy-based Sampling*

Different tasks, models need different sampling method.

### 2.1. Least Confidence Sampling

$$
\phi_{LC}(x) = P_\theta(y^*|x)
$$


$$
\phi_{LC}(x) = (1-P_\theta(y^*|x))\times\frac{n}{n-1}
$$
Larger the uncertainty, the score closer to 1.

n mean the number of labels.

x is the item.

y* the highest softmax label.



### 2.2. Margin of Confidence Sampling

$$
\phi_{MC}(x) = P_\theta(y_1^*|x) - P_\theta(y_2^*|x)
$$

$$
\phi_{MC}(x) = 1 - (P_\theta(y_1^*|x) - P_\theta(y_2^*|x))
$$

y1*  is the highest softmax label.

y2* is the second highest softmax label.



### 2.3. Ratio of Confidence Sampling

$$
\phi_{RC}(x) = P_\theta(y_1^*|x)/P_\theta(y_2^*|x)
$$

$$
\phi_{RC}(x) = P_\theta(y_2^*|x)/P_\theta(y_1^*|x)
$$

### 2.4. Entropy Based Sampling

$$
\phi_{ENT}(x) = -\sum_yP_\theta(y|x)log_2P_\theta(y|x)
$$

$$
\phi_{ENT}(x) = \frac{-\sum_yP_\theta(y|x)log_2P_\theta(y|x)}{log_2(n)}
$$

