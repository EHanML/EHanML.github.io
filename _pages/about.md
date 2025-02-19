---
layout: single
permalink: /about/
title: About
author_profile: true
header:
    overlay_image: /assets/images/header.jpg
    # caption: "Photo by [Joel Filipe](https://unsplash.com/@joelfilip) on [Unsplash](https://unsplash.com)"
    actions:
      - label: "<i class='fas fa-file-pdf'></i> Resume"
        url: /assets/docs/resume.pdf
classes: wide
date: May 12, 2021
---

<!-- bundle exec jekyll serve -w -->

I am engaged in gaining **wide and deep** knowledge of cutting-edge machine learning (ML) methods, **connect those dots**, and deliver precise data science solutions to real-world problems. 

<i class="far fa-sticky-note"></i> **Wide:** Familiar with ML algorithms across a wide range of domains.
  {: .notice--info}
  {: .text-justify}
<i class="far fa-sticky-note"></i> **Deep:** High level understanding of the statistical principiles behind ML algorithms.
  {: .notice--info}
  {: .text-justify}
<i class="far fa-sticky-note"></i> **Connect the dots:** Here is a metaphor. Imagine each ML knowledge as a dot. Then most industry-level applications are direct *leveraging* those dots (applying GAN with a dataset), most ML researches are *interpolating* those dots (inventing WGAN by replacing JS-divergence with Wasserstein distance), and very few ML researches are *extrapolating* (Ian Goodfellow inventing GAN). I am engaged in the interpolation of the dots, i.e., use the *convex hull* of my knowledge dots to solve real-world issues.
  {: .notice--info}
  {: .text-justify}

<!--- especially in agricultural scenarios. --->

<!---The field of agriculture has not fully benefited from AI so far. Currently, most agricultural AI applications are using machine learning (ML) techniques as **Maslow's hammer**;  they formulate the agricultural problems into the form that existing ML methods can process rather than design ML algorithms for specific argricultural problems. However, just like the CNN is developed for computer vision, the GNN is developed for social networks, the transformer is developed for NLP, and etc., we have limited methods that are designed specifically for particular agricultural problems. Hence, my research ambition is to develop domain specfic ML algorithms for the data revolution in argrculture.  --->

Currently, most real-world applications are using machine learning (ML) techniques as **Maslow's hammer**;  problems are formulated into the form that existing ML methods can process. However, just like CNN is developed for computer vision, GNN is developed for social networks, the transformer is developed for NLP, etc., we need to design **task-specific ML algorithms** for each data science task. To do that, an ML system should be **data-centric**; we need to **program in terms of the data**:

> 1. **Decide assumption**: understand data sources and decide what data assumptions should be made --- *what is the experience?*
> 2. **Decide model graph**: based on the real-world probelm, think of what the model archetecture should be like --- *what's the DAG/functional form?*
> 3. **Decide learning ( & inference) process**: find an optimization solver --- *how to teach the experiences to the model?*
> 4. **Decide bussiness metric**: connect bussiness values to a metric and update the model iteratively.
> 5. **Deploy the model to production**



<i class="far fa-sticky-note"></i>  **Maslow's hammer:** if all you have is a hammer, everything looks like a nail.
  {: .notice--info}
  {: .text-justify}


## My Background

<figure style="width: 36%" class="align-right">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/book1.png" alt="">
</figure> 

I am currently a Ph.D. candidate in the agricultural and biological engineering department at the University of Florida (UF) major in machine learning. I had two master's degrees in statistics and quantitative genetics (applied statistics) both at UF. I have 7+ years of research experience in data science, and have led several projects either individually or collaboratively, which result in peer-review publications. These projects are highly-interdisciplinary, which requires me to 1) communicate efficiently with domain experts and engineers, 2) fast learn a new domain, 3) be familiar with a wide range of machine learning technologies, and 4) keep updating with cutting-edge machine learning methods for state-of-the-art practices. 

