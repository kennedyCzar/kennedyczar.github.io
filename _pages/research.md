---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---


<style>
img{
  border-radius: 10px;
}
iframe {
  width: 175px;
  display: inline;
  vertical-align:middle;
  <!-- margin-bottom:5px; -->
  <!-- margin-left:5px; -->
  <!-- border: 1px solid red; -->
}
.col-md-3 {
  margin:0;
  padding:0;
  margin-top:10px;
  margin-bottom:10px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  height: auto;
  float: none;
  background:white;
  border-radius:20px;
  <!-- border: 1px solid black; -->
}
tr:nth-child(even) {
  background-color: #404040!important;
}
.btn-success {
  font-family: Raleway-SemiBold;
  font-size: 7px;
  color: rgba(103, 192, 103, 0.75);
  letter-spacing: 1px;
  line-height: 15px;
  border: 2px solid rgba(103, 192, 103, 0.75);
  border-radius: 40px;
  background: transparent;
  transition: all 0.3s ease 0s;
}
.btn-primary {
  font-size: 10px;
  letter-spacing: 1px;
  line-height: 15px;
  border: 1px;
  border-radius: 40px;
  transition: all 0.3s ease 0s;
}
.btn-success:hover {
  color: #FFF;
  background: rgb(103, 192, 103, 0.75);
  border: 1px solid rgb(103, 192, 103, 0.75);
}

.btn-danger {
  font-size: 10px;
  letter-spacing: 1px;
  line-height: 15px;
  border: 1px;
  border-radius: 40px;
  transition: all 0.3s ease 0s;
}

.btn-danger:hover {
  color: #FFF;
  background: rgba(217, 83, 78, 0.75);
  border: 2px rgba(217, 83, 78, 0.75);
}

.btn-warning {
  font-size: 10px;
  letter-spacing: 1px;
  line-height: 15px;
  border: 1px;
  border-radius: 40px;
  transition: all 0.3s ease 0s;
}

.btn-warning:hover {
  color: #FFF;
  background: grey;
  border: 2px grey;
}
</style>

## Research
<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-9 col-sm-12">
<img src="{{ site.url }}{{ site.baseurl }}/images/software/gcvae_2.png" width="70%" height="170px" />
<h4><b>GCVAE: Generalized-Controllable Variational Autoencoder</b></h4>
<a href="{{site.url}}{{site.baseurl}}/papers/BELIEF2022_POSTER.pdf" target="_blank"><button class="btn btn-warning btn-sm">POSTER</button></a>
<a href="https://github.com/kennedyCzar/GCVAE" target="_blank"><button class="btn btn-primary btn-sm">GIT: GCVAE</button></a>
<a href="https://arxiv.org/abs/2206.04225" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> 
<a href = "https://colab.research.google.com/drive/1QlbAte_TOH5-WXo8NUCuMOiO7OFO43lW?usp=sharing" target = "_blank"><img alt = "Open in Colab" src = "https://colab.research.google.com/assets/colab-badge.svg"></a>

<b>Authors:</b>
<i>Kenneth Ezukwoke, Anis Hoayek, Mireille Batton-Hubert, Xavier Boucher</i>

GCVAE is a generalized version of VAE with adaptive weights.
It solves the problem of disentanglement and reconstuction trade-off by replacing fixed hyperparameters with trainable Lagrangian hyperparameters:
* Maximizing mutual information $$I_p(x, z)$$ during data reconstruction ($$x$$: data; $$z$$: latent)
* Data reconstruction is done $$w.r.t$$ inference constraints ($$e.g.$$, $$Kullback–Leibler$$ $$divergence$$)
* Optimization framework designed to introduce controllable and adaptive Lagrangian hyperparameters
* Proportional-Integral-Derivative (PID) controller serves for automatic controlling of hyperparameters ($$\alpha, \beta, \gamma$$)

