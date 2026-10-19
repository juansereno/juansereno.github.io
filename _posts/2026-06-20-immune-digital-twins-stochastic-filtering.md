---
layout: post
title: "Inferring parameters in immune digital twins when the immune system will not sit still"
date: 2026-06-20
tags:
  - digital twins
  - adaptive filtering
  - immunology
---

_Draft notes from my June 2026 talk at Washington State University. [Slides here](/assets/pdf/slides/WNAR26_slides.pdf)._

The digital twin paradigm rests on three things: a mechanistic software replica of the object, longitudinal data specific to that object, and an inference framework that keeps updating the model as the data arrives. For engineering systems this is hard but tractable. For the immune system it is harder, because the thing you are trying to track is genuinely stochastic — not merely noisily measured.

That distinction matters more than it sounds. If the variability were measurement noise, a well-tuned deterministic estimator would average it away. It is not. The response itself fluctuates, so the parameters you are estimating are moving targets, and an estimator that assumes otherwise will happily converge to a confident wrong answer.

The framework I presented treats the inference step with stochastic adaptive filters instead, so parameter estimates carry uncertainty that reflects the underlying biological variability rather than just the sensor.

**To expand:** worked example on the HIV model, comparison against batch identification, and what the uncertainty bounds actually mean for a clinician reading them.
