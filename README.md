# Predictive Maintenance via Deep Representation Learning

This repository contains a deep learning approach to predicting the Remaining Useful Life (RUL) of industrial turbofan engines utilizing the NASA C-MAPSS dataset.

---

Unplanned downtime is a major financial drain in manufacturing and aviation. This project aims to transition equipment maintenance from reactive to preventative by forecasting mechanical failure before it occurs.

While traditional approaches to this dataset rely heavily on manual feature engineering (e.g., rolling means and standard deviations) to smooth high-frequency sensor noise, this project demonstrates the efficacy of deep representation learning. By implementing a Stacked Sequence-to-Sequence GRU Autoencoder coupled with a custom Temporal Attention mechanism, the primary model successfully learns to filter noise and extract the underlying degradation manifold directly from raw, unedited sensor telemetry.

## Key Achievements:

- Eliminated the need for real-time feature engineering pipelines in production.
- Outperformed a 51-feature baseline LSTM utilizing only 17 raw sensor channels.
- Evaluated using the asymmetric NASA Scoring Function to heavily penalize late predictions, aligning the model with real-world, safety-critical industrial constraints.

## Technologies Used:
* **Language:** Python
* **Deep Learning:** TensorFlow, Keras
* **Data Manipulation:** Pandas, NumPy
* **Evaluation & Metrics:** Scikit-Learn
* **Visualization:** Matplotlib

## Roadmap

This repository is being expanded beyond the original academic submission into a modularized research and engineering project focused on:

- Architecture experimentation
- Reproducibility
- Scalable preprocessing pipelines
- Production-oriented sequence forecasting workflows

It will be modularized with:

- Config-driven data pipeline
- Separate modules for preprocessing, feature engineering, modeling, and evaluation
- Experiment tracking (Weights & Biases / MLflow ready)
- Reproducible training scripts

## Dataset

A. Saxena and K. Goebel (2008). "Turbofan Engine Degradation Simulation Data Set", NASA Prognostics Data Repository, NASA Ames Research Center, Moffett Field, CA

Link: <a href="https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/">NASA C-MAPSS-1 Turbofan Engine Degradation Dataset</a>

---

**Author:** Kyle Honke  
**License**: MIT  
**Status:** Actively modularizing for production-grade structure  
**Last Updated:** 05/11/2026