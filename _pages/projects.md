---
layout: single # splash
title: "Projects"
permalink: /projects/
# collection: projects
header:
    overlay_image: /assets/images/projheader.jpg
    # caption: "Photo by [Joel Filipe](https://unsplash.com/@joelfilip) on [Unsplash](https://unsplash.com)"
    # actions: 
      # - label: "Github"
      # - url: "https://github.com/EHanML"
author_profile: true
classes: wide


feature_row1-1:
  - image_path: assets/images/projects/wuprojimg.png # 16:9
    alt: "Retention Rates"
    title: "A Probabilistic Ensemble Scheme: Machine Learning-Based Uncertainty Quantification of Urban Water Demand Forecasts"
    text: "This project emphasis on exploring and developing the machine learning-based uncertainty quantification techniques. We propose a probabilistic ensemble scheme that successfully improve the predictive distribution from all individual models. The resulting model may contribute the development of the  smart city. "
    url: "/proj_wu/"
    btn_label: "Learn more"
    btn_class: "btn--success" # btn--warning btn--dange btn--info btn--primary
    # url2: "https://github.com/EHanML/Uncertainty_aware_ensemble_ML"
    # btn_label2: "Code"
    # btn_class: "btn--primary"
    tags: 
        - Uncertainty quantification
        - Bayesian Neural Network
        - Time series
        - LSTM
        - Ensemble
        - Water demand


feature_row1-2:
  - image_path: /assets/images/projects/CC.png
    alt: "ZI"
    title: "Deep hurdle: a new way for deep learning-based precipitation merging studies"
    text: "We propose a novel objective for machine-learning based precipitation merging studies."
    url: "/proj_wu/"
    btn_label: "Learn more"
    btn_class: "btn--success"
    tags: 
    - Satelite image 
    - Deep learning 
    - Precipitation merging study
    - FCNN
    - U-net
    - Zero-inflation 
    

feature_row1-3:
  - image_path: /assets/images/projects/xgb_map.png
    alt: "binary"
    title: "Improving remote sensing predictions of precipitation events using weather stations data with machine learning"
    text: "Our best-performing model had a remarkable improvement from the GPM product. We designed ML models to track the information flow, which can help us understand the spatial and temporal patterns of the precipitation with gridded data (i.e. satelite images)."
    url: "/proj_wu/"
    btn_label: "Learn more"
    btn_class: "btn--success"
    tags: 
    - Spatio-temporal
    - Remote sensing 
    - XGboost
    - Precipitation
    



---



## Selected Projects


&nbsp;
{% include feature_row id="feature_row1-1" type="left" %}
<a name="Water demands"></a> 
{% include feature_row id="feature_row1-2" type="left" %}
<a name="Precipitation events"></a> 
{% include feature_row id="feature_row1-3" type="left" %}
<a name="Precipitation events"></a> 


