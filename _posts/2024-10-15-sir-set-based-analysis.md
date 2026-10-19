---
layout: post
title: 'What set-based analysis tells you about epidemic interventions'
date: 2024-10-15
tags:
  - epidemics
  - MPC
  - invariant sets
---

*Draft notes from my October 2024 colloquium at the University of Idaho. [Slides here](/assets/pdf/slides/Colloquium_Mat-Stat_24_VF4.pdf).*

Most control formulations of epidemic intervention optimize a single scalar: flatten the peak, or minimize total infections. In practice a public health authority is holding two constraints at once — keep the infected peak prevalence below whatever the hospital system can absorb, *and* keep the epidemic final size down — while the intervention itself carries a cost that grows the longer it runs.

A set-based dynamic analysis of SIR-type systems makes the trade-off visible rather than implicit. Instead of asking "what is the optimal control signal," you ask which regions of state space can still reach an acceptable outcome, and what a finite-duration intervention does to that region.

The practical payoff is that finite-time social distancing measures — the only kind anyone actually implements — can be placed rather than merely sized. Timing turns out to matter as much as intensity.

**To expand:** the invariant set construction, and how this fed into the switched NMPC formulation in the Annual Reviews in Control paper.
