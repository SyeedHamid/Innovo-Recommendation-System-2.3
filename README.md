# Epic 2.3 GA Range Recommendation System

This repository contains a modular, production-grade pipeline for optimizing plant extraction processes using machine learning. Developed as part of the Innovo Intelligent Plant Extraction Optimization System, the pipeline predicts bioactive compound yield, recommends optimal process parameters, and verifies subcritical safety conditions using historical experiment data.

## Overview

The system automates manual analysis of plant extraction experiments. It ingests CSV files containing process data (e.g., temperature, pressure, time, pH) and yield measurements, then:

- Cleans and validates the data
- Detects outliers and unsafe conditions
- Extracts high-yield parameter ranges
- Trains multioutput XGBoost models
- Recommends optimal settings per plant
- Summarizes the best-performing process

## Features

- Native multioutput modeling with XGBoost
- Temporal derivative feature engineering
- Outlier detection with flagged values
- Subcritical safety filtering via flag logic
- Per-plant recommendations with dynamic range formatting
- Batch processing across multiple plant files
- Optional testing block for diagnostics (disabled by default)


