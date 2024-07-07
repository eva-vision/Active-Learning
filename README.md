# Active-Learning
## Methods: 𝜀-greedy, UCB1, UCB-𝛼:. Thompson, Bayesian UCB


Active Learning
Consider a 
𝐾
K-armed bandit machine, where pulling a lever may reward us with some amount of reward. The rewards from each lever are random variables following unknown, independent distributions. Our goal is to pull the levers in sequence to:

Explore the problem space, i.e., estimate the "goodness" of each lever (exploration).
Exploit this knowledge to maximize our total rewards (exploitation).
We recognize that these two goals conflict: to explore, we must pull suboptimal levers, which reduces our total rewards. Due to the probabilistic nature of the levers, a "good" lever might occasionally give a bad reward, so it can be beneficial to test levers that seem bad more than once. This is the exploration vs. exploitation dilemma.

Although our strategies work for various distributions, we will use the well-known Bernoulli distribution. Each lever has an unknown parameter 
𝜃
𝑘
θ 
k
​
 , representing the probability of receiving a reward of 1 unit from that lever. Thus, each pull corresponds to a Bernoulli trial, where 
𝑦
∈
{
0
,
1
}
y∈{0,1} is the reward received after pulling the 
𝑘
k-th lever. Let 
𝑦
‾
𝑘
y
​
  
k
​
  denote the average reward from the 
𝑘
k-th lever, 
𝑛
𝑘
n 
k
​
  denote the number of times the 
𝑘
k-th lever has been pulled, and 
𝑛
n denote the total number of pulls so far.
