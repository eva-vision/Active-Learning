# Active-Learning
## Methods: Epsylon-Greedy, UCB1, UCB-Alpha:. Thompson, Bayesian UCB



Consider a 
𝐾-armed bandit machine, where pulling a lever may reward us with some amount of reward. The rewards from each lever are random variables following unknown, independent distributions. Our goal is to pull the levers in sequence to:

Explore the problem space, i.e., estimate the "goodness" of each lever (exploration).
Exploit this knowledge to maximize our total rewards (exploitation).
We recognize that these two goals conflict: to explore, we must pull suboptimal levers, which reduces our total rewards. Due to the probabilistic nature of the levers, a "good" lever might occasionally give a bad reward, so it can be beneficial to test levers that seem bad more than once. This is the exploration vs. exploitation dilemma.

Although our strategies work for various distributions, we will use the well-known Bernoulli distribution. Each lever has an unknown parameter 
𝜃𝑘 representing the probability of receiving a reward of 1 unit from that lever. Thus, each pull corresponds to a Bernoulli trial, where 
𝑦∈{0,1} is the reward received after pulling the 𝑘-th lever. Let 𝑦‾𝑘 denote the average reward from the 𝑘-th lever, 𝑛𝑘 denote the number of times the 
𝑘-th lever has been pulled, and 𝑛 denote the total number of pulls so far.
