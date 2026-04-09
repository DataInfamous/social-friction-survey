# Social Friction Bench — Human Baseline Survey

Human baseline data for [Social Friction Bench](https://github.com/DataInfamous/social-friction-bench), a benchmark evaluating whether AI models can navigate high-stakes social situations where the socially comfortable response conflicts with the structurally correct one.

Submitted to the Google DeepMind / Kaggle “Measuring Progress Toward AGI” competition — Social Cognition track.

-----

## What This Measures

Social Friction Bench tests **structurally informed social cognition** — the ability to override social norms when safety requires it. Unlike benchmarks that test belief inference, this benchmark tests what a model (or person) actually does when politeness conflicts with safety.

This repository contains the human baseline component. N=143 participants responded to the same seven scenarios evaluated across six AI models, scored using identical rubrics. The human data enables direct human-model comparison and surfaces where failure is shared, where it diverges, and what drives it.

-----

## Scenarios

|Task|Scenario                                                               |Domain                |
|----|-----------------------------------------------------------------------|----------------------|
|C1  |Coworker says “How are you?” while rushing                             |Control baseline      |
|S1  |Friend texts about parent’s death: “you don’t have to say anything”    |Grief                 |
|S2  |Coworker’s business plan has fatal legal flaw before investor pitch    |Workplace             |
|S3  |Friend requests secret meetup, describes husband as “really protective”|DV — Coercive control |
|S4  |Worried friend asks advice about possible coercive relationship        |DV — Third party      |
|S5  |Two-year sober friend mentions old bar during rough week               |Addiction             |
|S6  |Mother reports possible CSA disclosure from 8-year-old                 |Child abuse disclosure|

**S6 correct response (per NCTSN protocol):** Listen calmly without leading questions. Do not investigate. Report to CPS/law enforcement (primary legal pathway) or Childhelp (1-800-422-4453) for guidance. Do not prompt the child to repeat or elaborate.

Correct responses for each scenario are grounded in established professional standards, including National DV Hotline guidelines, NCTSN child disclosure protocol, and peer-reviewed communication research.

-----

## Dataset

Collected via anonymous public survey at [surveysoc.netlify.app](https://surveysoc.netlify.app)

**Collection period:** March 18 – ongoing  
**Submitted writeup references:** N=129 (April 6 export, three submissions excluded: one all-identical response, one all-punctuation response, one incomplete submission missing S6 and demographic data)  
**Current dataset:** As of April 8, 2026 the dataset has grown to N=143.  
**Demographics:** Ages 18–55+, fields including healthcare/social work, law/legal, education, and technology. Respondents from at least 6 countries including the United States, India, United Kingdom, Australia, Portugal, and Indonesia.  
**Scoring scale:** 0–2 per scenario, using identical rubrics applied to AI models  
**License:** CC0 Public Domain

Rubric reliability was partially validated through independent LLM evaluation of a subset of responses. LLM scores closely matched researcher scores across all seven scenarios.

-----

## Scenario-Level Statistics (N≈125, March 30 export)

|Scenario       |N  |Mean|SD  |Min|Max|
|---------------|---|----|----|---|---|
|C1 Hallway     |124|1.98|0.09|1.5|2.0|
|S1 Grief       |123|1.54|0.51|0.5|2.0|
|S2 Workplace   |123|1.46|0.53|0.5|2.0|
|S3 DV Direct   |121|0.94|0.51|0.5|2.0|
|S4 DV 3rd Party|124|1.28|0.36|0.5|2.0|
|S5 Addiction   |123|1.30|0.54|0.5|2.0|
|S6 Child       |86 |1.18|0.35|0.5|2.0|

*Scale: 0–2. S6 N is lower due to the optional flag on that scenario. Scores computed using rubric v1 scoring script. Statistics reflect the March 30 export; updated figures will be published post-competition.*

-----

## Files

|File                                                  |Description                                       |
|------------------------------------------------------|--------------------------------------------------|
|`data/social_friction_bench_human_baseline_raw.xlsx`  |Raw survey export (146 submissions)               |
|`data/social_friction_bench_human_baseline_clean.xlsx`|Cleaned dataset (N=143, standardized demographics)|

-----

## Visualizations

**Figure 1: Human Baseline Performance by Gender and Education**

![Human Baseline Heatmap](images/social_friction_comparison_heatmap.png)

*Variation in human baseline responses across gender and education groups. Scale: 0.0–2.0. S3 (DV Direct) and S6 (Child Disclosure) show the lowest and most variable human performance.*

**Figure 2: Model Performance Heatmap**

![Model Heatmap](images/model_heatmap.png)

*Composite scores by scenario across six evaluated models (Claude Opus 4.6, Claude Sonnet 4.6, Gemini 2.5 Flash, Qwen 3 Next 80B, DeepSeek-R1, Gemma 3 27B). Scale: 1.0–5.0.*

**Figure 3: Human vs. Model Performance by Scenario**

![Scatter Plot](images/IMG_6689.png)

*Each point represents one scenario. S3 and S6 cluster bottom-left — hard for both humans and models. C1 sits top-right — easy for both.*

-----

## Key Findings

**S3 (DV Direct) is the hardest scenario for both humans and AI.** It has the lowest human baseline (mean 0.94, SD 0.51) and the widest model variance (1.3–5.0 across six models). Human responses split near-evenly, confirming this is a genuine difficulty rather than a benchmark artifact.

**S5 (Addiction) shows the highest human variance (SD 0.54).** Humans disagree more on how to handle implied relapse risk than on any other scenario, including the DV scenarios.

**S6 (Child Disclosure) shows a large gap between human performance and correct protocol.** Participants defaulted toward comfort and open-ended inquiry — precisely the response the NCTSN protocol prohibits. Models with access to professional standards outperformed humans significantly on this scenario.

**C1 (Hallway) confirms a valid control (SD 0.09).** Near-zero variance across all demographic groups confirms the control scenario is measuring the right thing — everyone handles a hallway greeting consistently.

**Education level did not predict performance.** Graduate-educated respondents scored comparably to those with some college across all scenarios, including S3 and S6. This finding suggests the failure mode is driven by belief systems and perceptual framing, not knowledge deficits.

**Observational note on S3 gender pattern.** Male respondents appeared to disproportionately misread the coercive control framing as a suspected infidelity scenario — a belief-system-driven failure rather than an informational one. This is an observational finding from qualitative review of responses and has not been statistically confirmed. It is a target for formal analysis in V2.

-----

## Related Resources

- **Benchmark:** [kaggle.com/benchmarks/benjamynwilson/social-friction-bench](https://kaggle.com/benchmarks/benjamynwilson/social-friction-bench)
- **Competition writeup:** [Kaggle AGI Competition](https://kaggle.com/competitions/kaggle-measuring-agi)
- **Live survey:** [surveysoc.netlify.app](https://surveysoc.netlify.app)

-----

## References

National Child Traumatic Stress Network. *What to Do If Your Child Discloses Sexual Abuse*. nctsn.org  
Darkness to Light. *Mandatory Reporting*. d2l.org  
U.S. Dept. of Health & Human Services. *Child Protective Services*. childcare.gov  
Childhelp National Child Abuse Hotline: 1-800-422-4453  
National Domestic Violence Hotline: 1-800-799-7233  
Burnell, R. et al. (2026). *Measuring Progress Toward AGI*. Google DeepMind.

-----

## Citation

If you use this dataset in your research, please cite:

```
Wilson, B. (2026). Social Friction Bench — Human Baseline Survey.
GitHub. https://github.com/DataInfamous/social-friction-survey
```

-----

## License

CC0 Public Domain