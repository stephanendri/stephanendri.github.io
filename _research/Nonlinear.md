---
title: "Nonlinear asset pricing"
collection: research
permalink: /research/Nonlinear
excerpt: '<div style="text-align: justify "> This paper shows how truly independent nonlinear factors improve the stochastic discount factor estimation. Their main purpose is to serve as factors to predict future returns out-of-sample. We use the Fama-French 25 ME/BM- sorted portfolios and fifty anomaly portfolios adding interaction terms built using individual stock characteristics. Then, we estimate the SDF using raw characteristic return, linear principal component, and a nonlinear principal component. We found that the SDF estimated using nonlinear factors outperform the one using linear factors or raw characteristic returns in terms of OOS $R^2$ performance. The nonlinearity introduced through the nonlinear PC performs very well with respect to the nonlinearity introduced through interaction.</div>'
date: 2021-01-01
venue: 'Working paper'
paperurl: <!--'http://stephanendri.github.io/files/NLPC_paper.pdf'-->
citation: 'Stéphane, N Dri. (2021). &quot;Nonlinear asset pricing.&quot; <i>Working paper</i>.'
---
<!-- <div style="text-align: justify "> This paper shows how truly independent nonlinear factors improve the stochastic discount factor estimation. Their main purpose is to serve as factors to predict future returns out-of-sample. We use the Fama-French 25 ME/BM- sorted portfolios and fifty anomaly portfolios adding interaction terms built using individual stock characteristics. Then, we estimate the SDF using raw characteristic return, linear principal component, and a nonlinear principal component. We found that the SDF estimated using nonlinear factors outperform the one using linear factors or raw characteristic returns in terms of OOS R^2 performance. The nonlinearity introduced through the nonlinear PC performs very well with respect to the nonlinearity introduced through interaction.</div> -->

[Slides](http://stephanendri.github.io/files/NLPC_paper.pdf){: .btn}

<!--[Paper](http://stephanendri.github.io/files/JMP.pdf) -->

<!--Recommended citation: Stéphane N'Dri (2021). "Long run carbon consumption risks and asset prices"  <i>Working paper </i>.-->

## Motivation

* In modern finance, the price of any asset is obtained by the expected discounted payoffs : $$p_t^{i}=E_t(SDF_{t+1}CF_{t+1}^{i})$$
  * An estimation error in the stochastic discount factor (SDF) will be reflected in the price;
  * Well assess the SDF is important to reduce the pricing error.
* In this paper, I use the nonlinear principal components (PCs) as factors to estimate the SDF as opposed to the linear PCs as it is usually done. (See Kozak et al. (2020))
  * Account for the nonlinearities in the data.
* Advantages of using nonlinear factors :
  * Factors are truly independent as opposed to linear PCs which
are merely uncorrelated. 
    * As a consequence, I capture truly different risk measures.
  * Need less factors when using nonlinear PCs than when
using linear counterpart. 
    * As a consequence, I have a parsimonious model.
  * The increasing number of anomalies is not a problem anymore.

## Methodology

* Let $ r_{t}=( r_{1,t},..., r_{N,t})'$ be the vector of excess returns of N portfolios, t=1,...,T
* Let $Z_{t}$ be a N-by-k matrix of asset anomaly characteristics; 
* Let $RC_t=Z_{t-1}'r_t$ be a k-by-1 vector of raw characteristic returns;
  * Extract linear and nonlinear factors from RC;
  * F is either RC or the linear factors or the nonlinear factors.
* Let $\Sigma=Cov(F)$ be a k-by-k variance-covariance matrix of the factors;
* Let $\mu=\mathbb{E}(F)$ be a k-by-1 vector of expected factor returns;
* $SDF_t=1-\lambda'(F_t-\mathbb{E}F_t)$
* I estimate two models : a purely linear model and an hybrid model;
* For each model :
* I impose two kind of penalties to estimate the SDF coefficients :
  * L2 pen :
$\hat \lambda=arg \min_{\lambda}( \mu -\Sigma \lambda)'\Sigma^{-1}( \mu -\Sigma \lambda)+\gamma \lambda'\lambda$
  * L1L2pen :
$\hat \lambda=arg \min_{\lambda}( \mu -\Sigma \lambda)'\Sigma^{-1}( \mu -\Sigma \lambda)+\gamma_1 \sum_{i=1}^{k} |\lambda_i |+\gamma_2\lambda'\lambda$
* Estimate the parameter $\hat \lambda$ via Ridge or Elastic net using LAR-EN;
* Choose optimally the tuning parameters $\gamma$ or ( $\gamma_1$ and $\gamma_2$) using out-of-sample $R^2$.

<!--\gamma_1 \sum_{i=1}^{k} \mid \lambda_i \mid. or \gamma_1 \sum_{i=1}^{k} \lvert \lambda_i \rvert--> 
 
 
## Findings
* The hybrid model requires less risk factors to achieve the highest out-of-sample performance compared to a model using only linear factors or a model projected into the raw characteristic returns. 
* Weight shifting on some anomalies. The mimicking portfolios (MPs) and the linear factors disagree on the anomalies that are marginal in terms of weights
* I believe that the nonlinear principal components have good prediction power. 
* Thus, they should be taken into account for the development of future factor model.

