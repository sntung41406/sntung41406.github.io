---
title: "Research"
---

My research studies **liquidity in digital markets**. When a market is run by an algorithm rather than by a dealer, someone still has to supply the liquidity it trades against. I ask where that liquidity sits across prices, what a liquidity position is worth and how to hedge it, and how the rules that govern liquidity should be designed when traders and providers respond strategically.

The common object in this work is the **liquidity profile**: the amount of liquidity available at each price. The profile determines how far a trade moves the price, which providers earn fees, and how each provider's holdings change as the price moves. The work follows three directions, described below. Projects marked *ongoing* are work in progress; their descriptions are not finished results.

## Liquidity Modeling and Pricing

How does the liquidity profile evolve, what is a liquidity position worth, and how should a provider choose its profile?

- **Price dynamics and long-run wealth** — models of the AMM pool price as a process kept within a fee band around an external reference price, and the long-run growth rate of a liquidity provider's wealth in geometric mean market makers (G3Ms). A related empirical study documents heavy tails and volatility clustering in Web3 asset returns across centralized and decentralized exchanges.
- **Concentrated liquidity** — a continuous-time framework that treats the liquidity profile as the state variable; a measurement of the Uniswap v3 profile as a surface over time and price; and a decomposition of impermanent loss into a strip of options weighted by the profile, which identifies loss-versus-rebalancing (LVR) as its non-hedgeable part.
- **Stochastic dynamics of the profile** — a stochastic partial integro-differential equation (SPIDE) for how the profile evolves, reduced to a small number of modes describing its level, slope, and curvature, and calibrated to Uniswap pools.
- **Liquidity control in factor space** *(ongoing)* — with Cheuk Yin Lee, Kohta Takehara, and Tai-Ho Wang: an individual provider's choice of liquidity profile, posed as a stochastic control problem over a finite set of profile modes.
- **Further ongoing work** — the valuation of impermanent loss together with fee income, wealth growth in multi-asset G3Ms, and pricing and hedging for fully collateralized option-like claims.

## Strategic Liquidity and Market Design

How should liquidity and trading rules be chosen when the participants who supply and consume liquidity respond strategically? I study this at the level of individual providers within a protocol and at the level of the protocol's rules. (Related external challenges: [AMM challenge](https://www.optimizationarena.com/amm) · [Prop AMM challenge](https://www.optimizationarena.com/prop-amm))

