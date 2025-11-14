---
layout: page
title: Green Bond and Carbon Emissions
description: Evaluating the causal impact of municipal green bonds on local carbon emissions using causal machine learning
img: assets/img/publication_preview/green_bond_cover.png
importance: 2
category: work
related_publications: true
---

**Green Bond Issuance and Carbon Emissions: A Causal Machine Learning Assessment**

**Citation:** Li & Adriaens (2025), Environmental Science & Technology

This study evaluates whether U.S. municipal green bonds issued between 2009 and 2019 actually reduce local carbon emissions, and how those effects vary across regions and economic conditions. Using a causal forest model embedded within a double machine learning framework, we estimate how changes in green bond issuance influence county-level CO₂ emissions over time.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/keytrend.png" title="Key trends in green bond issuance and carbon emissions" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Key Findings

### 1. Green bonds lead to measurable emission reductions

We detect statistically significant CO₂ reductions in the 1–3 years following issuance. Effects grow over time, consistent with delays in infrastructure project completion.

- A 1% increase in issuance volume results in roughly a 0.039% reduction in emissions two years later.
- Estimated abatement cost: ~$192 per ton CO₂, demonstrating competitive cost-effectiveness relative to many mitigation pathways.

### 2. Impacts vary widely across counties

Green bond effectiveness is highly spatially heterogeneous.

- Counties with more small and medium enterprises, lower payroll per employee, and smaller establishment sizes show the largest reductions.
- These areas may depend more on public financing to implement carbon-reducing projects.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/feature.png" title="Feature analysis of green bond effectiveness" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### 3. Certified vs. self-labeled green bonds show similar outcomes

Third-party certification does not consistently increase emission reductions in municipal markets, although the certified sample is small.

### 4. First-time issuers also benefit, but with more variability

Counties issuing their first green bond experience average emission reductions, though estimates are less precise due to selection patterns and wider heterogeneity.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/firsttimeissue.png" title="First-time issuer analysis" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### 5. Forward-looking policy implications

The causal ML structure allows projecting future emission impacts under changing socioeconomic conditions (e.g., payroll growth, urbanization, industrial structure). This provides a pathway for scenario-based planning and prioritizing counties where green finance yields the greatest environmental return.

## Why It Matters

Municipal green bonds are expanding rapidly as cities seek climate finance solutions. This study provides the strongest evidence to date that:

- Green municipal bonds can reduce carbon emissions,
- Those benefits are uneven, and
- Targeted issuance strategies can improve outcomes.

These insights support policymakers, local governments, and investors who are designing next-generation climate finance strategies.

