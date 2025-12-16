# Badminton Stroke Execution Quality Prediction
> A Simplified Machine Learning Study

## 1. Motivation

In badminton training and performance analysis, stroke quality is often evaluated qualitatively by coaches based on experience and observation.
While advanced systems may incorporate video analysis or sensor fusion, it remains unclear whether simplified, handcrafted stroke-related features alone already contain meaningful predictive signals regarding stroke execution quality.

This study aims to bridge domain knowledge in badminton training with classical machine learning methods by exploring whether basic kinematic and body control features can be used to distinguish well-executed strokes from poorly executed ones.
Rather than building a production-ready evaluation system, this work focuses on validating the feasibility and interpretability of a simplified modeling approach as a foundation for more complex future studies.

## 2. Problem Formulation

This study formulates stroke execution quality assessment as a binary classification task under controlled assumptions.

Input: Stroke-related features describing the execution of a badminton stroke, such as swing speed, racket angle, reaction time, and body balance.

Output: A binary label indicating whether the executed stroke is considered a well-executed attempt (1) or a poorly executed attempt (0).

Importantly, the target label does not represent whether the shuttlecock was physically contacted or whether a point was scored.
Instead, it serves as a proxy for execution quality, reflecting whether the stroke execution meets a simplified standard of effectiveness.

The objective of this formulation is to investigate whether these handcrafted features contain sufficient predictive information to support stroke execution quality assessment using classical machine learning models.

## 3. Scope and Assumptions

To ensure a well-defined and interpretable learning task, the scope of this study is deliberately constrained by the following assumptions:

Shuttlecock contact is assumed to have already occurred, and contact detection is outside the scope of this study.

A single stroke type (e.g., smash) is considered, avoiding confounding factors related to stroke selection.

The focus is on execution quality, rather than match outcome, scoring, or opponent response.

Temporal dependencies between consecutive strokes are not modeled; each stroke is treated as an independent instance.

Labels are treated as simplified proxies derived from predefined rules rather than ground-truth match annotations.

These assumptions allow the study to isolate the relationship between stroke-related features and execution effectiveness, providing a controlled environment for evaluating the feasibility of machine learning-based assessment.

## 4. Feature Design

The selected features are designed based on domain knowledge from badminton training and biomechanics, aiming to capture key aspects of stroke execution and body control:

Swing speed: approximates force generation and offensive intent.

Racket angle: reflects directional control and stroke mechanics.

Reaction time: represents responsiveness and timing.

Body balance: indicates stability and coordination during execution.

Shuttle height at contact: provides contextual information about stroke positioning.

These features do not directly measure impact location or sweet-spot contact, but instead act as high-level descriptors that collectively approximate stroke execution quality.