The controllable hyperparameters ensures simultaneously learning a well disentangled representation with high reconstruction quality and minimal information loss during the bottleneck-compression.
</div>
<div class="col-md-3 col-sm-12">
  <img src="{{site.url}}{{site.baseurl}}/images/software/gcvae.png" width="175px"/>
</div>
</div>
</div>


<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-9 col-sm-12">
<img src="{{ site.url }}{{ site.baseurl }}/images/software/fdr_fa.png" width="80%" height="170px" />
<h4><b>Leveraging Pre-trained Models for Failure Analysis Triplets Generation</b></h4>
<a href="https://github.com/FA4-0/Leveraging-Pre-trained-Models-for-Failure-Analysis-Triplets-Generation" target="_blank"><button class="btn btn-primary btn-sm">GIT: LPMFATG</button></a>
<a href="https://arxiv.org/abs/2210.17497" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> 


<b>Authors:</b>
<i>Kenneth Ezukwoke, Anis Hoayek, Mireille Batton-Hubert, Xavier Boucher, Pascal Gounet, Jerome Adrian</i>

The research focuses on leveraging pretrained language models (such as transformers) for failure analysis (diagnosis) in semiconductor industry.
* Generative Pretrained Transformers ($$GPT2$$) is best for the task of Failure Analysis Triplet Generation (FATG)
* Sequential structured data is challenging for Encoder-Decoder Transformers especialy for data-to-text problems
* BLEU, ROUGE and METEOR scores do not correlate with human evaluation when scoring sequential data-to-text problems
* We introduce Levenshstein Sequential Evaluation ($$LESE-N$$) metric, which correlates with human-evaluation

Significantly improved results fine-tuning pretrained GPT2 (a decoder only transformer) for the downstream task of FATG. Next, we introduce the GCVAE variational loss for fine-tuning.
</div>
<div class="col-md-3 col-sm-12">
  <img src="{{site.url}}{{site.baseurl}}/images/software/lese.png" width="205px" height="200px"/>
</div>
</div>
</div>

<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-9 col-sm-12">
<img src="{{ site.url }}{{ site.baseurl }}/images/software/biggcvae.png" width="80%" height="200px" />
<h4><b>Big GCVAE</b></h4>
<a href="https://github.com/FA4-0/Big-GCVAE" target="_blank"><button class="btn btn-primary btn-sm">GIT: Big-GCVAE</button></a>


<b>Authors:</b>
<i>Kenneth Ezukwoke, Anis Hoayek, Mireille Batton-Hubert, Xavier Boucher, Pascal Gounet, Jerome Adrian</i>

This work is the convergence resulting from finetuning Large Language Model (LLM) with the Generalized-Controllable Variational AutoEncoder (GCVAE), for improved Failure Analysis Triplet Generation (FATG)
* Introduces latent space modeling for domain generalization, hence improving inference and generation
* Finetuned on Generalized-Controllable Variational AutoEncoder loss (GCVAE) exhibits superior performance over stateof-the-arts
* Demonstrates capacity to generate failure analysis triplets specifically tailored to root cause identification in product packages
* Self-supervised model that operates with adaptive-controllable hyperparameters, eliminating the need for human intervention in the decision-making process

An improved domain specific (FATG) LLM model that introduces latent modeling for domain generalization and generation.
</div>
<div class="col-md-3 col-sm-12">
  <img src="{{site.url}}{{site.baseurl}}/images/software/gcvae_mmd.png" width="205px" height="200px"/>
</div>
</div>
</div>


<div class="jumbotron">
<div class="row align-items-end">
<div class="col-md-9 col-sm-12">
<img src="{{ site.url }}{{ site.baseurl }}/images/software/oanda.jpg" width="80%" height="110px" />
<h4><b>FORECASTING-1.0 / Automated Signal Generator</b></h4>
<a href="https://github.com/kennedyCzar/FORECASTING-1.0" target="_blank"><button class="btn btn-primary btn-sm">GIT: FORECASTING-1.0</button></a>
<a href="https://github.com/fibai/AUTOMATED-SIGNAL-GENERATOR" target="_blank"><button class="btn btn-primary btn-sm">GIT: ASG</button></a>
<!--<a href="https://arxiv.org/abs/2210.17497" target="_blank"><button class="btn btn-danger btn-sm">PAPER</button></a> -->


