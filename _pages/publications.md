---
layout: archive
title: "Research"
permalink: /publications/
author_profile: false
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

I am a researcher working at the intersection of **digital finance**, **mathematical modeling**, and **AI**. My work combines rigorous mathematical tools with modern machine learning to understand and improve how digital financial markets are designed and operated. I am particularly focused on decentralized exchanges and prediction markets — building models that are both theoretically grounded and practically deployable.



## Current Research Areas

My research sits at the intersection of financial markets, machine learning, and game theory. The central question is: **can we replace hand-crafted rules and assumptions in market design with systems that learn directly from data?**

This work spans two connected areas:
 
1. **Automated Market Makers (AMMs)** — redesigning decentralized exchange protocols so that everyday liquidity providers are better protected against sophisticated traders who exploit them.
2. **Prediction Markets & High-Frequency Dynamics** — building learning systems that extract actionable signals directly from raw market data, without relying on hand-engineered features.
Both pillars share a common foundation in self-supervised representation learning (systems that learn structure from data without human-labeled examples).

---

### Pillar 1: Automated Market Makers (AMMs)
 
**The problem:** In most decentralized exchanges today, passive liquidity providers (LPs) — the people who fund trading pools — quietly lose money to informed traders who exploit price gaps between the pool and the broader market. This is called *Loss-Versus-Rebalancing (LVR)*. The projects below attack this problem from different angles.
 
