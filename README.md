# Cluster-Wide Task Slowdown Detection in Cloud Systems

This repository contains the research and materials for **SORN**, a deep learning framework designed to detect cluster-wide malfunctions in modern cloud systems by analyzing task duration time distributions.

## Overview

Maintaining the health of cloud systems is critical for user satisfaction and avoiding financial penalties associated with Service Level Agreement (SLA) violations. Traditional monitoring methods often struggle with the scale of modern cloud environments, leading to:

* **Computational Inefficiency:** Tracking millions of tasks individually is impractical.

* **High False Alarm Rates (Noise):** Volatile virtual environments create natural fluctuations, leading to false positives when monitoring individual tasks.

## The SORN Approach

SORN (Skimming Off subperiods and Reconstructing Non-slowing fluctuation) shifts the focus from individual task tracking to **Cluster-Wide Distribution Analysis**. By summarizing how all tasks are running at any given moment, SORN provides an efficient, scalable, and noise-resistant method for anomaly detection.

### Key Technical Innovations
To handle complex system patterns, SORN utilizes three dedicated modules:

1. **Skimming Attention (SA):** Handles **Compound Periodicity** by iteratively reconstructing and separating periodic components in descending order of amplitude, ensuring subtle patterns are not ignored.
2. **Neural Optimal Transport (OT):** Filters **Non-Slowing Fluctuations** by using a custom transport cost matrix that distinguishes between beneficial task speedups and actual slowdowns, drastically reducing false alarms.
3. **Picky Loss Function:** Ensures **Robust Training** by adaptively weighting reliable, predictable data points, preventing the model from learning from contaminated historical data.

## Performance
SORN demonstrates superior accuracy (F1 score) compared to state-of-the-art methods across multiple datasets, while maintaining minimal time and memory overhead.

## Future Trajectories
The goal is to evolve from detection to a **self-healing cloud** architecture:

1. **Detection:** Identifying slowdowns using SORN.
2. **Diagnosis:** Employing Large Language Models (LLMs) for deep root cause analysis.
3. **Recovery:** Utilizing Multi-Agent Systems to initiate automatic recovery.

## View Presentation
[View Presentation]{./presentation.pdf}
