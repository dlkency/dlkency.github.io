---
layout: page
title: Multi-Stage Deep Learning Framework for Wildfire Financial Risk
description: Integrating geomorphons, VIIRS fire data, and neural networks to quantify downslope wind-driven fire risk for insurance and built environment
img: assets/img/3stagemodel.jpg
importance: 2
category: work
related_publications: false
---

**Multi-Stage Deep Learning Framework for Wildfire Financial Risk**

I work with multiple undergraduate and graduate students at UNC on three wildfire projects that integrate this holistic modeling approach.

## Why Downslope, Wind-Driven Fires Matter

One reason wildfire risk has been poorly quantified in insurance catastrophe models is the behavior of **downslope, wind-driven fires**—the most dangerous fires for the built environment. While fires typically spread uphill, strong winds can reverse this pattern. Terrain funnels and accelerates these winds through valleys and canyons toward populated areas, pushing fires rapidly into wildland–urban interface (WUI) communities and greatly increasing the risk of catastrophic damage. These fires were primarily human-ignited, occurred closer to population centers, and resulted in outsized impacts on human lives and infrastructure. Weather–topography interactions strongly shape fire spread, especially by generating complex wind patterns in valleys. However, a major bottleneck in accurate fire prediction is the **lack of high-resolution wind data**.

## Geomorphons: Terrain-Form Classification

To address this, we leverage a terrain-form classification framework from geomorphology. We adopt the landform classification approach of Jasiewicz and Stepowski, referred to as **geomorphons**. For each pixel in a digital elevation model (DEM), the algorithm evaluates whether the surrounding terrain rises, falls, or remains flat across multiple directions, and encodes this local topographic pattern into a simple landform category (e.g., ridge, valley, slope, or flat area). A complementary layer is **landform direction**, which indicates which way the terrain feature faces. This matters because terrain orientation strongly affects how wind is channeled and how fires spread—especially along valleys and ridges. These static layers are inputs to the neural network in Model 2 to improve performance. Including this information instead of raw DEM alone helps the network learn likely pathways of fire propagation when high-resolution wind data are unavailable.

## Fire Data and Urban–Wildfire Contrast

Model 2 uses fire data from **VIIRS I-Band Active Fire** (375 m spatial resolution, half-day temporal resolution). From the preprocessed fire-evolving process we know that fires in urban areas and wildfires behave quite differently—as illustrated by contrasts between events such as the August Complex and the Palisades fire.

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

## Multi-Stage Framework

Our novelty lies in integrating all three components—terrain-informed fire spread modeling, VIIRS-based fire evolution, and financial risk quantification—into a **unified multi-stage framework** for risk management and insurance.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3stagemodel.jpg" title="Multi-stage deep learning framework for wildfire financial risk" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Multi-stage framework integrating geomorphons, VIIRS fire data, and neural networks for wildfire financial risk.
</div>

## Why This Matters for Insurance and Households

Many of the costliest wildfires on record are those that blow into urban areas with high-density, high-value properties. This class of risk has been understudied in the literature and underestimated by the insurance industry, contributing to industry stress and affordability issues for households. Our framework aims to improve quantification of these downslope, wind-driven fire events so that catastrophe models and insurers can better price and manage wildfire risk in the WUI.
