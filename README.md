# Transport-informed model for remote attribution of soil moisture variability

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17011639.svg)](https://doi.org/10.5281/zenodo.17011639)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

This repository contains the code and analysis scripts for the paper: **"Upwind terrestrial influences on soil moisture variability across South America"** (Huang et al., 2025). 

@Feini Huang (feinihuang9554@gmail.com)

We develop an observation-driven framework that integrates atmospheric moisture transport trajectories with deep learning to quantify vegetation's contribution to downwind soil moisture variability across South America.

## 📖 Overview

Soil moisture exhibits coherent spatial patterns that reflect systematic influences from upwind terrestrial conditions. This framework quantifies how vegetation dynamics in the Amazon and other regions modulate soil moisture hundreds to thousands of kilometers downwind via atmospheric moisture transport.

**Key findings:**
- Upwind information contributes **67%** to the model's predictive power
- Vegetation explains **15%** of this upwind impact
- Vegetation-mediated influence is significantly enhanced in agricultural zones
- Effects vary nonlinearly across climatic regimes (R1-R4)

## 🗂️ Repository Structure
YF-0-data-*                   Data preprocessing
  YF-0-data-SMs.ipynb          Soil moisture processing
  YF-0-data-esacci_filled_era5.ipynb    ESA CCI gap-filling
  YF-0-data-somo.ml.ipynb      SoMo.ml dataset preparation
  YF-0-data-windows_xy.ipynb   Spatial window generation
  YF-0-data_preocess.ipynb     Main preprocessing

YF-1-model-*                   Model implementations
  YF-1-model-local_only.ipynb  Baseline local model
  YF-1-model-spatial-context.ipynb    Non-directional model
  YF-1-model-transport.ipynb   Transport-informed model (main)

YF-2-source_influence.ipynb    Source influence analysis
YF-3-regime_piecewise.ipynb    Climatic regime classification

YF-4-plot-*                    Main figures
  YF-4-plot-fig2.ipynb         Source-sink structure (Fig. 2)
  YF-4-plot-fig3.ipynb         Climatic regimes (Fig. 3)
  YF-4-plot-fig4.ipynb         Additional main figures

YF-5-analysis-*                Supplementary analyses
  YF-5-analysis-cascade.ipynb      Cascading effects
  YF-5-analysis-cropland.ipynb     Cropland sensitivity
  YF-5-analysis-droughts.ipynb     Drought analysis
  YF-5-analysis-sig_asymmetry.ipynb    Asymmetry significance
  YF-5-analysis-std_*seeds.ipynb      Robustness tests
  YF-5-analysis-xai_uncertainty.ipynb    XAI uncertainty

YF-6-plot-*                    Supplementary figures (S1-S22)
  YF-6-plot--Fs14-esacci-missing.ipynb
  YF-6-plot-figs10-droughts.ipynb
  YF-6-plot-figs11-source_sink_seasons.ipynb
  YF-6-plot-figs18-uc3d.ipynb
  YF-6-plot-figs3-r2_laia.ipynb
  YF-6-plot-figs4-esacci_r2.ipynb
  YF-6-plot-figs5-wind_rainfall.ipynb
  YF-6-plot-figs6-xais_uncertainty.ipynb
  YF-6-plot-figs7-std_randomseeds.ipynb
  YF-6-plot-figs9-cropland-sensitivity-ratio.ipynb


## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- PyTorch (for deep learning models)
- Jupyter Notebook
- Key packages: numpy, pandas, xarray, matplotlib, scikit-learn, pytorch

### Installation

```bash
git clone https://github.com/hydroshub/Transport-informed-model-for-remote-attribution.git
cd Transport-informed-model-for-remote-attribution
pip install -r requirements.txt  # Create this file if needed


