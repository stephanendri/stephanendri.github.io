---
title: "Asset Pricing with Nonlinear Principal Components"
collection: research
permalink: /research/Nonlinear
excerpt: '<div style="text-align: justify "> This paper shows how truly independent nonlinear factors improve the stochastic discount factor (SDF) estimation. The main purpose of the nonlinear factors is to serve as factors to predict future returns out-of-sample. We use the Fama-French 25 ME/BM- sorted portfolios and fifty anomaly portfolios adding interaction terms built using individual stock characteristics to test the effectiveness of the nonlinear factors. Then, we estimate the SDF using raw characteristic return, linear principal component, and a nonlinear principal component. We found that the SDF estimated using a mixture of nonlinear and linear factors outperform the one using solely linear factors or raw characteristic returns in terms of out-of-sample $R^2$ performance. More importantly, the hybrid model -using both nonlinear and linear principal components- requires less risk factors to achieve the highest out-of-sample performance compared to a model using only linear factors.</div>'
date: 2021-01-01
venue: 'Working paper'
paperurl: <!--'http://stephanendri.github.io/files/NLPC_paper.pdf'-->
citation: 'Caio Almeida, René Garcia, Stéphane N Dri. (2021). &quot;Asset Pricing with Nonlinear Principal Components.&quot; <i>Working paper</i>.'
---
<!-- <div style="text-align: justify "> This paper shows how truly independent nonlinear factors improve the stochastic discount factor estimation. The main purpose of the nonlinear factors is to serve as factors to predict future returns out-of-sample. We use the Fama-French 25 ME/BM- sorted portfolios and fifty anomaly portfolios adding interaction terms built using individual stock characteristics to test the effectiveness of the nonlinear factors. Then, we estimate the SDF using raw characteristic returns, linear principal component, and a nonlinear principal component. We found that the SDF estimated using a mixture of nonlinear and linear factors outperform the one using solely linear factors or raw characteristic returns in terms of OOS R^2 performance. More importantly, the hybrid model -using both nonlinear and linear principal components- requires less risk factors to achieve the highest out-of-sample performance compared to a model using only linear factors.</div> -->

[Slides](http://stephanendri.github.io/files/NLPC_paper.pdf){: .btn}

<!--[Paper](http://stephanendri.github.io/files/JMP.pdf) -->

<!--Recommended citation: Stéphane N'Dri (2021). "Long run carbon consumption risks and asset prices"  <i>Working paper </i>.-->

## Motivation

* In modern finance, the price of any asset is obtained by the expected discounted payoffs : $$p_t^{i}=E_t(SDF_{t+1}CF_{t+1}^{i})$$
  * An estimation error in the stochastic discount factor (SDF) will be reflected in the price;
  * Well assess the SDF is important to reduce the pricing error.
* In this paper, we use the nonlinear principal components (PCs) as factors to estimate the SDF as opposed to the linear PCs as it is usually done. (See Kozak et al. (2020))
  * Account for the nonlinearities in the data.
* Advantages of using nonlinear factors :
  * Factors are truly independent as opposed to linear PCs which
are merely uncorrelated. 
    * As a consequence, we capture truly different risk measures.
  * Need less factors when using nonlinear PCs than when
using linear counterpart. 
    * As a consequence, we have a parsimonious model.
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
* We estimate two models : a purely linear model and an hybrid model;
* For each model :
* We impose two kind of penalties to estimate the SDF coefficients :
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
* We believe that the nonlinear principal components have good prediction power. 
* Thus, they should be taken into account for the development of future factor model.

