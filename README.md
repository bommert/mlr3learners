# mlr3learners

This packages provides essential learners for [mlr3](https://mlr3.mlr-org.com), maintained by the mlr-org team.
We will most likely not add new learners to this package.

[![Build Status](https://travis-ci.org/mlr-org/mlr3learners.svg?branch=master)](https://travis-ci.org/mlr-org/mlr3learners)
[![CRAN Status Badge](https://www.r-pkg.org/badges/version-ago/mlr3learners)](https://cran.r-project.org/package=mlr3learners)
[![Cran Checks](https://cranchecks.info/badges/worst/mlr3learners)](https://cran.r-project.org/web/checks/check_results_mlr3learners.html)
[![Codecov](https://codecov.io/gh/mlr-org/mlr3learners/branch/master/graph/badge.svg)](https://codecov.io/gh/mlr-org/mlr3learners)
[![StackOverflow](https://img.shields.io/badge/stackoverflow-mlr3-orange.svg)](https://stackoverflow.com/questions/tagged/mlr3)

Other learners live in the [mlr3learners](https://github.com/mlr3learners) organization and are possibly maintained by people outside the mlr-org team.
There is a [wiki page](https://github.com/mlr-org/mlr3learners/wiki/Extra-Learners) listing all currently available custom learners.
See [below](#requestingadding-additional-learners) for instructions on how to add a new learner.

## Classification Learners

| ID                                                                                              | Learner                       | Package                                               |
| :---------------------------------------------------------------------------------------------- | :---------------------------- | :---------------------------------------------------- |
| [classif.glmnet](https://mlr3learners.mlr-org.com/reference/LearnerClassifGlmnet.html)          | Penalized Logistic Regression | [glmnet](https://cran.r-project.org/package=glmnet)   |
| [classif.kknn](https://mlr3learners.mlr-org.com/reference/LearnerClassifKKNN.html)              | k-Nearest Neighbors           | [kknn](https://cran.r-project.org/package=kknn)       |
| [classif.lda](https://mlr3learners.mlr-org.com/reference/LearnerClassifLDA.html)                | LDA                           | [MASS](https://cran.r-project.org/package=MASS)       |
| [classif.log_reg](https://mlr3learners.mlr-org.com/reference/LearnerClassifLogReg.html)         | Logistic Regression           | stats                                                 |
| [classif.naive_bayes](https://mlr3learners.mlr-org.com/reference/LearnerClassifNaiveBayes.html) | Naive Bayes                   | [e1071](https://cran.r-project.org/package=e1071)     |
| [classif.qda](https://mlr3learners.mlr-org.com/reference/LearnerClassifQDA.html)                | QDA                           | [MASS](https://cran.r-project.org/package=MASS)       |
| [classif.ranger](https://mlr3learners.mlr-org.com/reference/LearnerClassifRanger.html)          | Random Forest                 | [ranger](https://cran.r-project.org/package=ranger)   |
| [classif.svm](https://mlr3learners.mlr-org.com/reference/LearnerClassifSVM.html)                | SVM                           | [e1071](https://cran.r-project.org/package=e1071)     |
| [classif.xgboost](https://mlr3learners.mlr-org.com/reference/LearnerClassifXgboost.html)        | Gradient Boosting             | [xgboost](https://cran.r-project.org/package=xgboost) |

## Regression Learners

| ID                                                                                 | Learner                     | Package                                                       |
| :--------------------------------------------------------------------------------- | :-------------------------- | :------------------------------------------------------------ |
| [regr.glmnet](https://mlr3learners.mlr-org.com/reference/LearnerRegrGlmnet.html)   | Penalized Linear Regression | [glmnet](https://cran.r-project.org/package=glmnet)           |
| [regr.kknn](https://mlr3learners.mlr-org.com/reference/LearnerRegrKKNN.html)       | k-Nearest Neighbors         | [kknn](https://cran.r-project.org/package=kknn)               |
| [regr.km](https://mlr3learners.mlr-org.com/reference/LearnerRegrKM.html)           | Kriging                     | [DiceKriging](https://cran.r-project.org/package=DiceKriging) |
| [regr.lm](https://mlr3learners.mlr-org.com/reference/LearnerRegrLM.html)           | Linear Regression           | stats                                                         |
| [regr.ranger](https://mlr3learners.mlr-org.com/reference/LearnerRegrRanger.html)   | Random Forest               | [ranger](https://cran.r-project.org/package=ranger)           |
| [regr.svm](https://mlr3learners.mlr-org.com/reference/LearnerRegrSVM.html)         | SVM                         | [e1071](https://cran.r-project.org/package=e1071)             |
| [regr.xgboost](https://mlr3learners.mlr-org.com/reference/LearnerRegrXgboost.html) | Gradient Boosting           | [xgboost](https://cran.r-project.org/package=xgboost)         |

## Requesting/Adding additional learners

Please follow these steps to add/request a new learner. 
Steps 2-6 are only needed if you want to add a learner yourself.

1. Open an issue in [mlr3learners](https://github.com/mlr-org/mlr3learners/issues) following the issue template.

1. Fork the
   [mlr3learnertemplate](https://github.com/mlr-org/mlr3learnertemplate) repo
   and adjust the template to your needs. 
   Follow the instructions given in the [mlr3book](https://mlr3book.mlr-org.com/ext-learner.html) to get started.

2. When you are somewhat done, request to add your learner to the [mlr3learners](https://github.com/mlr3learners) organization by transfering your repository to the _mlr3learners_ organization. Once transfered, you will get access rights to your repository to finalize the learner.

3. Add your learner to the section in [mlr3learners wiki](https://github.com/mlr-org/mlr3learners/wiki) which matches best the current status of your repo.

4. Once you are happy with the status of the learner, request a review in the issue from @mllg, @berndbischl, @pat-s or @be-marc

5. Congrats! Your learner has been successfully added to the mlr3 ecosystem. Now that you've implemented the learner, we would also be happy if you also maintain it against the upstream package :)
