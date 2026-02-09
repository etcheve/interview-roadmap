### Options, Futures, and Other Derivatives

**Summary:**  
Covers the core concepts of derivatives, pricing models, risk management, and hedging strategies. Focuses on understanding mechanics, intuition, and practical applications in finance.

---

**1) Derivatives basics**  
- Value depends on an underlying (stock, rate, FX, commodity)  
- Main goals: hedging, speculation, arbitrage  
- **Key idea:** derivatives transfer risk; they don’t create or destroy it

---

**2) Futures & forwards**  
- **Forward:** OTC, customized, counterparty risk  
- **Future:** exchange-traded, standardized, margining, daily settlement (mark-to-market)  
- Linear payoff: profit/loss moves one-for-one with underlying  
- Core concepts:
  - Long vs short  
  - Spot vs forward price  
  - Cost of carry  
  - Convergence at maturity  

---

**3) Margin, leverage, and clearing**  
- Initial margin, maintenance margin, margin calls  
- Daily settlement reduces counterparty risk  
- Clearing houses reduce systemic risk  
- **Interview takeaway:** Futures are safer because losses are realized daily  

---

**4) Interest rates & bond pricing**  
- Zero-coupon bonds, yield curves, bootstrapping  
- Rates ↔ bond prices, duration, convexity  
- Compounding conventions matter (simple, continuous)  

---

**5) Forward & futures pricing**  
- Forward price = spot price grown at risk-free rate − income + storage costs  
- Dividends, coupons, foreign interest rates matter  
- Arbitrage keeps prices aligned  
- **Key mental model:** mispricing → risk-free profit  

---

**6) Options basics**  
- Call vs put; European vs American  
- Intrinsic value vs time value  
- Nonlinear payoff:
  - Limited downside  
  - Potentially unlimited upside (calls)  

---

**7) Put-call parity**  
- Fundamental relation: Call − Put = Forward − Strike discounted  
- Ensures pricing consistency, arbitrage detection, foundation for option theory  
- **Interview note:** missing this is noticeable  

---

**8) Binomial trees**  
- Discrete model of price evolution  
- Introduces risk-neutral valuation  
- Probabilities don’t reflect real-world beliefs  

---

**9) Black-Scholes model**  
- Closed-form solution for European options  
- Assumptions: lognormal prices, constant volatility, frictionless markets  
- Inputs:
  - Spot price  
  - Strike  
  - Time  
  - Risk-free rate  
  - Volatility (only unobservable)  
- Core pricing model, even if assumptions are violated  

---

**10) Greeks (risk sensitivities)**  
- Delta: sensitivity to price  
- Gamma: curvature (delta of delta)  
- Vega: sensitivity to volatility  
- Theta: time decay  
- Rho: interest rates  
- Used for hedging, risk management, portfolio neutralization  
- **Interview tip:** Delta-hedging ≠ risk-free forever, only instantaneously  

---

**11) Volatility**  
- Implied vs historical  
- Volatility smiles and skews  
- **Key insight:** markets quote options in volatility space, not price space  

---

**12) Hedging strategies**  
- Delta hedging with stocks or futures  
- Static vs dynamic hedging  
- Transaction costs break perfect hedges  
- **Reality check:** continuous hedging is impossible; risk leaks through jumps  

---

**13) Interest rate derivatives**  
- Swaps, FRAs, caps, floors  
- Swap = series of forward rate agreements  
- LIBOR / SOFR curves matter  
- Core for rates desks  

---

**14) Credit derivatives**  
- Credit default swaps (CDS)  
- Default probability, recovery rate  
- Separates credit risk from interest rate risk  
- CDS pricing ties to bond spreads  

---

**15) Exotic options (overview)**  
- Asian, barrier, lookback, digital options  
- Introduce path-dependence  
- Often require numerical methods (Monte Carlo, PDEs)  
- Used to shape risk profiles precisely  

---

**16) Risk management & stress testing**  
- Value at Risk (VaR), Expected Shortfall  
- Stress scenarios often better than pure statistics  

---

**Big mental model from Hull:**  
- Pricing is about no-arbitrage  
- Probabilities are risk-neutral  
- Volatility is the key unknown  
- Hedging reduces risk but never removes it  
- Markets are imperfect → models are approximations  

---

**Interview essentials:**  
- Explain futures vs forwards  
- Explain options payoff & Greeks  
- Explain risk-neutral pricing intuitively  
- Explain hedging tradeoffs

