# Focal Loss



This is a note for Focal Loss. I need to write it down to remember some details.

Focal Loss come from  CV and is a modification of CrossEntropy Loss. It is designed to solve this problem : unbalanced labels. When training my NER model, I find the dataset I got has extremely unbalanced labels, in which O label occupies  79.04%. Using CrossEntropy loss function directly gets a high accuracy but low f1-score. Because the model always tags O label.

## 1. CrossEntropy Loss

Take *binary classification* for an example, CrossEntropy loss sum all the loss with equal weight. Thus, unbalanced labels impacts the model.
$$
CE(p,y) = \begin{cases}
-log(p) \qquad &y = 1\\
-log(1-p)\qquad &otherwise
\end{cases}
\qquad (1)
$$
Using  $p_t$ represent $p$.
$$
p_t = \begin{cases}
p \qquad &y = 1\\
1-p\qquad &otherwise
\end{cases}
\qquad (2)
$$
Then we can reformat formula (1) as :
$$
CE(p,y) = CE(p_t) = -log(p_t) \qquad (3)
$$

## 2. Focal Loss

Since, CrossEntropy Loss gives all the class equal weight, it seems a solution to set different weight for each class. we get:
$$
FL(p_t) = -\alpha_tlog(p_t) \qquad (4)
$$
Formula (4) can control the weight of classes, but cannot control the weight of easy-classify class and hard-classify class. Then let's make $\alpha_t$  a little more complex by introducing $\gamma$ .
$$
FL(p_t) = -(1-p_t)^\gamma log(p_t) \qquad (5)
$$
Formula (5) is binary Focal Loss exactly, And $\gamma$ is called focusing parameter, $\gamma \ge 0$ , $(1-p_t)^\gamma$ is called modeling factor. It is obvious that when $\gamma = 0$ ,formula (5) become formula (3)

And then, focusing parameter make model focus on  hard-classy labels by decrease the weight of easy-classify labels. 

In the original paper, the combine formula (4) and formula (5), getting formula (6):
$$
FL(p_t) = -\alpha_t(1-p_t)^\gamma log(p_t) \qquad (6)
$$
Formula (6) can not only control weight of different type of classes but also easy-classify and hard-classify classes. And their experiments shows that when $\gamma = 2 , \alpha_t = 0.25$ , we could get the best model. But be aware the their experiment is CV, not NLP.



## 3. Define Multi-Focal Loss Class using pytorch

formula(6) is binary focal loss,. In my experiment, there are 27 types if labels, thus $\gamma$ and $\alpha_t$ are not single float but tensor of floats. Their shape are the same, (LabelNum, 1) . I'd like to define label as a bottom $i$, then I get:
$$
FL_{total} = \begin{cases}
\displaystyle\sum\limits_{i=0}^{LabelNum} FL_i(p_t) \qquad &averagr = false\\
\frac{1}{LabelNum}\times\displaystyle\sum\limits_{i=0}^{LabelNum} FL_i(p_t)\qquad &average=true
\end{cases}
$$
