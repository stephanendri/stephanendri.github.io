---
title: "JMP - Long run carbon consumption risks and asset prices"
collection: research
permalink: /research/JMP
excerpt: '<div style="text-align: justify "> 
This paper analyzes how environmental policies that aim to reduce carbon emissions affect asset prices and household consumption. Using novel data, I propose a measure of carbon emissions from a consumer point of view and a carbon consumption growth risk measure. The measures are based on information on aggregate consumption and the carbon footprint for each good and service. To analyze the effects of environmental policies, a long-run risks model is developed where consumption growth is decomposed into two components: the growth rate of carbon consumption and the growth rate of the share of carbon consumption out of total consumption. This paper argues that the long-run risk in consumption growth comes mainly from the carbon consumption growth arising from policies and actions to curb emissions, such as the Paris Agreement and the U.N. Climate Change Conference (COP26). My model helps to detect long-run risk in consumption from climate policies while simultaneously solving the equity premium and volatility puzzles. The decomposition of consumption could lead to identifying the most polluting consumption items and to constructing an investment strategy that minimizes or maximizes a long-term environmental criterion. </div>'
date: 2021-10-01
venue: 'Working paper'
paperurl: <!--'[Slides](http://stephanendri.github.io/files/Slides_LRCCR.pdf)'-->
citation: 'Stéphane, N Dri. (2021). &quot;Long run carbon consumption risks and asset prices .&quot; <i>Working paper</i>.'
---
<!-- <div style="text-align: justify "> 
This paper analyzes how environmental policies that aim to reduce carbon emissions affect asset prices and household consumption. Using novel data, I propose a measure of carbon emissions from a consumer point of view and a carbon consumption growth risk measure. The measures are based on information on aggregate consumption and the carbon footprint for each good and service. To analyze the effects of environmental policies, a long-run risks model is developed where consumption growth is decomposed into two components: the growth rate of carbon consumption and the growth rate of the share of carbon consumption out of total consumption. This paper argues that the long-run risk in consumption growth comes mainly from the carbon consumption growth arising from policies and actions to curb emissions, such as the Paris Agreement and the U.N. Climate Change Conference (COP26). My model helps to detect long-run risk in consumption from climate policies while simultaneously solving the equity premium and volatility puzzles. The decomposition of consumption could lead to identifying the most polluting consumption items and to constructing an investment strategy that minimizes or maximizes a long-term environmental criterion.</div> -->

[Slides](http://stephanendri.github.io/files/Slides_LRCCR.pdf){: .btn}
[Paper](http://stephanendri.github.io/files/Carbon_consumption_risk_JMP.pdf){: .btn}

## Motivation

* FIRST
  * Environnemental issues
  * Consumption of goods and services pollutes the environnement ;
  * Production vs. consumption-based CO2 emissions (GCP). [Fact](http://stephanendri.github.io/files/cons_prod.png){: .btn}
  * Despite that, most papers and climate policies focus on the production side.

* SECOND
  * Climate change is a long horizon phenomenon ;
  * Need a long-run risk model to assess it ;
  * Yet, the effect of the canonical long-run risks on the assets depends on investors detecting it ;
  * Require a new LRR model by considering carbon emissions consumption.
  * However, emission does have long-run risk and is more detectable :
  * Curbing carbon emissions at the pre-industrial level ;
  * Emission $\rightarrow$ Damages $\rightarrow$ affects aggregate consumption.


## Data
![MarineGEO circle logo](http://stephanendri.github.io/files/pic22.png "MarineGEO logo")

<!--Model
======
![MarineGEO circle logo](http://stephanendri.github.io/files/model1.png "MarineGEO logo")

Findings
======
![MarineGEO circle logo](http://stephanendri.github.io/files/finding1.png "MarineGEO logo")-->


## Model
**Long-run carbon consumption risks model**

 * Consumption growth decomposition :
<font color=red>$$\Delta c_{t+1} = \Delta cc_{t+1} - \Delta\alpha_{cc, t+1}$$ </font> 

 * Carbon consumption growth dynamic :
<font color=black>$$\Delta cc_{t+1} = \nu_{cc} + x_t + \sigma_t \epsilon_{cc, t+1}$$</font> 

 * Conditional expectation of carbon consumption growth dynamic :
<font color=black>$$x_{t+1} = \rho_x x_t + \psi_x \sigma_t \epsilon_{x, t+1}$$ </font> 

 * Conditional volatilty of carbon consumption growth dynamic : 
<font color=black>$$\sigma_{t+1}^2 = (1 - \nu)\sigma^2 + \nu \sigma_t^2 + \sigma_w \epsilon_{\sigma, t+1}$$ </font> 

 * Share of carbon consumption out of total consumption growth dynamic :
<font color = black> $$\Delta\alpha_{cc, t+1} = \nu_\alpha (1 - \rho_\alpha) + \rho_\alpha \Delta\alpha_{cc, t} + \sigma_\alpha \epsilon_{\alpha, t+1} + \pi \sigma_t \epsilon_{cc, t+1}$$</font>

 * Dividend of any asset i growth dynamic :
<font color = red> $$\Delta d_{i, t+1} = \nu_i + \phi_i x_t + \phi_{\alpha, i} \Delta\alpha_{cc, t} + \psi_i \sigma_t \epsilon_{i, t+1}$$ </font> 

Where $\epsilon_{x, t+1}, \epsilon_{cc, t+1}, \epsilon_{\alpha, t+1}, \epsilon_{i, t+1}$ and $\epsilon_{\sigma, t+1}$ are i.i.d.
 
 
 
## Findings
* LRCCR model replicates the equity premium, volatility and risk-free rate much better than LRR :
  * By decomposing consumption growth into two components ;
  * Long-run risks in both expected carbon consumption and volatility.
* My LRCCR model increases the capacity to detect the long-run risk during the period 1956-2018. But during the period 1930 - 1955, it was less dectectable :
  * Investors can profit from it using climate change news ;
* The long-run risk variable <font color="blue">$x_t$</font> and its conditional variance <font color="blue">$\sigma _t ^2$</font> help improving the predictability of the equity premium and the consumption growth.

<!--[Paper](http://stephanendri.github.io/files/JMP.pdf) -->

<!--Recommended citation: Stéphane N'Dri (2021). "Long run carbon consumption risks and asset prices"  <i>Working paper </i>.-->
