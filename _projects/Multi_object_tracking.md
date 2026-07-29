---
layout: page
title: Multi-Object Tracking
description: Labeled random finite set filters for multi-sensor multi-object tracking
img: assets/img/MOT/mot_hero.png
importance: 1
category: Work
---

<!--
=====================================================================
IMAGE GENERATION TASK LIST (for Gemini / image agent)
=====================================================================
Generate 6 images and save them to: assets/img/MOT/

  1. mot_hero.png      (16:9)  - page thumbnail / hero
  2. mot_problem.png   (4:3)   - the tracking problem
  3. mot_lrfs.png      (4:3)   - labeled random finite set over time
  4. mot_glmb.png      (4:3)   - GLMB Bayes recursion + hypothesis tree
  5. mot_fusion.png    (4:3)   - heterogeneous multi-sensor fusion
  6. mot_mdap.png      (4:3)   - multi-dimensional assignment / cost tensor

SHARED STYLE (apply to every image):
  Clean flat vector technical infographic, academic paper / IEEE figure
  aesthetic. Plain white background. Muted palette: deep navy #1f3a5f,
  slate grey #5b6b7c, one accent (amber #a9791b or teal #2a7f7f), light
  grey fills. Thin uniform strokes, generous white space, no gradients,
  no 3D bevels, no drop shadows, no photorealism, no stock-photo people,
  no logos or watermarks.
=====================================================================
-->



<p>Cameras, radars, lidars, sonars, and bearing-only sensors all produce a stream of detections frame after frame. <em>Multi-object tracking</em> (MOT) aims to transform these raw detection streams into joint estimates of object counts and their spatial trajectories over time.</p>

<p>Objects enter and leave scenes at unknown times, detectors produce false alarms or miss objects entirely, and detections lack object identity labels. My research addresses multi-object tracking within the <em>labeled random finite set</em> (LRFS) framework (<a href="https://ieeexplore.ieee.org/document/10704579">Vo et al., IEEE TSP 2024</a>), treating object collections as set-valued random variables under rigorous Bayesian recursion. We focus on multi-sensor fusion across heterogeneous modalities without relying on tracking-specific training data.</p>

