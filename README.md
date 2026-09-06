# Step 14 — Calculate Effect Sizes

## Maya’s Evidence Synthesis Journey

### From Reported Results to a Common Metric

Maya has now prepared the data for analysis.

She started with **111 eligible studies** in her systematic review.

After examining the available quantitative information, she identified **22 studies** that could contribute to the planned meta-analysis.

Now she has another question.

> **Maya:** “The 22 studies report their results in different ways. Some give means and standard deviations. Others might report a *t* statistic, confidence interval, or another statistic. How can I combine all of these results?”

Her mentor smiles.

> **Mentor:** “That is exactly why we calculate effect sizes.”

> **Maya:** “So the effect size puts the results on a common scale?”

> **Mentor:** “Exactly. We transform the statistical results reported by each study into an effect-size metric that can be compared and, when appropriate, combined.”

Maya opens her dataset.

> **Maya:** “So I calculate one effect size for every study?”

> **Mentor:** “Not necessarily. A single study can report several outcomes, time points, or comparisons. So you may calculate several effect sizes from one study.”

> **Maya:** “Then I need to keep track of which effect size belongs to which study and outcome.”

> **Mentor:** “Exactly. Your Study ID and Outcome ID become very important.”

---

# 1. What Is an Effect Size?

An **effect size** is a numerical representation of the magnitude and direction of a relationship, difference, or intervention effect.

In a meta-analysis, effect sizes allow results from different studies to be expressed in a comparable form.

For example:

| Study | Intervention Mean | Control Mean | Result              |
| ----- | ----------------: | -----------: | ------------------- |
| S001  |              82.4 |         76.8 | Intervention higher |
| S002  |              85.1 |         79.3 | Intervention higher |
| S003  |              78.5 |         72.3 | Intervention higher |

The raw means cannot necessarily be combined directly because studies may use different scales.

For example:

* Study A may use a 0–100 test.
* Study B may use a 0–50 test.
* Study C may use a 1–5 rating scale.

Effect-size calculation helps express these findings in a common metric.

---

# 2. Why Can't Maya Just Compare the Means?

Maya asks:

> **Maya:** “If the intervention group has a higher mean than the control group, why don't I just compare the means?”

Her mentor explains:

> **Mentor:** “Because the difference between means depends on the measurement scale.”

Suppose two studies report:

| Study | Intervention | Control | Mean Difference |
| ----- | -----------: | ------: | --------------: |
| A     |           82 |      76 |               6 |
| B     |           42 |      36 |               6 |

Both have a mean difference of 6.

But suppose Study A uses a 100-point test and Study B uses a 50-point test.

A difference of 6 points does not necessarily represent the same magnitude of effect.

This is one reason standardized effect sizes can be useful.

---

# 3. The First Question: What Type of Outcome Do We Have?

Before calculating an effect size, Maya needs to understand the outcome.

Different types of outcomes require different effect-size approaches.

| Outcome type    | Example                         | Possible effect-size family                    |
| --------------- | ------------------------------- | ---------------------------------------------- |
| Continuous      | Test score                      | Mean difference / standardized mean difference |
| Binary          | Passed vs. did not pass         | Risk ratio / odds ratio                        |
| Correlation     | Relationship between variables  | Correlation-based effect size                  |
| Time-to-event   | Time until an event             | Hazard ratio                                   |
| Proportion/rate | Percentage achieving an outcome | Proportion-based methods                       |

For Maya's AI-learning example, the primary outcomes are continuous learning outcomes such as:

* achievement
* knowledge
* skill
* performance

Therefore, a mean-based effect size is often appropriate when the required information is available.

---

# 4. Mean Difference

Maya begins with the simplest example.

If two studies use the **same outcome scale**, she may use a **mean difference (MD)**.

The basic formula is:

**MD = Mean Intervention − Mean Control**

For S001:

* Intervention mean = 82.4
* Control mean = 76.8

Therefore:

**MD = 82.4 − 76.8 = 5.6**

So the intervention group scored **5.6 points higher** than the control group.

---

# 5. When Is Mean Difference Appropriate?

Mean difference is particularly useful when studies measure an outcome using the **same scale or a directly comparable scale**.

For example:

