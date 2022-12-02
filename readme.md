# A Challenge Set to Evaluate Robustness of Machine Translation Automatic Metrics for WMT22 Metrics Shared Task

### Test Set Description

This test set is submitted to the WMT22 Metrics Shared Task - Challenge Sets Subtask (https://wmt-metrics-task.github.io/subtasks/challenge/) for evaluating the robustness of MT automatic metrics. 

Our test set has 721 test cases and focuses on five categories of errors: (1) number; (2) date & time (D/T); (3) named-entity & terminology (NE&Term); (4) unit; and (5) affirmation/negation (AFF/NEG). 

| Phenomenon           | Flores | WMT  | Overall |
| -------------------- | ------ | ---- | ------- |
| Number               | 183    | 172  | 355     |
| Date & Time          | 50     | 90   | 140     |
| Ne & Terminology     | 68     | 42   | 110     |
| Unit                 | 23     | 35   | 58      |
| Affirmation/Negation | 58     | 0    | 58      |
| Overall              | 382    | 339  | 721     |

Each case contains a source text, a reference, a good translation, an incorrect translation, a language phenomena label and a source of origin label indicating where the sentence comes from. The following is a case example:

| Lable                 | Text                                                         |
| --------------------- | ------------------------------------------------------------ |
| Source                | 在已知的大约24,000 块坠落至地球的陨石中，经核实只有**34** 块是来自火星。 |
| Good Translation      | Of the roughly 24,000 meteorites known to have fallen to Earth, only **thirty-four** have been confirmed to have come from Mars. |
| Incorrect Translation | Of the roughly 24,000 meteorites known to have fallen to Earth, only **30** have been confirmed to have come from Mars. |
| Reference             | Out of the approximately 24,000 known meteorites to have fallen to Earth, only about **34** have been verified to be martian in origin. |
| Phenomenon            | Number (Different Format)                                    |
| Source of the case    | Flores                                                       |



### How To Use

In general, Kendall’s tau-like correlation (Freitag et al., 2021) is used to evaluate metric performance. A good
translation has higher quality than the corresponding bad one, so a good metric should assign a higher score to the good translation. If a metric does so, we label the metric "Concordant" on the case, and "Discordant" vice versa. The correlation is calculated based on the following formula:
$$
\tau = \frac{Corconrdant - Discordant}{Concordant + Discordant}
$$


### Credit

If you use this data, please cite the following paper: 