<div class="avt2">

  <div class="avt2-head">
    <div class="eyebrow">Framework Architecture</div>
  </div>

  <!-- 01 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>01</b> Estimation Problem</div>
      <h3>Multi-Object Estimation Under Uncertainty</h3>
      <span class="en">Cardinality · Kinematic States · Identities</span>
      <p>At every time step, sensors report un-ordered detection sets containing real targets, false clutter, and missed detections. The tracker must simultaneously resolve four core sources of uncertainty: time-varying object counts, clutter alarms, missed detections, and data association ambiguity.</p>
      <p>Data association is combinatorially complex: as target and measurement counts grow, assigning detections to targets leads to hypothesis expansion. Classical trackers use greedy nearest-neighbour or probabilistic data association, whereas random finite set filters propagate full multi-object densities.</p>
    </div>
    <div class="fig-card">
       <img class="figimg" src="{{ 'assets/img/MOT/mot_problem.png' | relative_url }}" alt="The multi-object tracking problem: trajectories, detections, false alarms and missed detections">
       <div class="fig-cap">Detections, clutter, missed detections, and the trajectories to be recovered.</div>
    </div>
  </div>

  <!-- 02 -->
  <div class="sol flip">
    <div class="sol-copy">
      <div class="sol-index"><b>02</b> RFS Formulation</div>
      <h3>Objects as Labeled Random Finite Sets</h3>
      <span class="en">Random Finite Sets · Unique Labels · Trajectories</span>
      <p>The LRFS formulation models the multi-object state at each time step as a finite set of labeled kinematic states. Each element pairs kinematic variables (position, velocity) with a unique trajectory label that persists over time.</p>
      <p>By treating object count as a random variable, target births and deaths are incorporated directly into the Bayesian filtering model, eliminating ad-hoc heuristic track management.</p>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/MOT/mot_lrfs.png' | relative_url }}" alt="Labeled random finite set: a set of labeled object states evolving over time with births and deaths">
      <div class="fig-cap">A set-valued state with labels, propagated through births and deaths.</div>
    </div>
  </div>

  <!-- 03 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>03</b> Bayesian Filtering</div>
      <h3>The GLMB Family of Filters</h3>
      <span class="en">Generalized Labeled Multi-Bernoulli · Bayes Recursion</span>
      <p>The Generalized Labeled Multi-Bernoulli (GLMB) filter represents the multi-object density as a weighted mixture of label hypotheses and object spatial distributions. Crucially, the GLMB form is mathematically conjugate under prediction and measurement updates.</p>
      <p>To maintain computational tractability against exponential hypothesis growth, truncation methods prune insignificant hypotheses while preserving significant posterior components.</p>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/MOT/mot_glmb.png' | relative_url }}" alt="GLMB Bayes recursion with prediction and update, and truncation of the hypothesis tree">
      <div class="fig-cap">A closed-form recursion, kept tractable by retaining only significant hypotheses.</div>
    </div>
  </div>

  <!-- 04 -->
  <div class="sol flip">
    <div class="sol-copy">
      <div class="sol-index"><b>04</b> Multi-Sensor Fusion</div>
      <h3>Measurement-Level Multi-Sensor Fusion</h3>
      <span class="en">MS-GLMB · Heterogeneous Sensor Networks</span>
      <p>Under conditional independence, multi-sensor measurement likelihoods factorize into per-sensor terms. The Multi-Sensor GLMB (MS-GLMB) filter updates target densities using raw measurement sets from all sensors simultaneously.</p>
      <p>Fusion occurs at the measurement level inside the Bayesian update rather than combining single-sensor tracks, seamlessly accommodating heterogeneous sensors (cameras, radars, lidars) and non-overlapping fields of view.</p>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/MOT/mot_fusion.png' | relative_url }}" alt="Heterogeneous sensors fused at the measurement level by a single multi-sensor filter">
      <div class="fig-cap">Heterogeneous detections enter one filter and leave as labeled trajectories.</div>
    </div>
  </div>

  <!-- 05 -->
  <div class="sol">
    <div class="sol-copy">
      <div class="sol-index"><b>05</b> Optimization</div>
      <h3>Multi-Dimensional Data Association</h3>
      <span class="en">Multi-Dimensional Assignment Problem (MDAP) · Gibbs Sampling</span>
      <p>Truncating multi-sensor GLMB mixtures requires discovering association maps with maximal weights, framed as a Multi-Dimensional Assignment Problem (MDAP). Each target is assigned measurement indices across all sensors under feasibility constraints.</p>
      <p>To bypass NP-hard combinatorial complexity, stochastic Gibbs sampling efficiently draws high-weight association maps directly proportional to posterior component weights.</p>
    </div>
    <div class="fig-card">
      <img class="figimg" src="{{ 'assets/img/MOT/mot_mdap.png' | relative_url }}" alt="Multi-dimensional assignment: a per-sensor cost layer with one selected assignment per object">
      <div class="fig-cap">One cost layer per sensor, one feasible assignment per object across all of them.</div>
    </div>
  </div>

  <div class="pub-section">
    <h3>References</h3>
    <ol class="pub-list">
      <li>
        Ba-Ngu Vo, Ba-Tuong Vo, Tran Thien Dat Nguyen, and Changbeom Shim. <em><a class="general" href="https://ieeexplore.ieee.org/document/10704579">An Overview of Multi-Object Estimation via Labeled Random Finite Set</a></em>. <strong>IEEE Transactions on Signal Processing</strong>, 72:4888-4917, 2024.
      </li>
      <li>
        B.-T. Vo and B.-N. Vo. <em><a class="general" href="https://ieeexplore.ieee.org/document/6507656">Labeled random finite sets and multi-object conjugate priors</a></em>. <strong>IEEE Transactions on Signal Processing</strong>, 61(13):3460-3475, 2013.
      </li>
      <li>
        B.-N. Vo, B.-T. Vo, and D. Phung. <em><a class="general" href="https://ieeexplore.ieee.org/document/6928494">Labeled random finite sets and the Bayes multi-target tracking filter</a></em>. <strong>IEEE Transactions on Signal Processing</strong>, 62(24):6554-6567, 2014.
      </li>
      <li>
        B.-N. Vo, B.-T. Vo, and M. Beard. <em><a class="general" href="https://ieeexplore.ieee.org/document/8861414">Multi-sensor multi-object tracking with the generalized labeled multi-Bernoulli filter</a></em>. <strong>IEEE Transactions on Signal Processing</strong>, 67(23):5952-5967, 2019.
      </li>
    </ol>
  </div>

</div>