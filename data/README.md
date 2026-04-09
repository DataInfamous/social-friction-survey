# Social Friction Bench — Dataset

## Files

|File                                             |Rows|Description                       |
|-------------------------------------------------|----|----------------------------------|
|`social_friction_bench_human_baseline_raw.xlsx`  |146 |Raw Formspree export              |
|`social_friction_bench_human_baseline_clean.xlsx`|143 |Cleaned, standardized demographics|
|`social_friction_bench_human_baseline_v2.csv`    |143 |CSV version for analysis          |

## Columns

|Column               |Type       |Description                                   |
|---------------------|-----------|----------------------------------------------|
|`_date`              |datetime   |Submission timestamp                          |
|`C1_hallway`         |text       |Response to hallway greeting (control)        |
|`S1_grief`           |text       |Response to grief notification                |
|`S2_workplace`       |text       |Response to business plan with legal flaw     |
|`S3_dv_direct`       |text       |Response to implied DV situation (direct)     |
|`S4_dv_third_party`  |text       |Response to implied DV situation (third party)|
|`S5_addiction`       |text       |Response to implied addiction relapse signal  |
|`S6_child_disclosure`|text       |Response to child abuse disclosure            |
|`age`                |categorical|Respondent age range                          |
|`education`          |categorical|Highest education level                       |
|`field`              |categorical|Professional field                            |
|`gender`             |categorical|Gender identity                               |
|`reflection`         |text       |Optional self-reflection on responses         |
|`response_source`    |categorical|organic / surveyswap                          |

## Collection

- Survey: surveysoc.netlify.app
- Period: March 18 – ongoing
- Submitted writeup references N=129 (April 6 export, three submissions excluded)
- Current N = 143 (April 8, 2026)
- Anonymous, voluntary participation