| Study | Measurement            | Intervention | Control |
| ----- | ---------------------- | -----------: | ------: |
| S001  | 0–100 achievement test |         82.4 |    76.8 |
| S002  | 0–100 achievement test |         85.1 |    79.3 |
| S003  | 0–100 achievement test |         78.5 |    72.3 |

Because the measurement scale is comparable, the mean differences can be interpreted in the original units.

---

# 6. Standardized Mean Difference

Maya asks:

> **Maya:** “What happens if the studies measure the same outcome using different scales?”

Her mentor explains:

> **Mentor:** “Then a standardized mean difference can be useful.”

The **standardized mean difference (SMD)** expresses the difference between groups relative to the variability of the outcome.

A common form is:

**SMD = (Mean Intervention − Mean Control) / Pooled SD**

For small-sample bias correction, a corrected standardized effect such as **Hedges' g** can be used.

---

# 7. Why Hedges' g?

Maya notices that many educational meta-analyses use Hedges' g.

> **Maya:** “Why not just use Cohen's d?”

Her mentor explains:

> **Mentor:** “Cohen's d is a standardized mean difference. Hedges' g applies a small-sample correction that can reduce bias in estimated standardized effects, particularly when sample sizes are small.”

For this project, Maya decides that **Hedges' g** will be the primary standardized mean difference metric.

The exact effect-size choice should be specified in the protocol and applied consistently.

---

# 8. Example: Calculating Hedges' g

Consider S001:

| Statistic | Intervention | Control |
| --------- | -----------: | ------: |
| n         |           60 |      60 |
| Mean      |         82.4 |    76.8 |
| SD        |          8.6 |     9.1 |

First calculate the mean difference:

**82.4 − 76.8 = 5.6**

Then calculate the pooled standard deviation.

The pooled SD is approximately:

**8.85**

The uncorrected standardized mean difference is therefore approximately:

**d = 5.6 / 8.85 ≈ 0.63**

After applying the small-sample correction, Hedges' g is approximately:

**g ≈ 0.62**

The important point is not simply the number.

Maya needs to understand the process:

**Means + SDs + sample sizes**
↓
**Standardized mean difference**
↓
**Small-sample correction**
↓
**Hedges' g**

---

# 9. The Direction of the Effect

Maya asks another important question.

> **Maya:** “What if one study reports higher scores as better, but another outcome is coded in the opposite direction?”

Her mentor responds:

> **Mentor:** “Then you need to make sure the direction of the effect is consistent before synthesis.”

Suppose:

**Positive effect = AI intervention improves learning**

Maya should code the effect sizes so that positive values consistently represent improvement in learning, if that is the direction specified in the protocol.

For example:

| Study | Raw interpretation                | Standardized direction         |
| ----- | --------------------------------- | ------------------------------ |
| S001  | Intervention > Control            | Positive                       |
| S002  | Intervention > Control            | Positive                       |
| S003  | Higher score = better learning    | Positive                       |
| S004  | Higher score = poorer performance | Reverse-coded before synthesis |

The important principle is:

> **Effect-size direction must be defined before analysis and applied consistently.**

---

# 10. What If the Study Reports Something Other Than Mean and SD?

Maya looks at the remaining studies.

> **Maya:** “Not every paper reports Mean and SD.”

> **Mentor:** “That's common. You may still be able to calculate an effect size.”

Studies may report statistics such as:

* standard error
* confidence interval
* *t* statistic
* *F* statistic
* *p* value
* correlation
* odds ratio
* regression coefficient

Depending on the effect-size metric and information available, some of these statistics can be converted into an effect size.

---

# 11. Example: Confidence Interval

Suppose a study reports:

**Mean difference = 5.6**

and a 95% confidence interval:

**[2.1, 9.1]**

Maya may be able to derive the standard error from the confidence interval and use that information in effect-size calculations, depending on the planned effect-size method.

The important lesson is:

> **Do not assume that a study is unusable simply because Mean and SD are not reported.**

Check whether another reported statistic provides enough information to calculate the planned effect size.

---

# 12. What If the Study Reports a *t* Statistic?

Suppose a study reports:

**t = 2.75**

along with the relevant sample sizes.

Maya may be able to convert the reported statistic into a standardized effect size.

