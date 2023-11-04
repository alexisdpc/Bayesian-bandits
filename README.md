# Bayesian bandits

We implement a Bayesian Reinforcement Learning algorithm. Suppose you are at the casino and in some of bandits (slot machines) there is a higher probability of winning. We aim to find the bandit in which we are more likely to win. For example, take four bandits that have $p=[0.2, \, 0.4, \, 0.6, \, 0.8]$ as winning probabilities.

The aim is to find the winning rate of each bandit. We can use Bayes theorem and aim to find the posterior probability

$$ p(\theta |X) = \frac{p(X|\theta) \, p(\theta)}{p(X)}, $$

where $X$ is the data collected and we aim to find the parameter $\theta$. If the prior is a Beta distribution and the likelihood is  Binomial then it can be shown that the posterior will also be a Beta distribution. Therefore, the Beta distribution is the conjugate distribution of the Binomial distribution

$$ p(\theta)  = {\rm Beta}(\alpha, \beta) $$

$$ \implies p(\theta |X)   = {\rm Beta}\left(\alpha + \sum_{i=1}^N x_i , \, \beta +N - \sum_{i=1}^N x_i\right). $$

The number of wins are added to the parameter $\alpha$ while the number of losses are added to $\beta$.

![image](https://github.com/alexisdpc/Bayesian_bandits/assets/124795834/065d831b-879e-414d-97a9-0cd0af840777)
![image](https://github.com/alexisdpc/Bayesian_bandits/assets/124795834/7e162af9-f843-4ff6-b4f3-c9d9aa4b3eaf)




