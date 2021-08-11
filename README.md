# Papers-of-Offline-RL

Related papers for offline reforcement learning (we mainly focus on representation and sequence modeling and conventional offline RL)

# Statement

Anyone is welcomed to submit a pull request for the related and unlisted papers on offline RL, which are published on peer-review conferences (ICML/NeurIPS/ICLR/CVPR etc.) or released on arXiv.



## Contents
- <a href="#Representation Learning">Representation Learning (for RL) </a><br>
- <a href="#Sequence Modeling">Sequence Modeling </a><br>
- <a href="#Conventional Offline-Reinforcement-Learning">Conventional Offline-Reinforcement-Learning </a><br>

<a id='Representation Learning'></a>
## Representation Learning (for RL)

- [Provable Representation Learning for Imitation with Contrastive Fourier Features](https://arxiv.org/pdf/2105.12272.pdf)  

  **提出用contrastive learning**方法从offline dataset表征state，可以证明在使用该方法优化表征state的函数和强化学习过程时，等价于将学习的policy与收集offline dataset的target policy的距离的upper bound降低，不需要考虑target policy表征的形式，理论上可以将error降到0。相较Behavior Cloning方法（Bisimulation-based）性能大幅提升，实验在tabular case和Atari2600上训练的DQN均做了实验。（learning dynamic and reward）BC对target policy采集数据的形式有限制，且由于数据未全覆盖且空间大sample efficiency比较低  
  
- [Pretraining Representations for Data-Efficient
Reinforcement Learning](https://arxiv.org/pdf/2106.04799.pdf)  

- [Representation Matters: Offline Pretraining for Sequential Decision Making](https://arxiv.org/pdf/2102.05815.pdf)  


<a id='Sequence Modeling'></a>
## Sequence Modeling

- [Reinforcement Learning as One Big Sequence Modeling Problem](https://arxiv.org/pdf/2106.02039.pdf)
- [Decision Transformer: Reinforcement Learning via Sequence Modeling](https://arxiv.org/pdf/2106.01345.pdf)[[code]](https://github.com/kzl/decision-transformer)

<a id='Conventional Offline-Reinforcement-Learning'></a>
## Conventional Offline-Reinforcement-Learning

- [Conservative Q-Learning for Offline Reinforcement Learning](https://arxiv.org/pdf/2006.04779.pdf) [[code]](https://github.com/aviralkumar2907/CQL)   

  **CQL**：提出在offline-rl中Q learning过程中加入正则项来缓解over-estimate的问题。通过正则项可以学习到真实Q的lower bound，这样扩大估计值和真实值Q的距离，缓解offline RL中存在的distribution shift问题
- [Off-policy deep reinforcement learning without exploration](http://proceedings.mlr.press/v97/fujimoto19a/fujimoto19a.pdf)  

  **BCQ**: constrains the mismatch between the state-action visitation of the policy and the state-action pairs contained in the batch by using a state-conditioned generative model to produce only previously seen actions.
- [D4RL: Datasets for Deep Data-Driven Reinforcement Learning](https://arxiv.org/pdf/2004.07219.pdf)) [[code]](https://github.com/rail-berkeley/d4rl)  
- [Stabilizing Off-Policy Q-Learning via Bootstrapping Error Reduction](https://arxiv.org/pdf/1906.00949.pdf) [[code]](https://github.com/aviralkumar2907/BEAR)  

  **BEAR**：为环境offline RL设定中从静态数据集中学习存在的数据偏移问题，提出在Bellman方程迭代更新Q过程中，由于action distribution shift导致的累积误差越来越大可能会导致最终不收敛的现象。文章提出了如何限制动作的选择来减轻此问题，提出算法bootstrapping error accumulation reduction (BEAR)，借助support-set matching来避免此问题  
  
- [Offline Decentralized Multi-Agent Reinforcement Learning](https://arxiv.org/pdf/2108.01832.pdf)  

  **MABCQ**: 通过对conditional VAE模型的隐向量的约束，实现对Q learning网络从offline学习到online的约束，方法在MA-Mujoco上验证  
  
- [Believe What You See: Implicit Constraint Approach for Offline Multi-Agent Reinforcement Learning](https://arxiv.org/pdf/2106.03400.pdf)  

  **ICQ**: 本质上依然是对Q-network做约束，加上mixing网络为ICQ-Ma作为offline MARL的方法  
  
- [Boosting Offline Reinforcement Learning with Residual Generative Modeling](https://arxiv.org/pdf/2106.10411.pdf)  

  同样使用conditional VAE来约束offline learning过程中学到的policy  
  
- [Behavior Constraining in Weight Space for Offline Reinforcement Learning](https://arxiv.org/pdf/2107.05479.pdf)  

- [Offline Reinforcement Learning with Fisher Divergence Critic Regularization](https://arxiv.org/pdf/2103.08050.pdf)  

- [Offline Meta-Reinforcement Learning with Online Self-Supervision](https://arxiv.org/pdf/2107.03974.pdf)  

- [Offline-to-Online Reinforcement Learning via Balanced Replay and Pessimistic Q-Ensemble](https://arxiv.org/pdf/2107.00591.pdf)  

- [Policy Finetuning: Bridging Sample-Efficient Offline and Online Reinforcement Learning](https://arxiv.org/pdf/2106.04895.pdf)

- [S4RL: Surprisingly Simple Self-Supervision for Offline Reinforcement Learning in Robotics](https://arxiv.org/pdf/2103.06326.pdf)