Again, the exact conversion depends on:

* study design
* statistic reported
* degrees of freedom
* sample sizes
* effect-size metric being used

Therefore, Maya records the original statistic before conversion.

---

# 13. Always Preserve the Original Data

Maya asks:

> **Maya:** “If I convert everything into Hedges' g, can I just keep the effect size?”

> **Mentor:** “No. Keep the original information too.”

Her dataset should preserve:

| Study ID | Outcome ID | n I | Mean I | SD I | n C | Mean C | SD C | Original statistic | Effect size |
| -------- | ---------- | --: | -----: | ---: | --: | -----: | ---: | ------------------ | ----------: |
| S001     | S001-O1    |  60 |   82.4 |  8.6 |  60 |   76.8 |  9.1 | Mean/SD            |           g |
| S002     | S002-O1    |  75 |   85.1 |  9.2 |  74 |   79.3 | 10.1 | Mean/SD            |           g |
| S003     | S003-O1    |  48 |   78.5 | 10.1 |  48 |   72.3 |  9.8 | Mean/SD            |           g |

This creates a transparent chain:

**Published result → extracted statistic → calculation → effect size**

---

# 14. One Study Can Produce Multiple Effect Sizes

Maya initially thinks there should be one effect size per study.

Her mentor corrects the workflow:

> **Mentor:** “A study can provide several outcomes.”

For example, S001 might report:

| Study ID | Outcome ID | Outcome     | Effect size |
| -------- | ---------- | ----------- | ----------: |
| S001     | O1         | Achievement |        0.62 |
| S001     | O2         | Knowledge   |        0.48 |
| S001     | O3         | Skill       |        0.71 |

These are **three effect sizes from the same study**.

Maya therefore needs both:

**Study ID**
and
**Outcome ID**

This becomes especially important later when she conducts the meta-analysis because multiple effects from the same study may not be statistically independent.

---

# 15. One Study Can Also Have Multiple Time Points

A study may measure students:

* immediately after the intervention
* one month later
* three months later

For example:

| Study | Time point        | Effect size |
| ----- | ----------------- | ----------: |
| S005  | Post-test         |        0.58 |
| S005  | 1-month follow-up |        0.51 |
| S005  | 3-month follow-up |        0.43 |

Maya should not automatically treat these as three independent studies.

They are multiple observations from the **same study**.

The protocol should specify how multiple time points will be handled.

---

# 16. Effect Size and Its Variance

Maya calculates Hedges' g.

But her mentor stops her.

> **Mentor:** “There is one more number you need.”

> **Maya:** “The variance?”

> **Mentor:** “Exactly.”

For meta-analysis, Maya generally needs both:

1. **Effect size**
2. **Variance of the effect size** (or equivalent information such as its standard error)

The effect size tells her:

> **How large is the estimated effect?**

The variance tells her:

> **How precise is that estimate?**

---

# 17. Why Does Variance Matter?

Consider two studies:

| Study | Effect size | Variance |
| ----- | ----------: | -------: |
| A     |        0.60 |     0.02 |
| B     |        0.60 |     0.15 |

Both studies have the same estimated effect.

But Study A provides a more precise estimate.

This matters because meta-analysis uses information about precision when combining effect sizes.

Maya therefore cannot create an analysis dataset containing only:

`Study ID + Effect Size`

She also needs the information required to quantify uncertainty.

---

# 18. The Analysis Dataset

After calculating effect sizes, Maya creates a dataset specifically for quantitative synthesis.

For example:

| Study ID | Outcome ID | Outcome     | n I | n C | Effect Size | Variance | Direction |
| -------- | ---------- | ----------- | --: | --: | ----------: | -------: | --------- |
| S001     | O1         | Achievement |  60 |  60 |        0.62 |    0.034 | Positive  |
| S002     | O1         | Knowledge   |  75 |  74 |        0.60 |    0.027 | Positive  |
| S003     | O1         | Achievement |  48 |  48 |        0.63 |    0.043 | Positive  |
| S004     | O1         | Skill       |  55 |  55 |        0.80 |    0.039 | Positive  |

This is the dataset Maya will take into **Step 15 — Conduct the Meta-Analysis**.

---

