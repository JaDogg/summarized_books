# Machine Learning 

## Introduction

* Sample Usages
    * Google search ranking.
    * Facebook photo tagging.
    * Spam detection.
    * Find shortest path from A to B.
    * Database mining.
        * Web click data, medical data, biology, engineering
    * Handwriting recognition.
    * Natural language processing.
    * Computer vision.
    * Product recomendation.
* What is machine learning ?
    * Arthur Samuel (1959) - Field of study that gives computers the ability to learn without being explicitly programmed.
    * Tom Mitchell (1998) - Well-posed Learning Problem: A computer program is said to *learn* from experience `E` with respect of task `T` and some performace measure `P`, if its performance on `T`, as measured by `P`, improves with experience `E`.
        * Spam filter:
            * T - Classifying emails as spam or not.
            * E - User marks email as spam.
            * P - The fraction of emails correctly clasified as spam/not spam.
    * Machine learning grew out of work in AI.
* Supervised learning 
    * Knows right answers.
    * Algorithm produces more right answers.
    * Regression problem. Predict continues valued output.
        * Sample: How many items will sell in next 3 months ?
        * Housing price prediction
    * Classification problem. 
        * Sample: Is user account hacked ?
        * Breast cancer ["malignant", "benign"]
            * Features:
                * Age, Tumor size, Clump thickness, Uniformity of cell size,...
        * If it is infinite number of features -> Support vector machines.
* Unsupervised Learning
    * Clusturing:
        * Usage:
            * Social network analyzation.
            * Organize computer clusters.
            * Market segmentation.
            * Astronomical data analysis.
            * Given a set of news articles, group them into set of articles.
            * Given a set of customer data, automatically discover market segments and group customers into different market segments.
        * Cocktail party problem:
            * People talking all the time.
            * Two microphones are put at different location.
            * Give it to Cocktail party algorithm.
            * Seperate the audios.

## Linear Regression with One Variable

* House Price -> Regression Problem
* Notation:
    * `m` -> Number of training examples
    * `x`'s -> **Input** variable/**Features**
    * `y`'s -> **Output** variable/**Target** variable
    * `(x,y)` -> One training example
    * `(x^(i), y^(i))` -> i^th training example. `i` is the Index. not exp.
    * `h` -> Hypothesis
* Training Set -> Learning Algorithm -> `h`
* Size of house -> `h` -> Estimated price
* `h` maps from `x`'s to `y`'s 
* `h(_theta)(x) = (theta)_0 + (theta)_0x`
