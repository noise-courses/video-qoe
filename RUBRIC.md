# Grading rubric — Assignment 1: Video Quality Inference

**10 points, graded for completion.** Per the syllabus, assignments are graded
primarily on whether you did the work: if the notebook runs end to end and each
part does what it asks, you get full credit. Quality of the model is *not*
graded; a mediocre F1 with a working pipeline is 10/10.

| # | Item | Pts |
|---|---|---|
| **Part 1 — Warmup** | | **3** |
| 1.1 | Load `netflix.pcap` and use the DNS traffic to filter down to Netflix flows | 1 |
| 1.2 | Generate flow statistics/features (netml or your own) **and write a brief justification** for the features chosen | 1 |
| 1.3 | Add a segment-download-rate feature (video segments per time window) to the feature vector | 1 |
| **Part 2 — Video quality inference** | | **5** |
| 2.1 | Load the video dataset pickle and remove rows whose resolution is not one of 240/360/480/720/1080 | 1 |
| 2.2 | Identify and drop the columns that are unnecessary/unhelpful for prediction, **with a brief explanation of why** | 1 |
| 2.3 | Build the feature matrix and labels; train/test split; train a model of your choice | 1 |
| 2.4 | Hyperparameter tuning (grid/random search, CV, or a documented manual sweep) | 1 |
| 2.5 | Evaluate with **all four**: accuracy, F1, confusion matrix, ROC/AUC | 1 |
| **Part 3 — Real session** | | **2** |
| 3.1 | Apply the trained model to the preprocessed Netflix session to infer resolution at 10-second intervals | 1 |
| 3.2 | **Plot** the inferred resolution over time | 1 |

## Requirements that gate the score

- **The notebook must run.** Submit it *executed* (outputs saved). A notebook
  with error tracebacks in its outputs, or with no outputs at all, is treated
  as not running: the failing part(s) earn 0 until fixed and resubmitted.
- **Sub-items are all-or-nothing.** Each row is 1 point if done in good faith,
  0 if absent. There are no half points; "did the thing" is the bar.
- **Written answers count.** Items 1.2 and 2.2 require a sentence or two of
  explanation, not just code.
- **AI use.** Encouraged, but acknowledge it in the notebook and be ready to
  explain your code. Not acknowledging AI use does not cost points on this
  assignment, but see the syllabus on assessment of understanding.

## Late policy

Due 5:00 p.m. Chicago time on the due date; 96-hour grace balance for the term,
then half credit within one week, then zero. See the syllabus.
