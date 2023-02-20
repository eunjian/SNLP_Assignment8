# [Assignment 8: Author profiling](https://snlp2020.github.io/a8/)

In this assignment,
we are interested in predicting the gender of the author of a short text.
Unlike earlier assignments,
this assignment is intentionally open-ended.

The main challenge in this assignment is the size of the data set.
Since our data set is small,
achieving reliably good scores is rather difficult.

## Data

The primary data set is from the short essays 
written by the class participants at the beginning of the semester.
You will find two files in your repositories,
[one for training](essays-train.txt)
and [one for testing](essays-test.txt).
Both data sets are provided as tab-separated-value files.
Where column headers for the class label and the essay texts are
`label` and `text`, respectively.
Note that a record may span multiple lines,
if the essay text contains newlines,
in which case text will be quoted.
You are recommended to use a library (e.g., Python `csv` library)
to read the data.

You should use the `essays-train.tsv` for both training and tuning your model,
and you should use `essays-test.tsv` **only for testing**.
It is OK to use it to test alternative models/systems,
but test file should not be used during development/tuning process.

## Task

### 8.1 Implement, tune and test a text classification model

Implement one or more text classification methods,
tune its hyperparameters,
and test on the provided test set.
For this exercise use only the data set provided.

You are encouraged to try multiple models/systems,
and organize your code the way you like.
Please pay attention to good programming practices.
You may lose points if your code is difficult to follow.

### 8.2 Augment the training/development data with external data

Since the data set is small,
one way to improve classification results is to use external data.
Since the external data swill be "out of domain",
it may not be as effective as the given training set.
However, gender identification is a popular subject.
There are many freely available data sets,
which you can use of to improve the results you obtained in 8.1.
Finding appropriate data sets and experimenting with them is part of this exercise.
Potentially useful external data include, but not limited to,
earlier data sets on author profiling or gender detection,
pre-trained embeddings or features based on clustering results on a large, unlabeled data set.
If nothing else works,
you can try to make use of the Twitter corpus collected
for [assignment 1](https://snlp2020.github.io/a1/).

### 8.3 Report your results

Part of your grade will be based on a short (no more than 1000 words) report
describing your approach and your results.
Please write your report as a [markdown](https://en.wikipedia.org/wiki/Markdown)
document with name `report.md`.

If you worked on both exercises above,
your report should describe both exercises.
However, it should still be written as a single coherent report,
describing the common aspects of the experiments only once.

Your report should include the following.

- Technical information about your code:
    - How to run your code to replicate/reproduce the results you report
    - A list of additional libraries required.
        If you use non-standard libraries, including them 
        in your repository is a good idea.
    - Links to additional data or resources used.
        If they are publicly available (and large),
        do not include them in your repository but provide links.
        If they are not publicly available,
        but too big for inclusion in your repository,
        please provide an alternative download link.
- A description of your approach:
    - Which method/model(s) did you use?
    - How did you tune your model(s)?
    - Did you employ any preprocessing or feature selection steps?
    - Did you use external data, if so what are they?
- A report of your results:
    - Report the appropriate scores for your model(s)
    - If you used multiple models,
        or alternative data sources and/or other settings
        with the same model, please report all.
    - A comparison with an appropriate trivial baseline.
- (optional) an analysis of useful features.
    For example by analyzing the learned weights,
    or through ablation experiments.
    
## Evaluation

This is an extra assignment.
The exercises 8.1 and 8.2 together with their descriptions (8.3)
make up for two seperate assignment.
For both exercises:

- 6/10th of the score will be based on checking your source code and experimental setup,
    and reproducibility of your results.
- You will get 2 points (out of 10) for a well-written report.
    The report should clearly indicate the required information above,
    and you should pay attention to formatting and language.
- 2 points (out of 10) will be based on the macro-averaged F1 score on the test set.
    - For 8.1, you get 1 points if the score you obtained is over a
      majority baseline, and 2 points, if your score is over the
      average score obtained during last year's assignment.
    - For 8.2,  you get 1 points if the score you obtained is over a
      majority baseline, and 2 points, if your score is over the
      score you obtained in 8.1.
