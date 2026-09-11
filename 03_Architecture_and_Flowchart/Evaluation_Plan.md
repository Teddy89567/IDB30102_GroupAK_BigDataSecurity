# Evaluation Plan

This section explains how the three cases are compared in this research.

## What is Measured

The evaluation looks at three main results:

- Accuracy (%)
- Re-identification Risk (%)
- Execution Time (milliseconds)

These results are used to compare the original dataset with k-Anonymity and Differential Privacy.

## Baseline

The original UCI Adult dataset is used as the baseline. No privacy technique is applied to the baseline.

The results are also compared with the findings from Anoop et al. (2025).

## Dataset and Test Environment

The UCI Adult Census Income dataset is used for the experiment.

The dataset is processed locally using the custom Python script `anonymization_framework.py`.

Two privacy-preserving techniques are tested:

- k-Anonymity (`k = 3`)
- Differential Privacy (`ε = 1.0`)

## Evaluation Metrics

| Metric | Purpose |
|---|---|
| Accuracy (%) | Shows how well the data can still be used |
| Re-identification Risk (%) | Shows the risk of identifying an individual |
| Execution Time (ms) | Shows the time needed to process the data |

## Summary of Results

The preliminary results from the sample input dataset are shown below.

| Technique / Treatment | Accuracy (%) | Re-ID Risk (%) | Execution Time (ms) |
|---|---:|---:|---:|
| Baseline (Raw Data) | 33.33% | 100.00% | 285.66 ms |
| k-Anonymity (`k = 3`) | 33.33% | 60.00% | 114.34 ms |
| Differential Privacy (`ε = 1.0`) | 33.33% | 90.00% | 110.57 ms |

## Preliminary Observation

From the preliminary results, all three cases have the same accuracy of 33.33%.

The re-identification risk is lower after applying both privacy techniques. k-Anonymity gives a lower re-identification risk of 60.00%, while Differential Privacy gives 90.00%.

The execution time is also lower for both privacy techniques compared with the raw dataset in this sample test. Differential Privacy has the shortest execution time at 110.57 ms.

These are preliminary results from the sample input dataset. Further testing can be carried out to confirm the results.