# 19. What If an Effect Size Cannot Be Calculated?

Maya encounters a study that reports:

> “The intervention group performed significantly better than the control group.”

But the paper provides no usable numerical information.

Maya asks:

> **Maya:** “Can I just estimate the effect size?”

Her mentor responds:

> **Mentor:** “No. Do not invent numerical information.”

Instead, Maya should:

1. Check the full text.
2. Check supplementary materials.
3. Check related reports of the same study.
4. Follow the protocol for contacting authors if applicable.
5. Document the missing information.
6. Determine whether a valid effect size can be obtained.

If the required information cannot be obtained, the study may remain part of the systematic review while not contributing an effect size to the particular meta-analysis.

---

# 20. Don't Confuse Statistical Significance With Effect Size

Maya finds another statement:

> “The intervention produced a statistically significant improvement, p < .05.”

She asks:

> **Maya:** “Can I use the p-value as the effect size?”

> **Mentor:** “No.”

A **p-value** and an **effect size** answer different questions.

| Quantity            | Main question                                            |
| ------------------- | -------------------------------------------------------- |
| Effect size         | How large is the estimated effect?                       |
| Confidence interval | How uncertain is the estimate?                           |
| p-value             | How compatible are the data with a specified null model? |
| Variance/SE         | How precise is the estimate?                             |

A statistically significant result does not automatically represent a large effect.

Likewise, a non-significant result does not mean the estimated effect is exactly zero.

---

# 21. What Does Maya Need to Decide Before Calculating?

Before calculating effect sizes for all 22 studies, Maya writes down her decisions.

### Effect-size plan

**Primary outcome:** Student learning outcomes

**Primary effect-size metric:** Hedges' g for continuous outcomes measured on different scales

**Mean difference:** Used when the outcome is measured on a directly comparable scale across studies

**Effect direction:** Positive values represent better learning outcomes for the AI intervention

**Multiple outcomes:** Retain Study ID and Outcome ID

**Multiple time points:** Handle according to the prespecified analysis plan

**Multiple effect sizes from one study:** Preserve their relationship rather than treating them automatically as independent observations

**Missing statistics:** Use protocol-defined methods for recovering or deriving effect sizes

**Unavailable effect size:** Do not invent values; document the study and reason

---

# 22. Maya's Effect-Size Workflow

Maya now has a repeatable process.

```text
Included quantitative study
        ↓
Identify outcome and comparison
        ↓
Identify reported statistics
        ↓
Determine appropriate effect-size metric
        ↓
Check direction of outcome
        ↓
Calculate effect size
        ↓
Calculate variance / standard error
        ↓
Check calculation
        ↓
Record Study ID + Outcome ID
        ↓
Document decisions or conversions
        ↓
Add to meta-analysis dataset
```

---

# 23. Applying the Workflow to the 22 Studies

Maya now processes the 22 studies.

| Study | Quantitative information | Effect-size approach | Meta-analysis dataset |
| ----- | ------------------------ | -------------------- | --------------------- |
| S001  | Mean, SD, n              | Hedges' g            | Include               |
| S002  | Mean, SD, n              | Hedges' g            | Include               |
| S003  | Mean, SD, n              | Hedges' g            | Include               |
| S004  | Mean, SD, n              | Hedges' g            | Include               |
| S005  | Mean, SD, n              | Hedges' g            | Include               |
| S006  | Mean, SD, n              | Hedges' g            | Include               |
| S007  | Mean, SD, n              | Hedges' g            | Include               |
| S008  | Mean, SD, n              | Hedges' g            | Include               |
| S009  | Mean, SD, n              | Hedges' g            | Include               |
| S010  | Mean, SD, n              | Hedges' g            | Include               |
| S011  | Mean, SD, n              | Hedges' g            | Include               |
| S012  | Mean, SD, n              | Hedges' g            | Include               |
| S013  | Mean, SD, n              | Hedges' g            | Include               |
| S014  | Mean, SD, n              | Hedges' g            | Include               |
| S015  | Mean, SD, n              | Hedges' g            | Include               |
| S016  | Mean, SD, n              | Hedges' g            | Include               |
| S017  | Mean, SD, n              | Hedges' g            | Include               |
| S018  | Mean, SD, n              | Hedges' g            | Include               |
| S019  | Mean, SD, n              | Hedges' g            | Include               |
| S020  | Mean, SD, n              | Hedges' g            | Include               |
| S021  | Mean, SD, n              | Hedges' g            | Include               |
| S022  | Mean, SD, n              | Hedges' g            | Include               |