- **Price-impact design** *(ongoing)* — a Stackelberg game in which a liquidity provider commits to a price-impact rule and competing arbitrageurs respond, including the conditions under which the arbitrageurs' game has a unique equilibrium. Adding fee-paying uninformed order flow is the next step.
- **Proprietary AMMs** *(ongoing)* — a single strategic provider choosing how to distribute its quotes across prices against informed and uninformed traders. Equilibrium with many competing providers is an open question.
- **Auction-managed AMMs** *(ongoing)* — how a manager who leases the right to set fees should choose rent and fees over a lease; a control problem for a single manager. (Original mechanism, by Adams and coauthors: [am-AMM paper](https://link.springer.com/chapter/10.1007/978-3-032-07024-1_6))
- **Batch routing** *(ongoing)* — a model, motivated by CoW Protocol, that combines direct matching between orders with routing through pools.
- **Self-supervised regime detection (SSRD)** *(ongoing)* — whether market features available at decision time identify regimes that predict later outcomes for liquidity providers.
- **Multi-AMM simulation in JAX** *(ongoing)* — a simulator of competing pools for experiments on fee and pool design, including reinforcement learning.

## Prediction Markets

How should event contracts be priced and funded when prices are probabilities and every position resolves into a fixed payout? Forecasting supports this direction: I evaluate forecasting and learning methods by how well they inform liquidity decisions. (Related external challenge: [Prediction market challenge](https://www.optimizationarena.com/prediction-market-challenge))

- **Forecasting against market prices** — pre-game forecasts of professional League of Legends map outcomes, compared with matched Polymarket contracts. The study benchmarks forecasts against event-contract prices; it does not establish a trading advantage.
- **Concentrated-liquidity AMM for prediction markets** *(ongoing)* — with Tai-Ho Wang and Kohta Takehara: a binary-market AMM funded by a single collateral deposit that provides liquidity over a range of prices, and the provider's expected loss under different rules for what happens at the edges of the range.
- **World models for short-horizon contracts** *(ongoing, planning stage)* — learning representations of short-horizon Polymarket contracts in the spirit of joint-embedding predictive architectures (JEPA), first for forecasting and eventually for planning liquidity provision. (LeCun on JEPA and world models: [part I](https://www.youtube.com/watch?v=kYkIdXwW2AE) · [part II](https://www.youtube.com/watch?v=v_jDvpEGTIg))
- **Sports outcomes via temporal graph neural networks** *(ongoing)* — a graph neural network over historical match results for estimating team strength across competitions.

* * *

## Preprints

[Dynamics of the liquidity profile in concentrated liquidity provision: An SPIDE approach.](https://arxiv.org/abs/2610.30539) Lee, C. Y., Risk, J., Tung, S.-N., & Wang, T.-H. [arXiv:2610.30539](https://arxiv.org/abs/2610.30539) (2026).

[Pre-game paired-comparison modeling of professional League of Legends map outcomes.](https://arxiv.org/abs/2609.08060) Guan, M.-R., & Tung, S.-N. [arXiv:2609.08060](https://arxiv.org/abs/2609.08060) (2026).

[Pricing and hedging for liquidity provision in Constant Function Market Making.](https://arxiv.org/abs/2603.01344) Risk, J., Tung, S.-N., & Wang, T.-H. [arXiv:2603.01344](https://arxiv.org/abs/2603.01344) (2026).

[Dynamics of Liquidity Surfaces in Uniswap v3.](https://arxiv.org/abs/2509.05013) Risk, J., Tung, S.-N., & Wang, T.-H. [arXiv:2509.05013](https://arxiv.org/abs/2509.05013) (2025).

## Publications

### DeFi & Mathematical Finance

[A mathematical framework for modelling CLMM dynamics in continuous time.](https://doi.org/10.1007/s42521-026-00198-z) Tung, S.-N., & Wang, T.-H. *Digital Finance*, 8, Article 39 (2026).

[Growth rate of liquidity provider's wealth in G3Ms.](https://doi.org/10.1080/1350486X.2026.2662662) Tung, S.-N., Lee, C. Y., & Wang, T.-H. *Applied Mathematical Finance*, 32(6), 379–422 (2025).

[Stylized facts in Web3.](https://doi.org/10.3934/fmf.2024021) Silva, A. C., Tung, S.-N., & Chen, W.-R. *Frontiers of Mathematical Finance*, 3(4), 572–609 (2024).

[An arbitrage driven price dynamics of Automated Market Makers in the presence of fees.](https://doi.org/10.3934/fmf.2024018) Najnudel, J., Tung, S.-N., Yamazaki, K., & Yen, J.-Y. *Frontiers of Mathematical Finance*, 3(4), 560–571 (2024).

### Number Theory

[On the automorphy of 2-dimensional potentially semistable deformation rings of $G_{\mathbb{Q}_p}$.](https://doi.org/10.2140/ant.2021.15.2173) Tung, S.-N. *Algebra & Number Theory*, 15(9), 2173–2194 (2021).

[On the modularity of 2-adic potentially semi-stable deformation rings.](https://doi.org/10.1007/s00209-020-02588-4) Tung, S.-N. *Mathematische Zeitschrift*, 298, 107–159 (2021).

[Finiteness properties of the category of mod p representations of $\mathrm{GL}_2(\mathbb{Q}_p)$.](https://doi.org/10.1017/fms.2021.72) Paškūnas, V., & Tung, S.-N. *Forum of Mathematics, Sigma*, 9, e80 (2021).