<figure style="width: 36%" class="align-left">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/ds.png" alt="">
</figure> 

In my spare time, I enjoy reading machine learning books and learning about different machine learning areas. I finished more than 10 books and several online courses during my Ph.D. program, so I have the fundamental knowledge across a wide range of machine learning areas, including *Bayesian graphical model, computer vision, natural language processing, graph neural network, ensemble methods, kernel machines, Bayesian deep learning, generative model (e.g. GAN, VAE, EBM, diffusion probabilistic models, and score-based generative modeling), reinforcement learning, and meta-learning*. However, textbooks are not enough because the field of AI is developing faster than ever; new methods can become outdated in a few months. Hence, I never stop catching up with the latest papers published in the top AI conferences. I find many of these papers can be well summarized in few sentences so I create this [60s-Paper](/portfolio/) module to help people get the principles of these papers fast. My solid statistical training enables me to gain a deep understanding of why and how machine learning works so I can precisely deploy AI solutions to various scenarios (see my [Projects](/projects/)). 




<!-- Besides machine learning, I am passionate about real-world agricultural problems because it aims to solve basic human needs. Therefore, I am committed to contributing to the AI revolution of agricultural systems. My vision is to digitize agricultural problems and solve them with AI techniques. The AI revolution is an inevitable worldwide trend. However, the field of agriculture has not fully benefited from AI so far. Current agricultural AI applications are mostly classical statistical and machine learning decision-makers and other AI techniques, such as image recognition, that replace simple human labor. AI can do much more than that; AI is a general idea that formulates real-world problems to numerical representation that computers can process. My research's long-term goal is to use statistical AI techniques, such as machine learning, deep learning, and their Bayesian version, to help with the decision support systems and other agriculture featured problems. 

I am looking for acedemy job opportunities where I can keep learning the cutting eadge techniques and deliver AI solutions to the argricalural problems. My goal is to boost the efficiency of agricultural systems with machine learning techniques. Therefore, those who spent their entire life fighting for a basic living will have the energy to explore their potential and make the world a better place. Feel free to [contact me](mailto: joshuahane@gmail.com) if you think I am suitable for your position.  -->

I am looking for a job where I can keep learning the cutting eadge techniques and deliver data science solutions to real-world problems. My goal is seeking data-driven opportunities and transcending traditional disciplinary boundaries with machine learning methods. Feel free to [contact me](mailto: joshuahane@gmail.com) if you think I am suitable for your position. 


## My Research Interests

-**Machine learning techinques**: Uncertainty quantification, probabilistic machine learning, Bayesian deep learning, ensemble learning, time series forecasting, zero-inflated modeling, anomally detection, generative models, computer vision (satellite image collections), cost-sensitive learning.

-**Real-world issues**: I have experiences in water resource, sensor data, remote-sensing data, animal behavior and quantitative genetic issues. 

<i class="far fa-sticky-note"></i> **Note:** Although I have hands on these issues only, the machine learning algorithms behind can easily translate to other domains as long as the problems are clearly set up.
  {: .notice--info}
  {: .text-justify}



## Skills

-**Program:** `Python`, `R`, `SQL`.

-**Frequently used python packages:**:

  > **Deep learning:** `tensorflow`, `pytorch`.\\
  > **Computer vision:** `PIL`, `cv2`. \\
  > **Machine learning:** `hyperopt`, `Sklearn`, `XGBoost`, `lightGBM`, `numpy`, `pandas`.\\
  > **Earth data:** `earthengine`.

-**Frequently used R packages:**:

  > **Machine learning:** `caret`, `tidyverse` series.\\
  > **Statistical testing:** `LmerTest`.\\
  > **Frequentist statistical analysis:** `mgcv`, `nlm`, `lmer4`.\\
  > **Bayesian statistical analysis:** `stan`, `INLA`.


-**Others:** `slurm` (super-computer workload manager), `latex` (for writting), `jekyll` (for web design).