These 22 studies now have the information needed for the planned quantitative synthesis.

---

# 24. Quality Checks Before Moving On

Before Maya sends the dataset to the meta-analysis, she checks:

### Study identification

* Does every record have a unique Study ID?
* Does every outcome have an Outcome ID?
* Are related reports linked to the same study?

### Sample information

* Are intervention and control sample sizes correct?
* Are group sizes plausible?
* Are there transcription errors?

### Outcome information

* Is the outcome eligible?
* Is the outcome direction consistent?
* Is the measurement scale correctly identified?

### Effect-size calculation

* Is the selected effect-size metric appropriate?
* Was the correct formula used?
* Was any small-sample correction applied correctly?
* Is the variance available?

### Documentation

* Were conversions documented?
* Were assumptions documented?
* Were missing-data decisions documented?
* Can another researcher reproduce the calculation?

---

# 25. Maya's Final Dataset

After checking the calculations, Maya has transformed the extracted study results into an analysis-ready effect-size dataset.

```text
111 eligible studies
        ↓
22 studies suitable for quantitative synthesis
        ↓
Extract quantitative information
        ↓
Calculate effect sizes
        ↓
Calculate variance / standard errors
        ↓
Check direction and calculations
        ↓
Document decisions
        ↓
Meta-analysis dataset
        ↓
STEP 15
Conduct the Meta-Analysis
```

Maya closes her spreadsheet.

> **Maya:** “Now every study has a common effect-size metric.”

> **Mentor:** “Exactly.”

> **Maya:** “So now I can combine them?”

> **Mentor:** “Yes—but not yet without thinking about the model and the studies' differences.”

Maya looks curious.

> **Maya:** “What do you mean?”

Her mentor points to the 22 effect sizes.

> **Mentor:** “These studies don't necessarily estimate exactly the same effect. They may differ in participants, AI technologies, settings, interventions, and methods. Now we need to decide how to statistically combine the effect sizes.”

Maya nods.

> **Maya:** “So that is the meta-analysis.”

> **Mentor:** “Exactly.”

---

# 26. Key Takeaways

By the end of this step, Maya understands that:

1. An effect size represents the magnitude and direction of a finding.
2. Effect sizes allow results from different studies to be expressed in a common metric.
3. Mean difference is useful when studies use directly comparable measurement scales.
4. Standardized mean differences can be useful when studies measure comparable constructs using different scales.
5. Hedges' g is a commonly used corrected standardized mean difference.
6. Mean, SD, and sample size are one common way to calculate an effect size.
7. Other reported statistics may also provide enough information to derive an effect size.
8. Effect direction must be consistent across studies.
9. A study can contribute multiple effect sizes.
10. Effect-size variance or equivalent precision information is important for meta-analysis.
11. A p-value is not an effect size.
12. Missing information should be documented rather than invented.
13. Study ID and Outcome ID help preserve the relationship between multiple outcomes from the same study.
14. The final effect-size dataset becomes the input for the meta-analysis.

---

# 27. What Should Maya Do Next?

Maya has now converted the results from the eligible quantitative studies into effect sizes.

The next question is:

> **How should these effect sizes be statistically combined?**

That takes Maya to:

## Step 15 — Conduct the Meta-Analysis

There she will learn about:

* fixed-effect and random-effects models
* weighting studies
* pooled effect sizes
* confidence intervals
* forest plots
* interpreting the pooled estimate
* why studies may produce different effect estimates
* choosing an appropriate meta-analytic model

---

# Repository Structure

```text
step-14-calculate-effect-sizes/
│
├── README.md
│
├── effect-sizes/
│   ├── effect-size-guide.md
│   ├── calculation-guide.md
│   ├── effect-size-decisions.md
│   ├── effect-size-data.xlsx
│   └── effect-size-checks.md
│
├── examples/
│   ├── mean-difference-example.md
│   ├── hedges-g-example.md
│   ├── alternative-statistics-example.md
│   └── multiple-outcomes-example.md
│
├── documentation/
│   ├── coding-guide.md
│   ├── calculation-log.md
│   └── missing-data-log.md
│
└── assessment/
    └── assessment.md
```