<b>Author:</b>
<i>Kenneth Ezukwoke</i>

A financial research software with the capacity to automatically generate signals for algorithmic trading using <a href = 'https://developer.oanda.com/rest-live-v20/introduction/' target="_blank">OANDA v20 REST API</a> as data source.
* Data pool request for currencies, metals, derivatives and commodities for different timeframes (e.g., H30, H6, H8, H12, W) based on OANDA v20 REST API
* Built on well known trend and price-based technical indicators (e.g., SMA, EMA, MACD, HMA, Stoch-Oscilator, CCI, SuperTrend) for signal generation
* Interactive Graphical User Interface (GUI) for seemless strategy control

Disclaimer: FORECASTING-1.0 and ASG are research tools for educational and experimental purpose only. Software is subject to users discretion and open to financial risk upon usage.
</div>
<div class="col-md-3 col-sm-12">
  <img src="{{site.url}}{{site.baseurl}}/images/software/AI-signal.gif" width="205px" height="200px"/>
</div>
</div>
</div>

## Selected projects

<div class="jumbotron">
<div class="datatable-begin" width="100%"></div>

| Project      | Description | Git    |
| :---        |    :----:   |          ---: |
| Advance Machine Learning- Kernel Methods      | Implementation of key advance ML algorithms (both classical and kernel versions)       | <a href="https://github.com/kennedyCzar/ADVANCE-MACHINE-LEARNING-KERNEL-METHOD" target="_blank"><button type="button" class="btn btn-success" >Github</button>   |
| Transfer Learning and Optimal Transport   | Subspace Alignment & Sinkhorn's Algorithm        |  <a href="https://github.com/kennedyCzar/TRANSFER-LEARNING-AND-OPTIMAL-TRANSPORT" target="_blank"><button type="button" class="btn btn-success" >Github</button>      |
| Social Mining Recommendation System   | Content based Recommedation system based on Graph mining        | <a href="https://github.com/kennedyCzar/Social-Mining-Recommendation-System" target="_blank"><button type="button" class="btn btn-success" >Github</button>      |
| Active and Online Learning Machine Learning Algorithms   | Online learning and Active learning ML algorithms        | <a href="https://github.com/kennedyCzar/Active-learning-and-online-learning-machine-learning-algorithms." target="_blank"><button type="button" class="btn btn-success" >Github</button>      |
| FORECASTING 1.0   | An intelligent model for time-series prediction and forecasting        | <a href="https://github.com/fibai/FORECASTING-1.0" target="_blank"><button type="button" class="btn btn-success" >Github</button>      |
| Unsupervised Anomaly Detection   | Unsupervised machine learning methods for novel anomaly detection        | <a href="https://github.com/PyAnomaly/UNSUPERVISED-ANOMALY-DETECTION" target="_blank"><button type="button" class="btn btn-success" >Github</button>      |
| NLP Pproject Book Insights with Plotly   | Machine learning for Natural Language Processing (NLP)        | <a href="https://github.com/kennedyCzar/NLP-PROJECT-BOOK-INSIGHTS-WITH-PLOTLY" target="_blank"><button type="button" class="btn btn-success" >Github</button>      |
| Stock Return Prediction using KNN-SVM-GAUSSIAN-ADABOOST   | Forecast stock prices using classical machine learning techniques        | <a href="https://github.com/kennedyCzar/STOCK-RETURN-PREDICTION-USING-KNN-SVM-GUASSIAN-PROCESS-ADABOOST-TREE-REGRESSION-AND-QDA" target="_blank"><button type="button" class="btn btn-success" >Github</button>      |

<div class="datatable-end"></div>
</div>



