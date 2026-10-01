# gmm-menu-fitter
This repository provides a quantitative operations model that estimates and simulates how institutional supply chains—specifically daily university dining menus—substitute protein offerings in response to macroeconomic commodity stress.

The core architecture utilizes a **Two-Step Generalized Method of Moments (GMM)** to fit empirical menu changes against daily fluctuations in Brent Crude (`BZ=F`) and Live Cattle (`LE=F`) futures. Rather than standard Markovian decay, the estimator applies heavy-tailed power-law memory kernels to capture how the cumulative memory of market volatility influences localized procurement decisions over time.

The optimized substitution parameters ($\beta$, $\gamma$) are then passed into a **100-path Monte Carlo forecasting engine**. This simulation models future commodity trajectories using Geometric Brownian Motion with an active stochastic feedback loop: the drift parameter of future beef prices dynamically adjusts based on the institution's predicted probability of substituting toward red meat, explicitly linking local operational hazards back to global price elasticities.