**Quick catch-up:** [AMM challenge](https://www.optimizationarena.com/amm) · [Prop AMM challenge](https://www.optimizationarena.com/prop-amm)

---
 
#### 1. Multi-AMM Simulation in JAX
 
**Motivation:** Testing market design ideas requires fast, flexible simulation across many market conditions.
 
**Goal/Scope:** Build a high-speed simulator that models how traders route orders across competing AMMs and how arbitrageurs close price gaps. The simulator is fully compiled for speed and supports direct training of reinforcement learning agents for fee-setting and pool design experiments.
 
---
 
#### 2. Single-Period LP Pricing (Glosten–Milgrom Framework)
 
**Motivation:** How should a liquidity provider set bid/ask prices when they don't know whether the next trader is informed or not?
 
**Goal/Scope:** Adapt a classical market microstructure model to a proprietary AMM setting. We solve for the LP's optimal price distribution given a mix of informed and uninformed traders. Early results show a sharp threshold effect: as the fraction of informed traders crosses a critical level, the LP's optimal response shifts abruptly from tight quotes to defensive wide spreads.
 
---
 
#### 3. N-Player LP Competition
 
**Motivation:** Real pools have multiple competing LPs, each trying to capture retail flow while avoiding toxic order flow.
 
**Goal/Scope:** Model the strategic interaction among N competing LPs who each set prices independently. We characterize the Nash equilibrium — the stable outcome where no LP can unilaterally improve their position. A key finding: in equilibrium, LPs must spread liquidity continuously (no concentration at single prices), and as N grows, profit margins are competed away toward zero.
 
---
 
#### 4. Stackelberg Arbitrage Game
 
**Motivation:** How does a pool operator set prices dynamically when arbitrageurs will immediately respond to any mispricing?
 
**Goal/Scope:** Model the interaction as a two-level game: the pool operator moves first (setting prices and a dynamic adjustment rule), then a group of arbitrageurs simultaneously compete for profit opportunities. We establish conditions guaranteeing a unique, stable equilibrium for the arbitrageurs' responses.
 
---
 
#### 5. am-AMM Continuous-Time Control
 
**Motivation:** The *auction-managed AMM* (am-AMM) model proposes leasing pool management rights to a single operator who takes on the risk of arbitrage losses in exchange for a fee. How should this operator behave optimally over time?
 
**Goal/Scope:** Extend the discrete am-AMM model to continuous time using stochastic optimal control. The operator simultaneously chooses fees and manages their rental payment to the pool. We derive closed-form solutions for optimal fees and rental policies under different assumptions about how liquidity responds to returns.
 
**Quick catch-up:** [am-AMM original paper](https://link.springer.com/chapter/10.1007/978-3-032-07024-1_6)
 
---
 
#### 6. P&L-Aware Regime Detection (SSRD)
 
**Motivation:** Standard clustering methods (like K-Means) group market states by statistical similarity — but statistical similarity doesn't always map to trading relevance.
 
**Goal/Scope:** Train a neural encoder that groups market states by their *downstream effect on LP profitability*, not just their statistical properties. The model learns soft cluster assignments that minimize LP profit variance within each cluster. Tested on Uniswap v3 ETH/USDC data, it shows meaningful variance reduction compared to standard K-Means.
 
---
 
### Pillar 2: Prediction Markets & High-Frequency Dynamics
 
**The problem:** Hand-crafted features for financial prediction are brittle — they work until market conditions shift. This pillar asks whether we can build systems that learn robust representations directly from raw data, bypassing feature engineering entirely.
 
**Quick catch-up:** [Prediction market challenge overview](https://www.optimizationarena.com/prediction-market-challenge)
 
---
 
#### 1. Short-Term Binary Options via JEPA & World Models
 
**Motivation:** Reconstructing raw market data (predicting exact prices tick-by-tick) wastes model capacity on noise. We only care about the information relevant to near-term outcomes.
 
**Goal/Scope:** Apply Yann LeCun's Joint-Embedding Predictive Architecture (JEPA) to short-duration (5–15 min) binary option markets on Polymarket. Rather than predicting raw prices, the model learns compact latent representations of limit order book states. A planning module then simulates potential quoting strategies in this latent space and selects actions that best balance fill probability against adverse selection risk.
 
**Quick catch-up:** [JEPA deep dive (blog)](https://rohitbandaru.github.io/blog/JEPA-Deep-Dive/)

---
 
#### 2. Sports Betting Markets via Temporal GNNs
 
**Motivation:** Sports prediction markets on platforms like Polymarket span many proposition types (match winner, map duration, in-game objectives). Isolated team statistics miss cross-regional competitive context and non-stationary performance over time.
 
**Goal/Scope:** Build a graph neural network that treats historical match results as a global graph, routing information across international competitions to calibrate relative team strength. A temporal component tracks how team form evolves over time, with a mechanism to widen uncertainty estimates at season boundaries when rosters change. A multi-output head produces calibrated predictions across different proposition types from a shared backbone.
 
**Quick catch-up:**  [TacticAI: AI assistant for football tactics (DeepMind)](https://deepmind.google/blog/tacticai-ai-assistant-for-football-tactics/)

---

## Publications

### DeFi & Mathematical Finance
* Tung, S. N., & Wang, T. H. (2024). A mathematical framework for modelling CLMM dynamics in continuous time. *arXiv preprint arXiv:2412.18580.* (Accepted for publication in Digital Finance)
* Lee, C. Y., Tung, S.-N., & Wang, T.-H. (2026). Growth rate of liquidity provider’s wealth in G3Ms. *Applied Mathematical Finance*, 32(6), 379–422. https://doi.org/10.1080/1350486X.2026.2662662
* A. Christian Silva, Shen-Ning Tung, Wei-Ru Chen. Stylized facts in Web3. *Frontiers of Mathematical Finance*, 2024, 3(4): 572-609. doi: 10.3934/fmf.2024021
* Joseph Najnudel, Shen-Ning Tung, Kazutoshi Yamazaki, Ju-Yi Yen. An arbitrage driven price dynamics of Automated Market Makers in the presence of fees. Frontiers of Mathematical Finance, 2024, 3(4): 560-571. doi: 10.3934/fmf.2024018

### Number Theory
* Tung, SN. On the automorphy of 2-dimensional potentially semistable deformation rings of $G_{\mathbb{Q}_p}$. *Algebra & Number Theory*, 15(9), 2173–2194 (2021). doi: 10.2140/ant.2021.15.2173 
* Tung, SN. **On the modularity of 2-adic potentially semi-stable deformation rings.** *Math. Z.* 298, 107–159 (2021). https://doi.org/10.1007/s00209-020-02588-4
* Paškūnas V, Tung S-N. Finiteness properties of the category of mod p representations of $\textrm{GL}_2 (\mathbb{Q}_p)$. *Forum of Mathematics, Sigma.* 2021;9:e80. doi:10.1017/fms.2021.72


## Preprints
* Risk, J., Tung, S. N., & Wang, T. H. (2025). Dynamics of liquidity surfaces in Uniswap v3. *arXiv preprint arXiv:2509.05013.* (Submitted)
* Risk, J., Tung, S. N., & Wang, T. H. (2026). Pricing and hedging for liquidity provision in Constant Function Market Making. *arXiv preprint arXiv:2603.01344.* (Submitted)