---

# Assessment

## Instructions

Choose the best answer for each question.

### 1. What is the primary purpose of calculating an effect size?

A. To determine whether a study should be published
B. To replace the study's sample size
C. To express the magnitude and direction of a finding in a form suitable for comparison
D. To determine whether a study has a low risk of bias

### 2. When is a mean difference particularly appropriate?

A. When outcomes are measured on directly comparable scales
B. When no numerical information is available
C. When studies have different outcome constructs
D. When only p-values are reported

### 3. What does a standardized mean difference do?

A. Removes the study's sample size
B. Converts every outcome into a percentage
C. Expresses a difference relative to outcome variability
D. Converts a p-value into a confidence interval

### 4. What is Hedges' g?

A. A risk-of-bias tool
B. A corrected standardized mean difference
C. A measure of publication bias
D. A heterogeneity statistic

### 5. Which information is commonly sufficient for calculating a standardized mean difference for two independent groups?

A. Mean, SD, and sample size for the relevant groups
B. Title and abstract
C. Author names only
D. Publication year only

### 6. A study reports a *t* statistic and relevant sample information. What should Maya do?

A. Automatically exclude the study
B. Replace the statistic with zero
C. Determine whether the reported information can be converted into the planned effect-size metric
D. Assume the effect is large

### 7. Why does Maya need to pay attention to effect direction?

A. To make all positive values represent the same substantive direction
B. To increase the sample size
C. To remove studies with negative results
D. To make all effect sizes equal

### 8. A study reports achievement, motivation, and engagement. How should Maya identify these results?

A. Give every result the same Study ID and no outcome identifier
B. Create separate studies for each outcome
C. Preserve the Study ID and use distinct Outcome IDs
D. Remove all but one outcome automatically

### 9. Why is variance important?

A. It identifies the study's publication year
B. It provides information about the precision of the effect estimate
C. It determines the study's eligibility
D. It identifies the research question

### 10. Maya finds that a paper reports only “p < .05.” What should she conclude?

A. The p-value itself is the effect size
B. The study necessarily has a large effect
C. She needs to determine whether sufficient information exists to obtain the planned effect size
D. The study automatically has a zero effect

### 11. What should Maya do when required numerical information cannot be recovered?

A. Invent a plausible value
B. Copy the value from another study
C. Document the missing information and follow the protocol's procedure
D. Automatically classify the study as having no effect

### 12. Why should Maya preserve the original extracted statistics after calculating the effect size?

A. To make the paper longer
B. To maintain a transparent and reproducible link between reported results and calculated effects
C. To increase the number of studies
D. To avoid calculating variance

### 13. Can one study contribute more than one effect size?

A. No, every study can have only one effect size
B. Yes, depending on outcomes, comparisons, or time points
C. Only if the study has more than 1,000 participants
D. Only when the study is randomized

### 14. What should Maya avoid doing with multiple outcomes from the same study?

A. Giving them Outcome IDs
B. Preserving their Study ID
C. Automatically treating them as independent studies
D. Documenting how they will be handled

### 15. What is the next step after calculating and checking the effect sizes?

A. Return to database searching
B. Repeat title and abstract screening
C. Conduct the meta-analysis
D. Develop the research question again

---

# Answer Key

| Question | Answer |
| -------- | ------ |
| 1        | C      |
| 2        | A      |
| 3        | C      |
| 4        | B      |
| 5        | A      |
| 6        | C      |
| 7        | A      |
| 8        | C      |
| 9        | B      |
| 10       | C      |
| 11       | C      |
| 12       | B      |
| 13       | B      |
| 14       | C      |
| 15       | C      |

---

## Final Transition

**Step 13:** Prepare the Data for Analysis
↓
**Step 14:** Calculate Effect Sizes
↓
**Step 15:** Conduct the Meta-Analysis

Maya is ready to combine the evidence—but first she needs to decide **how the 22 effect sizes should be statistically synthesized.**
