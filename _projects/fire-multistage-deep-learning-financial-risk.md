---
layout: page
title: Multi-Stage Deep Learning Framework for Wildfire Financial Risk
description: Integrating geomorphons, remote sensing fire & weather data, and neural networks to quantify downslope wind-driven fire risk for insurance and built environment
img: assets/img/3stagemodel.jpg
importance: 2
category: work
related_publications: false
---

**Multi-Stage Deep Learning Framework for Wildfire Financial Risk**

At UNC, I work with multiple undergraduate and graduate students on three wildfire projects that together build a holistic, multi-stage modeling pipeline: from hazard dynamics to financial risk.

**Wildfire footprint doesn’t equal wildfire loss.**

In the two examples below, the 2020 August Complex burns a massive area, while the 2025 Palisades fire has a much smaller footprint. Yet urban-interface fires like Palisades can drive disproportionately large economic losses because they intersect with dense, high-value assets and critical infrastructure. That mismatch (small burned area, huge financial damage) is exactly the gap our work targets.

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="lazy" path="assets/img/projects/august-complex-fire.gif" title="August Complex fire evolution" class="img-fluid rounded z-depth-1" %}
        <div class="caption">August Complex fire.</div>
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="lazy" path="assets/img/projects/palisades-fire.gif" title="Palisades fire evolution" class="img-fluid rounded z-depth-1" %}
        <div class="caption">Palisades fire.</div>
    </div>
</div>

## Why Downslope, Wind-Driven Fires Matter

One reason wildfire risk has been poorly quantified in insurance catastrophe models is the behavior of **downslope, wind-driven fires**, the most dangerous fires for the built environment. While fires typically spread uphill, strong winds can reverse this pattern. Terrain funnels and accelerates these winds through valleys and canyons toward populated areas, pushing fires rapidly into wildland–urban interface (WUI) communities and greatly increasing the risk of catastrophic damage. These fires were primarily human-ignited, occurred closer to population centers, and resulted in outsized impacts on human lives and infrastructure. Weather–topography interactions strongly shape fire spread, especially by generating complex wind patterns in valleys. However, a major bottleneck in accurate fire prediction is the **lack of high-resolution wind data**.

## Geomorphons: Terrain-Form Classification

To address this, we leverage a terrain-form classification framework from geomorphology. We adopt the landform classification approach of Jasiewicz and Stepowski, referred to as **geomorphons**. For each pixel in a digital elevation model (DEM), the algorithm evaluates whether the surrounding terrain rises, falls, or remains flat across multiple directions, and encodes this local topographic pattern into a simple landform category (e.g., ridge, valley, slope, or flat area). A complementary layer is **landform direction**, which indicates which way the terrain feature faces. This matters because terrain orientation strongly affects how wind is channeled and how fires spread—especially along valleys and ridges. These static layers are inputs to the neural network in Model 2 to improve performance. Including this information instead of raw DEM alone helps the network learn likely pathways of fire propagation when high-resolution wind data are unavailable.

## Fire Data: Capturing Hazard Dynamics at Scale

Model 2 uses VIIRS I-Band Active Fire detections (375 m spatial resolution, ~twice daily). We preprocess these detections into a fire-evolution sequence that supports spatiotemporal learning.

This dataset is particularly useful because it allows us to model fire growth consistently across events—whether they are large remote burns or fast-moving WUI intrusions—while keeping the modeling framework scalable.



## Multi-Stage Framework

Our novelty is an integrated, end-to-end framework that links:

1. Ignition and growth: a stochastic large-fire probability model + deep-learning fire propagation model

2. Topographic controls: geomorphons and landform orientation to represent wind channeling and terrain-driven spread pathways

3. Loss translation: mapping hazard and exposure into financial loss metrics for insurance and risk management

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3stagemodel.jpg" title="Multi-stage deep learning framework for wildfire financial risk" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Multi-stage framework integrating geomorphons, VIIRS fire data, and neural networks for wildfire financial risk.
</div>

## Why This Matters for Insurance and Households

Many of the costliest wildfires are not the ones that burn the most land—they’re the ones that blow into urban areas, where high-density, high-value properties concentrate losses. This class of risk remains underexplored in the research literature and has often been underestimated in catastrophe modeling, contributing to insurer stress and growing affordability challenges for households. Using a **state-of-the-art, multi-stage deep learning framework** that couples hazard dynamics, terrain-informed learning, and loss translation, we aim to better quantify downslope, wind-driven WUI fires so catastrophe models and insurers can more accurately price, manage, and mitigate wildfire financial risk.
