---
title: "Research"
---

I am a researcher working at the intersection of **digital finance**, **mathematical modeling**, and **AI**. My work combines rigorous mathematical tools with modern machine learning to understand and improve how digital financial markets are designed and operated. The central question is: **can we replace hand-crafted rules and assumptions in market design with systems that learn directly from data?**

This work spans two connected areas, both grounded in representation learning — systems that learn structure from data.

## Automated Market Makers (AMMs)

Redesigning decentralized exchange protocols to better protect passive liquidity providers (LPs) against *Loss-Versus-Rebalancing (LVR)*, the quiet drain caused by informed traders exploiting price gaps. ([AMM challenge](https://www.optimizationarena.com/amm) · [Prop AMM challenge](https://www.optimizationarena.com/prop-amm))

- **Multi-AMM simulation in JAX** — high-speed, fully compiled simulator for RL-based fee and pool design experiments across competing pools.
- **Single-period LP pricing (Glosten–Milgrom)** — optimal price distribution for a LP facing a mix of informed and uninformed traders; reveals a sharp threshold where quotes shift abruptly to defensive wide spreads.
- **N-player LP competition** — Nash equilibrium characterization of competing LPs; in equilibrium, liquidity must be spread continuously and profit margins vanish as N grows.
- **Stackelberg arbitrage game** — two-level game between pool operator and competing arbitrageurs, with conditions guaranteeing a unique stable equilibrium.
- **am-AMM continuous-time control** — stochastic optimal control for auction-managed AMMs; closed-form solutions for optimal fees and rental policies. ([am-AMM original paper](https://link.springer.com/chapter/10.1007/978-3-032-07024-1_6))
- **P&L-aware regime detection (SSRD)** — neural encoder that clusters market states by LP profitability impact rather than statistical similarity.

## Prediction Markets & High-Frequency Dynamics

Building learning systems that extract actionable signals directly from raw market data, bypassing brittle hand-engineered features. ([Prediction market challenge](https://www.optimizationarena.com/prediction-market-challenge))

- **Short-term binary options via JEPA** — world model for 5–15 min Polymarket contracts; learns compact latent representations of limit order book states and plans quoting strategies in latent space rather than predicting raw prices. (LeCun on JEPA and world models: [part I](https://www.youtube.com/watch?v=kYkIdXwW2AE) · [part II](https://www.youtube.com/watch?v=v_jDvpEGTIg))
- **Sports betting via temporal GNNs** — graph neural network over historical match results that routes information across international competitions to calibrate team strength, with uncertainty widening at season boundaries and a shared backbone for multi-proposition prediction.

* * *

## Publications

### DeFi & Mathematical Finance

[Pricing and hedging for liquidity provision in Constant Function Market Making.](https://arxiv.org/abs/2603.01344) Risk, J., Tung, S. N., & Wang, T. H. [arXiv:2603.01344](https://arxiv.org/abs/2603.01344) (submitted).

[Dynamics of liquidity surfaces in Uniswap v3.](https://arxiv.org/abs/2509.05013) Risk, J., Tung, S. N., & Wang, T. H. [arXiv:2509.05013](https://arxiv.org/abs/2509.05013) (submitted).

[A mathematical framework for modelling CLMM dynamics in continuous time.](https://arxiv.org/abs/2412.18580) Tung, S. N., & Wang, T. H. *Digital Finance* (accepted). [arXiv:2412.18580](https://arxiv.org/abs/2412.18580)

[Growth rate of liquidity provider's wealth in G3Ms.](https://doi.org/10.1080/1350486X.2026.2662662) Lee, C. Y., Tung, S.-N., & Wang, T.-H. *Applied Mathematical Finance*, 32(6), 379–422 (2026).

[Stylized facts in Web3.](https://doi.org/10.3934/fmf.2024021) Silva, A. C., Tung, S.-N., & Chen, W.-R. *Frontiers of Mathematical Finance*, 3(4), 572–609 (2024).

[An arbitrage driven price dynamics of Automated Market Makers in the presence of fees.](https://doi.org/10.3934/fmf.2024018) Najnudel, J., Tung, S.-N., Yamazaki, K., & Yen, J.-Y. *Frontiers of Mathematical Finance*, 3(4), 560–571 (2024).

### Number Theory

[On the automorphy of 2-dimensional potentially semistable deformation rings of $G_{\mathbb{Q}_p}$.](https://doi.org/10.2140/ant.2021.15.2173) Tung, S.-N. *Algebra & Number Theory*, 15(9), 2173–2194 (2021).

[On the modularity of 2-adic potentially semi-stable deformation rings.](https://doi.org/10.1007/s00209-020-02588-4) Tung, S.-N. *Mathematische Zeitschrift*, 298, 107–159 (2021).

[Finiteness properties of the category of mod p representations of $\mathrm{GL}_2(\mathbb{Q}_p)$.](https://doi.org/10.1017/fms.2021.72) Paškūnas, V., & Tung, S.-N. *Forum of Mathematics, Sigma*, 9, e80 (2021).
