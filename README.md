# Social Friction Bench — Human Baseline Survey

A survey collecting human responses to 7 social scenarios, used as a baseline for comparing human vs. AI social cognition.

## Purpose
This survey is part of the Social Friction Bench benchmark, submitted to the Google DeepMind / Kaggle "Measuring Progress Toward AGI" competition (Social Cognition track).

Responses are used to measure how humans navigate high-stakes social situations — grief, domestic violence warning signs, addiction relapse, workplace feedback, and child abuse disclosure — compared to frontier AI models.

## Dataset

Human baseline data collected via anonymous public survey at https://surveysoc.netlify.app/

N=98 (filtered from raw submissions; incomplete or invalid responses excluded to ensure scoring reliability).

## Visualizations

These visualizations summarize performance across scenarios designed to test conflicts between social comfort and structural correctness.

### Figure 1: Human Baseline Performance by Demographics

![Human Baseline Heatmap](images/social_friction_heatmap.png)

*Variation in human baseline responses across gender and education groups, highlighting differences in handling high-stakes social scenarios. Scale: 0.0–2.0.*

---

### Figure 2: Human vs. Model Performance Comparison

![Human vs Model Comparison](images/social_friction_comparison_heatmap.png)

*Comparative performance of human baseline and AI models (Claude Opus 4.6, Claude Sonnet 4.6, Gemini 2.5 Flash, Qwen 3 Next 80B, DeepSeek-R1, Gemma 3 27B) across all 7 scenarios. Higher scores indicate stronger structural alignment.*

## Files

| File | Description |
|---|---|
| `data/social_friction_bench_human_baseline_raw.xlsx` | Raw survey export (102 submissions) |
| `data/social_friction_bench_human_baseline_clean.xlsx` | Cleaned dataset (N=98, standardized demographics) |

Collection period: March 18 – April 3, 2026  
N = 98 (filtered)  
Demographics: ages 18–55+, fields including healthcare/social work, law/legal, education, and technology  
License: CC0 Public Domain