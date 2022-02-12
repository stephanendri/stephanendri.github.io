---
title: "Asset Pricing with Nonlinear Principal Components"
collection: research
permalink: /research/Nonlinear
excerpt: '<div style="text-align: justify "> This paper studies the role of truly independent nonlinear factors in asset pricing. While the most successful stochastic discount factor (SDF) benchmarks pricing the cross-section of stock returns are obtained from regularized linear principal components of characteristic-based returns we show that allowing for substitution of some linear principal components by independent nonlinear factors consistently improves the ability of the SDF to price this cross-section. We use the Fama-French 25 ME/BM-sorted portfolios, fifty anomaly portfolios, and fifty anomalies plus characteristic-based interaction terms to test the effectiveness of the nonlinear dynamic factors. The SDF estimated using a mixture of nonlinear and linear factors outperforms the ones using solely linear factors or raw characteristic returns in terms of out-of-sample $R^2$ pricing performance. Moreover, the hybrid model -using both nonlinear and linear principal components- requires less risk factors to achieve the highest out-of-sample performance compared to a model using only linear factors. </div>'
date: 2021-01-01
venue: 'Working paper'
paperurl: <!--'http://stephanendri.github.io/files/NLPC_paper.pdf'-->
citation: 'Caio Almeida, René Garcia, Stéphane N Dri. (2021). &quot;Asset Pricing with Nonlinear Principal Components.&quot; <i>Working paper</i>.'
---

[Slides](http://stephanendri.github.io/files/NLPC_paper.pdf){: .btn}
[Paper](http://stephanendri.github.io/files/AlmeidaGarciaNdriDecember2021.pdf){: .btn}

<!--[Paper](http://stephanendri.github.io/files/AlmeidaGarciaNdriDecember2021.pdf) -->

<!--Recommended citation: Stéphane N'Dri (2021). "Long run carbon consumption risks and asset prices"  <i>Working paper </i>.-->

## Motivation

* Look for a parsimonious stochastic discount factor (SDF);
* Increasing number of factors explaining the cross-section (CS) (\color{blue}Factor zoo.\color{black})
* Kozak et al. (2020) show the importance of rotating the SDF into a transformed space.
* Prior literature: Rotate the SDF into the space of linear principal components (PCs);
* This paper: Rotate the SDF into the space of nonlinear principal components;


## This paper

* How effective truly independent nonlinear factors are in pricing assets?


## Contribution

* First paper to empirically test the effectiveness truly independent nonlinear factors
  * In an asset pricing involving the identification of an SDF that prices the CS of stocks.


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

* For different fixed cross-sections of returns, the nonlinear SDF consistently outperforms the linear specification;
 * For the FF25P: 65% versus 49% 
 * For the 50 anomalies:  55% versus 22% 

* Nonlinear SDF requires less factors. 
 * For the 50 anomalies:  5 factors versus 15-20 factors
