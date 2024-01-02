---
aliases:
  - Multicollinearity - an overview
tags:
  - reference-material/read-it-later/article
  - mathematics
  - mathematics/statistics
  - measurement
file-created: 2023-04-01
file-modified: 2023-09-03
note-type: article
description: 
author: Info icon
linter-yaml-title-alias: Multicollinearity - an overview
original-title: "Multicollinearity - an overview | ScienceDirect Topics"
reference: true
source: https://www.sciencedirect.com/topics/mathematics/multicollinearity
website: 
---
 #status/postponed

# Multicollinearity - an overview

## Practitioners overcorrect for multicollinearity

- [x] Need to review how this works and what it explains ✅ 2023-08-22

> Two random variables will almost always correlate at some level in a sample, even if they share no fundamental relationship in the larger population. In other words, multicollinearity is a matter of degree; it is not a problem that either does or does not appear.
>
> Furthermore, partial multicollinearity violates absolutely none of the assumptions of linear regression: It does not bias coefficient estimates, does not result in inefficient use of the data available, and does not cause falsely confident conclusions. The sole effect of this data limitation is that it makes conclusions more ambiguous or hesitant than they otherwise might have been.
>
> Despite **the omnipresence and relative harmlessness** of the [multicollinearity problem](https://www.sciencedirect.com/topics/mathematics/multicollinearity-problem "Learn more about multicollinearity problem from ScienceDirect's AI-generated Topic Pages"), however, *practitioners often write as though it represents an analytical flaw* for which everyone must test and that must be solved if it appears. They may select solutions for dealing with multicollinearity that harm an analysis more than they help it. In short, practitioners take partial multicollinearity much more seriously than statistical theory or the methodological literature justifies.

Seems similar to the [[Self-organization is the complex behaviors of multiple individual interactions|self-organizing principles]] of [[Dynamic systems theory|dynamic systems theory]]. Things will interact or collineate with one another. The point is to determine the extent or degree we should give importance to a factor

---

# Multicollinearity - an overview | ScienceDirect Topics

> [!Warning] Reference note
> The original source can be found here: https://www.sciencedirect.com/topics/mathematics/multicollinearity

---

## Article content

%%make it easy to delete under a heading%%

## [Multicollinearity](https://www.sciencedirect.com/science/article/pii/B012369398500428X)

D. Stephen Voss, in [Encyclopedia of Social Measurement](https://www.sciencedirect.com/referencework/9780123693983/encyclopedia-of-social-measurement), 2005

### Introduction

Multicollinearity stands out among the possible pitfalls of empirical analysis for the extent to which it is poorly understood by practitioners. Articles in social science journals often expend an extensive amount of space dismissing the presence of this condition, even though it poses little threat to a properly interpreted analysis.

At its extreme, when explanatory variables overlap completely, multicollinearity violates the assumptions of the classical regression model (CRM). Full (or perfect) multicollinearity is easy to detect, however, because it prevents the estimation of coefficients altogether; an equation becomes unsolvable. This is not the sort of multicollinearity that customarily worries analysts. Full multicollinearity rarely appears in social science data unless the sample is exceedingly small. Otherwise, it generally results from some kind of simple error in the data handling or model specification, one that is easy to diagnose and painless to address. When practitioners speculate about a possible “multicollinearity problem,” therefore, they mean some sort of linear relationship among explanatory variables that falls short of complete overlap.

Partial multicollinearity—the use of overlapping variables that still exhibit independent variation—is ubiquitous in multiple regression. Two random variables will almost always correlate at some level in a sample, even if they share no fundamental relationship in the larger population. In other words, multicollinearity is a matter of degree; it is not a problem that either does or does not appear. Furthermore, partial multicollinearity violates absolutely none of the assumptions of linear regression: It does not bias coefficient estimates, does not result in inefficient use of the data available, and does not cause falsely confident conclusions. The sole effect of this data limitation is that it makes conclusions more ambiguous or hesitant than they otherwise might have been. Despite the omnipresence and relative harmlessness of the multicollinearity problem, however, practitioners often write as though it represents an analytical flaw for which everyone must test and that must be solved if it appears. They may select solutions for dealing with multicollinearity that harm an analysis more than they help it. In short, practitioners take partial multicollinearity much more seriously than statistical theory or the methodological literature justifies.

The remainder of this entry proceeds in four sections. First, we treat full multicollinearity in depth, both substantively and statistically. Next, we provide the basic intuition for why collinear variables confound an analysis, using specific examples, and offer various mathematical illustrations of how full multicollinearity prevents the classical regression model from producing coefficient estimates. We then turn to partial multicollinearity, distinguishing the effects of this data condition according to the purposes for which an analyst has included a particular variable. Next we briefly reviews the various symptoms of and tests for multicollinearity customarily used by social scientists. In the last section, we consider the array of methods for dealing with multicollinearity that analysts have available to them.

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B012369398500428X)

URL: https://www.sciencedirect.com/science/article/pii/B012369398500428X

## [Volume 4](https://www.sciencedirect.com/science/article/pii/B9780444527011000119)

E.M. Færgestad, … H. Martens, in [Comprehensive Chemometrics](https://www.sciencedirect.com/referencework/9780444527011/comprehensive-chemometrics), 2009

### 4.08.3.5 Multicollinearity

Multicollinearity describes a situation where different variables reflect related variation. This will be the situation whenever the number of variables *p* is larger than the number of samples *n*. The classical statistical methods for data modeling usually require *n* > *p* for independent variables, whereas modern functional genomics data typically have *n* < *p*, and very often *n* << *p* for highly correlated variables.

Performing the regression analysis, **y** = β0 + β1**x**1 + β2**x**2 + β12**x**12 + **e** may be viewed graphically as putting a two-dimensional plane on the data points in **Figure 4(a)**, where the samples are seen as dots representing nails where the axis for the response parameters is pointed upward from the plot, and therefore not visible as we here look straight down on the **x**1 and **x**2 axis. If the heights of the nails increase toward the upper right corner, the plane will have a slope reflecting positive relation to both **x**1 and **x**2. When **x**1 and **x**2 are correlated, as illustrated in **Figure 4(b)**, the regression will be like balancing a plane on a fence, which will be very unstable outside the fence. A solution to this is to transform the original variables into new variables (**Figure 4(c)**), called component 1 and component 2, where the first typically contains most of the variation. These new variables can be defined as being orthogonal. A regression can subsequently be based on the new orthogonal variables (see **Figure 4(d)**). We can view the new variables as reflecting some underlying latent phenomenon. One example is where **x**1 and **x**2 reflect two indicator variables for a disease; then the latent variable might reflect the disease as such. The number of x-variables can be extended to a large number. The multicollinear problem is by this approach turned over to be an advantage as several variables describing the same phenomenon will stabilize the regression. Furthermore, several variables together may further unravel the fundamental understanding of the system under study, compared to what is obtained when selecting only a subset of the variables prior to data analysis. This focuses on the interpretation and statistical treatment of the underlying phenomenon creating variability rather than on the observed variables.

![](Reference%20Materials/Clippings/3-s2.0-B9780444527011000119-gr4.jpg)

Figure 4. llustration of collinearity between two variables x1 and x2 and the changes to the new axis where the new axis spans, in decreasing order, the variability in the data. Here the new axis is orthogonal and the illustrated changes of axis correspond to principal component analysis (see also **Figure 8**).

In functional genomics, we typically have multicollinearity arising both when, for example, instruments give several variables on one property, and multicollinearity exists among the different properties analyzed. Consider, for example, a study where all genes expressed and various measurements downstreams toward the phenotype are analyzed for a large number of individuals. We would expect a very large number of different properties to vary and be more or less related. Regions on the chromosomes are inherited as linked groups of genes (haplotypes) giving correlated responses of different mRNAs, proteins, metabolites, and phenotypic characteristics. Furthermore, the activities of genes downstream from the genes toward the phenotypic consequences are linked together in complex regulatory or metabolic networks.

By projecting the data to new latent variables, we can describe, validate, and interpret some of the underlying common factors giving rise to the variation in the observed variables. With a very large number of variables, it is nevertheless also important to eliminate irrelevant information and to validate the significance of the observed variables. In this chapter, we therefore go through both projecting based approaches to view the underlying common sources of variation, as well as various approaches for judging the relevance of each of the observed variables.

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780444527011000119)

URL: https://www.sciencedirect.com/science/article/pii/B9780444527011000119

## [Philosophy of Econometrics](https://www.sciencedirect.com/science/article/pii/B9780444516763500130)

Aris Spanos, in [Philosophy of Economics](https://www.sciencedirect.com/book/9780444516763/philosophy-of-economics), 2012

### 7.7 If everything else fails, blame multicollinearity

Another questionable modeling strategy one often encounters in applied econometrics is the appeal to multicollinearity. When in practice a variety of ‘error-fixing’ and theory upholding strategies fail to give rise to an estimated model with theoretically ‘correct’ signs and magnitudes, as well as (seemingly) statistically significant coefficients for the variables of interest, applied econometricians often invoke the presence of near-multicollinearity as the culprit for the failure to corroborate their theory.

Near-multicollinearity is understood as a departure from the G-M assumption (3) rank(X)=k, see (41), where the (XτX) matrix is nearly singular. Greene \[2000, p. 256\], nicely summarizes the traditional perspective:

> “The problem faced by applied researchers is usually … that regressors are highly, although not perfectly, correlated. In this instance, the following symptoms are typically observed:

[[Incremental change|Small changes]] in the data can produce wide swings in the parameter estimates.

Coefficients may have very high standard errors and low significance levels even though they are jointly highly significant and the R2 in the regression is quite high.

Coefficients will have the “wrong” sign or implausible magnitudes.”

Despite the universal agreement among traditional econometric textbooks, it can be shown that, when one accounts for the underlying statistical parameterizations such as (46) above, none of the above symptoms stems from high correlation among the regressors. A much more plausible explanation for the wrong signs and magnitudes, as well as insignificant coefficients, is the severe statistical mis-specification such estimated models often suffer from; see \[Spanos and McGuirk, 2002\]. Indeed, statistical misspecification renders all the invoked statistics like the standard errors, t-ratios and the R2, meaningless artifacts upon which no reliable inference concerning signs and magnitudes can be drawn.

The real problem for the practitioner is not high correlation among regressors as such, but the ill-conditioning of (XτX) — a data specific problem — which gives rise to *erratic volatility* as it relates to the sensitivity of the coefficient estimates βˆ\=(XτX)−1Xτy to (potential) changes in the data matrices (XτX),(Xτy).

To quantify such potential erratic volatility the modeler could utilize norm bounds, and then pose the question whether such volatility is likely to endanger the reliability of inference. If yes, the way to proceed is to use one of several options to enhance the sample information in an attempt to render (XτX) well-conditioned; see \[Spanos and McGuirk, 2002\].

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780444516763500130)

URL: https://www.sciencedirect.com/science/article/pii/B9780444516763500130

## [More Regression Methods](https://www.sciencedirect.com/science/article/pii/B9780128200988000178)

Rand R. Wilcox, in [Introduction to Robust Estimation and Hypothesis Testing (Fifth Edition)](https://www.sciencedirect.com/book/9780128200988/introduction-to-robust-estimation-and-hypothesis-testing), 2022

### 11.1.1 Omnibus Tests for Regression Parameters

This section begins with testing Eq. (11.1). Generally, a type of bootstrap method performs well when using a robust regression estimator. An exception is when using a robust ridge estimator as in Section 10.13.15, with the goal of dealing with multicollinearity. The end of this section describes how to deal with this special case.

When working with robust regression, three strategies for testing hypotheses have received attention in the statistical literature and should be mentioned. The first is based on the so-called *Wald scores*, the second is a *likelihood ratio test*, and the third is based on a measure of *drop in dispersion*. Details about these methods can be found in Markatou et al. (1991), as well as Heritier and Ronchetti (1994). Coakley and Hettmansperger (1993) suggest using a Wald scores test in conjunction with their estimation procedure, assuming that the error term is homoscedastic. The method estimates the standard error of their estimator, which can be used to get an appropriate test statistic for which the null distribution is chi-squared. When both *x* and *ϵ* are normal, and the error term is homoscedastic, the method provides reasonably good control over the probability of a Type I error when n\=50. However, if *ϵ* is non-normal, the actual probability of a Type I error can exceed 0.1 when testing at the α\=0.05 level, even with n\=100 (Wilcox, 1994e). Consequently, details about the method are not described. Birkes and Dodge (1993) describe drop-in-dispersion methods when working with M regression methods that do not protect against leverage points. Little is known about how this approach performs under heteroscedasticity, so it is not discussed either. Instead, attention is focused on a method that has been found to perform well when there is a heteroscedastic error term. It is not suggested that the method described here outperforms all other methods that might be used, only that it gives good results over a relatively wide range of situations, and based on extant simulation studies, it is the best method available.

The basic strategy is to generate *B* bootstrap estimates of the parameters, and then determine whether the vector of values specified by the null hypothesis is far enough away from the bootstrap samples to warrant rejecting H0. This strategy is illustrated with the tree data in the Minitab handbook (Ryan et al., 1985, p. 329). The data consist of tree volume (*V*), tree diameter (*d*), and tree height (*h*). If the trees are cylindrical or cone-shaped, then a reasonable model for the data is y\=β1x1+β2x2+β0, where y\=ln(V), x1\=ln(d), x2\=ln(h), with β1\=2 and β2\=1 (Fairley, 1986). The ordinary least squares (OLS) estimate of the intercept is βˆ0\=−6.632, βˆ1\=1.98, and the estimates of the slopes are βˆ2\=1.12. Using M regression with Schweppe weights (the R function bmreg), the estimates are −6.59, 1.97, and 1.11, respectively.

Suppose bootstrap samples are generated as described in Section 10.1.1 (cf. Salibian-Barrera and Zamar, 2002). That is, rows of data are sampled with replacement. Fig. 11.1 shows a scatterplot of 300 bootstrap estimates, using M regression with Schweppe weights, of the intercept, β0, and β2, the slope associated with log height. The square marks the hypothesized values, (β0,β2)\=(−7.5,1). These bootstrap values provide an estimate of a confidence region for (β0,β2) that is centered at the estimated values βˆ0\=−6.59 and βˆ2\=1.11. Fig. 11.1 suggests that the hypothesized values might not be reasonable. That is, the point (−7.5,1) might be far enough away from the bootstrap values to suggest that it is unlikely that β0 and β2 simultaneously have the values −7.5 and 1, respectively. The problem is measuring the distance between the hypothesized values and the estimated values, and then finding a decision rule that rejects the null hypothesis with probability *α* when H0 is true.

![Figure 11.1](Reference%20Materials/Clippings/Figure%2011.1.gif)

Figure 11.1. Scatterplot of bootstrap estimates using the tree data. The square marks the null values.

For convenience, temporarily assume the goal is to test the hypothesis given by Eq. (11.1). A simple modification of the method in Section 8.2.5 can be used where bootstrap samples are obtained by resampling with replacement *n* rows from

(y1,x11,…,x1J⋮yn,xn1,…,xnJ),

yielding

(y1⁎,x11⁎,…,x1J⁎⋮yn⁎,xn1⁎,…,xnJ⁎).

Let βˆjb⁎, j\=1,…,p, b\=1,…,B, be an estimate of the *j*th parameter based on the *b*th bootstrap sample and any robust estimator described in Chapter 10. Then an estimate of the covariance between βˆj and βˆk is

vjk\=1B−1∑b\=1B(βˆjb⁎−β¯j⁎)(βˆkb⁎−β¯k⁎),

where β¯j⁎\=∑βˆjb⁎/B. Here, βˆj can be any estimator of interest. Now, the distance between the *b*th bootstrap estimate of the parameters and the estimate based on the original observations can be measured with

db2\=(βˆ1b⁎−βˆ1,…,βˆpb⁎−βˆp)V−1(βˆ1b⁎−βˆ1,…,βˆpb⁎−βˆp)′,

where **V** is the *p*\-by-*p* covariance matrix with the element in the *j*th row and *k*th column equal to vjk. That is, V\=(vjk) is the sample covariance matrix based on the bootstrap estimates of the parameters. The square root of db2, db, represents a simple generalization of the Mahalanobis distance. If the point corresponding to the vector of hypothesized values is sufficiently far from the estimated values, relative to the distances db, reject H0. This strategy is implemented by putting the db values in ascending order, yielding d(1)≤⋯≤d(B), setting M\=\[(1−α)B\], and letting *m* be the value of *M* rounded to the nearest integer. The null hypothesis is rejected if

(11.2)D\>d(m),

where

D\=(βˆ1,…,βˆp)V−1(βˆ1,…,βˆp)′.

The method just described is easily generalized to testing

H0:β1\=β10,β2\=β20,…,βq\=βq0,

the hypothesis that *q* of the p+1 parameters are equal to specified constants, β10,…,βq0. Proceed as before, only now

db\=(βˆ1b⁎−βˆ1,…,βˆqb⁎−βˆq)V−1(βˆ1b⁎−βˆ1,…,βˆqb⁎−βˆq)′,

and **V** is a *q*\-by-*q* matrix of estimated covariances based on the *B* bootstrap estimates of the *q* parameters being tested. The critical value, d(m), is computed as before, and the test statistic is

D\=(βˆ1−β10,…,βˆq−βq0)V−1(βˆ1−β10,…,βˆq−βq0)′.

The (generalized) p-value is

pˆ⁎\=1B∑I(D≤db),

where I(D≤db)\=1 if D≤db and I(D≤db)\=0 if D\>db.

The hypothesis testing method just described can be used with any regression estimator. When using the OLS estimator, it has advantages over the conventional F test, but problems remain. This is illustrated by Table 11.1, which shows the estimated probability of a Type I error for various situations when testing H0:β1\=β2\=0, α\=0.05, and where

Table 11.1. Estimated Type I error probabilities using OLS, *α* = 0.05, *n* = 20.

| *x* |  | *ϵ* |  | VP 1 |  | VP 2 |  | VP 3 |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| *g* | *h* | *g* | *h* | Boot | *F* | Boot | *F* | Boot | *F* |
| 0.0 | 0.0 | 0.0 | 0.0 | 0.072 | 0.050 | 0.097 | 0.181 | 0.009 | 0.015 |
| 0.0 | 0.0 | 0.0 | 0.5 | 0.028 | 0.047 | 0.046 | 0.135 | 0.004 | 0.018 |
| 0.0 | 0.0 | 0.5 | 0.0 | 0.052 | 0.049 | 0.084 | 0.174 | 0.009 | 0.018 |
| 0.0 | 0.0 | 0.5 | 0.5 | 0.028 | 0.043 | 0.042 | 0.129 | 0.005 | 0.019 |
| 0.0 | 0.5 | 0.0 | 0.0 | 0.022 | 0.055 | 0.078 | 0.464 | 0.003 | 0.033 |
| 0.0 | 0.5 | 0.0 | 0.5 | 0.014 | 0.074 | 0.042 | 0.371 | 0.002 | 0.038 |
| 0.0 | 0.5 | 0.5 | 0.0 | 0.017 | 0.048 | 0.072 | 0.456 | 0.005 | 0.032 |
| 0.0 | 0.5 | 0.5 | 0.5 | 0.011 | 0.070 | 0.039 | 0.372 | 0.005 | 0.040 |
| 0.5 | 0.0 | 0.0 | 0.0 | 0.054 | 0.044 | 0.100 | 0.300 | 0.013 | 0.032 |
| 0.5 | 0.0 | 0.0 | 0.5 | 0.024 | 0.057 | 0.049 | 0.236 | 0.010 | 0.038 |
| 0.5 | 0.0 | 0.5 | 0.0 | 0.039 | 0.048 | 0.080 | 0.286 | 0.010 | 0.033 |
| 0.5 | 0.0 | 0.5 | 0.5 | 0.017 | 0.058 | 0.046 | 0.217 | 0.010 | 0.040 |
| 0.5 | 0.5 | 0.0 | 0.0 | 0.013 | 0.054 | 0.083 | 0.513 | 0.006 | 0.040 |
| 0.5 | 0.5 | 0.0 | 0.5 | 0.009 | 0.073 | 0.043 | 0.416 | 0.002 | 0.048 |
| 0.5 | 0.5 | 0.5 | 0.0 | 0.013 | 0.053 | 0.079 | 0.505 | 0.005 | 0.043 |
| 0.5 | 0.5 | 0.5 | 0.5 | 0.006 | 0.067 | 0.036 | 0.414 | 0.005 | 0.050 |

(11.3)y\=β1x1+β2x2+λ(x1,x2)ϵ.

(For results on testing hypotheses when the function *λ* is known, see Zhao and Wang, 2009.) In Table 11.1, VP 1 corresponds to λ(x1,x2)\=1 (a homoscedastic error term), VP 2 is λ(x1,x2)\=|x1|, and VP 3 is λ(x1,x2)\=1/(|x1|+1). Both x1 and x2 have identical g-and-h distributions, with the *g* and *h* values specified by the first two columns. In some cases, the conventional F test performs well, but it performs poorly for VP 2. The bootstrap method improves matters considerably, but the probability of a Type I error exceeds 0.075 in various situations. In practical terms, when testing hypotheses using OLS, use the methods in Section 10.1.1 rather than the bootstrap method described here.

Table 11.2 shows αˆ, the estimated probability of a Type I error when using βˆmid, the biweight midregression estimator with n\=20, and the goal is to test H0:β1\=β2\=0, with α\=0.05. Now, the probability of a Type I error is less than or equal to the nominal level, but in some cases, it is too low, particularly for VP 3, where it drops as low as 0.002. (For more details about the simulations used to create Tables 11.1 and 11.2, see Wilcox, 1996f.) Simulations indicate that switching to the Theil–Sen estimator improves the control over the Type I error probability when dealing with heavy-tailed distributions (Wilcox, 2004c).

Table 11.2. Values of αˆ using biweight midregression, *α* = 0.05, *n* = 20.

| *x* |  | *ϵ* |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| *g* | *h* | *g* | *h* | VP 1 | VP 2 | VP 3 |
| 0.0 | 0.0 | 0.0 | 0.0 | 0.047 | 0.039 | 0.015 |
| 0.0 | 0.0 | 0.0 | 0.5 | 0.018 | 0.024 | 0.008 |
| 0.0 | 0.0 | 0.5 | 0.0 | 0.038 | 0.037 | 0.011 |
| 0.0 | 0.0 | 0.5 | 0.5 | 0.021 | 0.025 | 0.003 |
| 0.0 | 0.5 | 0.0 | 0.0 | 0.016 | 0.018 | 0.002 |
| 0.0 | 0.5 | 0.0 | 0.5 | 0.009 | 0.018 | 0.002 |
| 0.0 | 0.5 | 0.5 | 0.0 | 0.015 | 0.016 | 0.002 |
| 0.0 | 0.5 | 0.5 | 0.5 | 0.009 | 0.012 | 0.003 |
| 0.5 | 0.0 | 0.0 | 0.0 | 0.033 | 0.037 | 0.012 |
| 0.5 | 0.0 | 0.0 | 0.5 | 0.020 | 0.020 | 0.006 |
| 0.5 | 0.0 | 0.5 | 0.0 | 0.024 | 0.031 | 0.009 |
| 0.5 | 0.0 | 0.5 | 0.5 | 0.015 | 0.021 | 0.005 |
| 0.5 | 0.5 | 0.0 | 0.0 | 0.015 | 0.021 | 0.002 |
| 0.5 | 0.5 | 0.0 | 0.5 | 0.008 | 0.011 | 0.002 |
| 0.5 | 0.5 | 0.5 | 0.0 | 0.014 | 0.017 | 0.002 |
| 0.5 | 0.5 | 0.5 | 0.5 | 0.006 | 0.007 | 0.002 |

#### Methods Based on a Ridge Estimator

As noted in Section 10.13.15, when there is multicollinearity, a regression estimator can have relatively high standard errors, which in turn impacts power. Ridge estimators introduced in Section 10.13.15 are designed to deal with this issue, but an alternative to Eq. (11.2) is needed when testing Eq. (11.1).

#### Method RT1

First consider the non-robust ridge estimator. Let the values of the independent variables be denoted by the n×p matrix **X**. Let C\=X′X and V\=diag(ri2/(1−hii)) (i\=1,…,n), where hii\=xi(X′X)−1xi′, xi is the *i*th row of **X** and ri\=Yi−Yˆi (i\=1,…,n) are the residuals. As done in Section 10.13.15, let *k* denote the bias parameter used by the ridge estimator and let

(11.4)S(k)\=(C+kIp)−1X′VX(C+kIp)−1.

Wilcox (2019a) notes that sjj(k), the *j*th diagonal element of S(k), estimates the squared standard error of βˆj(k) and suggests testing H0: βj\=0 (j\=1,…,p) using the test statistic

(11.5)Tj\=βˆjsjj,

where the null distribution is approximated with a Student's t distribution, with n−p−1 degrees of freedom. The familywise error rate is controlled via Hochberg's method. If any of these *p* hypotheses is rejected, reject the global hypothesis given by Eq. (11.1). This is reasonable because when Eq. (11.1) is true, the ridge estimator is unbiased. But otherwise it is biased, in which case, any confidence interval based on Eq. (11.5) can be highly inaccurate. It remains unknown how to compute confidence intervals for the individual slopes based on the ridge estimator when one or more differ from zero. In practical terms, if H0: βj\=0 is rejected for any *j*, reject (11.1) but make no inferences about which slopes differ from zero.

#### Method RT2

Now consider a robust ridge estimator β˜ given by Eq. (10.19). Again the goal is to test Eq. (11.1). Consider the test statistic

(11.6)TR2\=p(n−1)n−pβ˜S−1β˜′,

which is an analog of Hotelling's T2 statistic. An approach to controlling the Type I error probability is to momentarily assume homoscedasticity, the error term has a normal distribution, and the independent variables have a multivariate normal distribution, with all correlations equal to zero. Then, for a given sample size, a simulation can be used to determine the null distribution, which yields a critical value. The issue is whether this critical value controls the Type I error probability reasonably well when dealing with an error term that has a non-normal distribution and when there is heteroscedasticity. Simulations reported by Wilcox (2019b) indicate that when using a robust ridge estimator, with βˆR in Eq. (10.19) taken to be the Theil–Sen estimator, reasonably good control of the Type I error probability is achieved. The MM-estimator performs nearly as well, but in some situations, the actual level was found to be well above the nominal level when leverage points are retained. When leverage points are removed, the actual level was found to be less than or equal to the nominal level, but in some cases, it is less than 0.025 when testing at the 0.05 level. In terms of power, TR2 does not dominate Eq. (11.2), but generally TR2 competes well with Eq. (11.2). Extant simulations indicate that Eq. (11.2) never offers a striking advantage, but TR2 can offer a distinct advantage even when there is little or no indication of multicollinearity (cf. Spanos, 2019).

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780128200988000178)

URL: https://www.sciencedirect.com/science/article/pii/B9780128200988000178

## [Multiple Regression](https://www.sciencedirect.com/science/article/pii/B9780128200254000129)

Andrew F. Siegel, Michael R. Wagner, in [Practical Business Statistics (Eighth Edition)](https://www.sciencedirect.com/book/9780128200254/practical-business-statistics), 2022

### Summary

Explaining or predicting a single *Y* variable from *two or more X* variables is called **multiple regression**. The goals of multiple regression are (1) to describe and understand the relationship, (2) to forecast (predict) a new observation, and (3) to adjust and control a process.

The **intercept or constant term**, *a*, gives the predicted (or “fitted”) value for *Y* when *all X* variables are zero. The **regression coefficient**, *b**j*, for the *j*th *X* variable specifies the effect of *X**j* on *Y* after adjusting for the other *X* variables; *b**j* indicates how much larger you expect *Y* to be for a case that is identical to another except for being one unit larger in *X**j*. Taken together, these regression coefficients give you the **prediction equation** or **regression equation**, predicted *Y* = *a* + *b*1 *X*1 + *b*2 *X*2 + … + *b**k**X**k*, which may be used for prediction or control. These coefficients (*a*, *b*1, *b*2, …, *b**k*) are traditionally computed using the method of *least squares*, which minimizes the sum of the squared prediction errors. The **prediction errors** or **residuals** are given by \[*Y* − (Predicted *Y*)\].

There are two ways of summarizing how good the regression analysis is. The **standard error of estimate**, *S**e*, indicates the approximate size of the prediction errors. The **coefficient of determination**, *R*2, indicates the percentage of the variation in *Y* that is “explained by” or “attributed to” the *X* variables.

Inference begins with the ***F* test**, an overall test to see if the *X* variables explain a significant amount of the variation in *Y*. If your regression is not significant, you are not permitted to go further. If the regression is significant, you may proceed with statistical inference using ***t* tests for individual regression coefficients**, which tell you whether a particular *X* variable has an effect on *Y* after adjusting (or controlling) for the other *X* variables (ie, holding them constant). Confidence intervals and hypothesis tests for an individual regression coefficient will be based on its standard error, Sb1, Sb2, … or Sbk. The critical *t* value will have *n* − *k* − 1 degrees of freedom.

Inference is based on the multiple regression linear model, which specifies that the observed value for *Y* is equal to the population relationship plus independent random errors that have a normal distribution

Y\=(α+β1X1+β2X2+…+βkXk)+ε\=(Populationrelationship)+Randomness

where ε has a normal distribution with mean zero and constant standard deviation σ, and this randomness is independent from one case to another. For each population parameter (α, β1, β2, …, β*k*, σ), there is a sample estimator (*a, b*1, *b*2, …, *b**k*, *S**e*).

The hypotheses of the *F* test are as follows:

H0:β1\=β2\=…\=βk\=0H1:Atleastoneofβ1,β2,…,βk≠0

The result of the *F* test is determined by the *p*\-value as computed using statistical software, and may be interpreted as a test of whether the percent variation explained (the coefficient of determination, *R*2) is larger than we would expect due to randomness alone.

The confidence interval for an individual regression coefficient *b**j* is

Frombj−tSbjtobj+tSbj

where the critical *t* value has *n* − *k* − 1 degrees of freedom. The hypotheses for the *t* test of the *j*th regression coefficient are:

H0:βj\=0H1:βj≠0

There are two approaches to the difficult problem of deciding which *X* variables are contributing the most to a regression equation. The **standardized regression coefficient**, biSXi/SY, represents the expected change in *Y* due to a change in *X**i*, measured in units of standard deviations of *Y* per standard deviation of *X**i*, holding all other *X* variables constant. If you don’t want to adjust for all other *X* variables (by holding them constant), you may compare the absolute values of the correlation coefficients for *Y* with each *X* instead.

There are some potential problems with a multiple regression analysis:

The problem of **multicollinearity** arises when some of your explanatory (*X*) variables are too similar to each other. The individual regression coefficients are poorly estimated because there is not enough information to decide *which one* (or more) of the variables is doing the explaining. You might omit some of the variables or redefine some of the variables (perhaps using ratios) to distinguish them from one another.

The problem of **variable selection** arises when you have a long list of potentially useful explanatory *X* variables and would like to decide which ones to include in the regression equation. With too many *X* variables, the quality of your results will decline because information is being wasted in estimating unnecessary parameters. If one or more important *X* variables are omitted, your predictions will lose quality due to missing information. One solution is to include only those variables that are clearly necessary, using a prioritized list. Another solution is to use an automated procedure such as *all subsets* or *stepwise regression.*

The problem of **model misspecification** refers to the many different potential incompatibilities between your application and the multiple regression linear model. By exploring the data, you can be alerted to some of the potential problems with nonlinearity, unequal variability, or outliers. However, you may or may not have a problem: Even though the histograms of some variables may be skewed, and even though some scatterplots may be nonlinear, the multiple regression linear model might still hold. The *diagnostic plot* can help you decide when the problem is serious enough to need fixing. Another serious problem arises if you have a time series; it may help to do multiple regression using the percent changes from one period to the next in place of the original data values for each variable.

The **diagnostic plot** for multiple regression is a scatterplot of the prediction errors (residuals) against the predicted values, and is used to decide whether you have any problems in your data that need to be fixed. In particular, if you find a cloud of points that do not tilt either up or down, then this suggests that there is no additional structure easily found in your data and that the regression model is working well. Do not intervene unless the diagnostic plot shows you a clear and definite problem.

There are three ways of dealing with nonlinearity and/or unequal variability: (1) transform some or all variables, (2) introduce a new variable, or (3) use nonlinear regression. If you transform, each group of variables that is measured in the same basic units should probably be transformed in the same way. If you transform some of the *X* variables but do not transform *Y*, then most of the interpretation of the results of a multiple regression analysis remains unchanged. If you use the natural logarithm of *Y*, then *R*2 and significance tests for individual regression coefficients retain their usual interpretation, individual regression coefficients have similar interpretations, and a new interpretation is needed for *S**e*.

The **elasticity** of *Y* with respect to *X**i* is the expected *percentage* change in *Y* associated with a 1% increase in *X**i*, holding the other *X* variables fixed; the elasticity is estimated using the regression coefficient from a regression analysis using the natural logarithm of both *Y* and *X**i*.

Another way to deal with nonlinearity is to use **polynomial regression** to predict *Y* using a single *X* variable together with some of its powers (*X*2, *X*3, etc.).

Two variables are said to show **interaction** if a change in both of them causes an expected shift in *Y* that is different from the sum of the shifts in *Y* obtained by changing each *X* individually. Interaction is often modeled in regression analysis by using a *cross-product*, formed by multiplying one *X* variable by another, which defines a new *X* variable to be included along with the others in your multiple regression. Interaction can also be modeled by using transformations of some or all of the variables.

An **indicator variable** (also called a *dummy variable*) is a quantitative variable consisting only of the values 0 and 1 that is used to represent qualitative categorical data as an explanatory *X* variable. The number of indicator variables used in multiple regression to replace a qualitative variable is *one less* than the number of categories. The remaining (omitted) category defines the *baseline.* The baseline category is represented by the constant term in the regression output, and regression coefficients for the included indicator variables measure the effect from this baseline. Instead of using indicator variables, you might compute separate regressions for each category. This approach provides a more flexible model with different regression coefficients for each *X* variable for each category.

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780128200254000129)

URL: https://www.sciencedirect.com/science/article/pii/B9780128200254000129

## [Statistics, Multivariate](https://www.sciencedirect.com/science/article/pii/B0122274105007316)

David L. Banks, Stephen E. Fienberg, in [Encyclopedia of Physical Science and Technology (Third Edition)](https://www.sciencedirect.com/referencework/9780122274107/encyclopedia-of-physical-science-and-technology), 2003

### III.B Multicollinearity

A potential difficulty in linear regression is that the rows of the data matrix ***X*** are sometimes highly correlated. This is called multicollinearity; it occurs when the explanatory variables lie close to a line or plane or other proper subspace of R*p*. If carried to the extreme of perfect correlation, this implies that the covariance matrix ***X****T*Σ − 1***X*** is not invertible, and thus the parameter estimates in (3) cannot be obtained. Multicollinearity is a common problem in observational studies, but can usually be entirely avoided in carefully designed experiments.

As an example, suppose the dependent variable is the compressive strength of an aluminium can and the explanatory variables include indices of the bowing in the can walls, obtained from both a dial gauge and a coordinate measuring machine. These two values are so highly correlated as to be almost perfectly redundant, causing multicollinearity. Similarly, multicollinearity will occur when the explanatory variables are near perfect linear functions of other explanatory variables. In chemical engineering, this happens when several explanatory variables are the proportions of additives in a mixture. If the sum of all proportions must equal one, then there is perfect correlation and the covariance matrix is singular. If one avoids this by excluding one of the proportions, then it can still happen that the excluded variable shows very little variation, inducing multicollinearity.

Conceptually, multicollinearity implies that there is less information in the sample than one would expect, given the number of measurements taken. The inferential impact of this is that the estimate θˆ is unstable, so that small perturbations in the data cause large changes in the inference. Consequently, predictions based on the fitted model can be very bad.

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B0122274105007316)

URL: https://www.sciencedirect.com/science/article/pii/B0122274105007316

## [Volume 3](https://www.sciencedirect.com/science/article/pii/B9780444527011000806)

M. Hubert, in [Comprehensive Chemometrics](https://www.sciencedirect.com/referencework/9780444527011/comprehensive-chemometrics), 2009

### 3.07.5.1 PCR and PLSR

When the number of independent variables *p* in a regression model is very large or when the regressors are highly correlated (this is known as multicollinearity), traditional regression methods such as ordinary least squares tend to fail.

An important example in chemometrics is multivariate calibration, whose goal is to predict constituent concentrations of a material based on its spectrum. Since a spectrum typically ranges over a large number of wavelengths, it is a high-dimensional vector with hundreds of components. The number of concentrations, on the other hand, is usually limited to at most, say, five. In the univariate approach, only one concentration at a time is modeled and analyzed. The more general problem assumes that the number of response variables *q* is larger than one, which means that several concentrations are to be estimated together. This model has the advantage that the covariance structure between the concentrations is also taken into account, which is appropriate when the concentrations are known to be strongly intercorrelated with each other. As argued in Martens and Naes,82 the multivariate approach can also lead to better predictions if the calibration data for one important concentration, say *y*1, are imprecise. When this variable is highly correlated with some other constituents that are easier to measure precisely, then a joint calibration may give better understanding of the calibration data and better predictions for *y*1 than a separate univariate calibration for this analyte. Moreover, the multivariate calibration can be very important to detect the outlying samples that would not be discovered by separate regressions. Here, we will write down the formulas for the general multivariate setting (8) for which *q* ≥ 1, but they can of course be simplified when *q* = 1.

PCR and partial least squares regression (PLSR) are two methods frequently used to build regression models in very high dimensions. Both assume that the linear relation (8) between the *x*\- and *y*\-variables is a bilinear model that depends on *k* scores t˜i:

(21)xi\=x―+Pp,kt˜i+fi

(22)yi\=y―+Aq,kti˜T+gi

with x― and y― the mean of the *x*\- and *y*\-variables.

Typically *k* is taken much smaller than *p*. Consequently, both PCR and PLSR first try to estimate the scores t˜i. Then, a traditional regression can be used to regress the response *y* onto these low-dimensional scores. To obtain the scores, one can perform PCA on the independent variables. This is the idea behind PCR. In this case, no information about the response variable is used when reducing the dimension. Therefore, PLSR is sometimes more appropriate, as this method estimates the scores maximizing a covariance criterion between the independent and dependent variables. In any case, the original versions of both PCR and PLSR strongly rely on CPCA and regression methods, making them very sensitive to outliers.

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780444527011000806)

URL: https://www.sciencedirect.com/science/article/pii/B9780444527011000806

## [Linear Regression](https://www.sciencedirect.com/science/article/pii/B9780123694928500182)

Ronald N. Forthofer, … Mike Hernandez, in [Biostatistics (Second Edition)](https://www.sciencedirect.com/book/9780123694928/biostatistics), 2007

### 13.4.4 Multicollinearity Problems

In a multiple regression situation, it is not uncommon to have independent variables that are interrelated to a certain extent especially when survey data are used. *Multicollinearity* occurs when an explanatory variable is strongly related to a linear combination of the other independent variables. Multicollinearity does not violate the assumptions of the model, but it does increase the variance of the regression coefficients. This increase means that the parameter estimates are less reliable. Severe multicollinearity also makes determining the importance of a given explanatory variable difficult because the effects of explanatory variables are confounded.

Recognizing multicollinearity among a set of explanatory variables is not necessarily easy. Obviously, we can simply examine the scatterplot matrix or the correlations between these variables, but we may miss more subtle forms of multicollinearity. An alternative and more useful approach is to examine what are known as the *variance inflation factors* (*VIF*) of the explanatory variables. The *VIF* for the *j*th independent variable is given by

VIFj\=11\-Rj2

where *R*2*j* is the *R*2 from the regression of the *j*th explanatory variable on the remaining explanatory variables. The *VIF* of an explanatory variable indicates the strength of the linear relationship between the variable and the remaining explanatory variables. A rough rule of thumb is that the *VIF*s greater than 10 give some cause for concern.

Now let us review the multiple regression results shown in Tables 13.10 and 13.11. The *VIF*s shown in these tables are all less than 10, indicating that the multicollinearity does not pose a serious problem for those models. As a demonstration for a severe multicollinearity, we added to the model shown in Table 13.10 another independent variable that is closed associated with weight and height. Table 13.12 shows the multiple regression analysis of SBP on weight, age, height, and the body mass index (BMI) defined as your weight in kilograms divided by the square of your height in meters. The *VIF*s for weight, height, and BMI are all greater than 10 in Table 13.12. More important, the variances of the regression coefficients for weight and height increased, and these variables are no longer statistically significant. The effect of weight on SBP shown in the earlier model cannot be demonstrated if we add BMI. A solution to a severe multicollinearity is to delete one of correlated variables. If we drop the BMI variable, we would eliminate the extreme multicollinearity.

Table 13.12. Multiple regression analysis III: Systolic blood pressure versus weight, age, height, body mass index.

| Predictor | Coef | SE Coef | T | *p* | VIF |
| --- | --- | --- | --- | --- | --- |
| Constant | 105.2 | 154.4 | 0.68 | 0.499 |  |
| Weight | 0.3052 | 0.4413 | 0.69 | 0.493 | 97.6 |
| Age | 0.4364 | 0.1333 | 3.27 | 0.002 | 1.2 |
| Height | − 0.354 | 2.246 | − 0.16 | 0.875 | 22.3 |
| BMI | − 1.040 | 3.016 | − 0.34 | 0.732 | 60.9 |
| S = 13.90 | R − Sq = 37.8% | R − | Sq(adj) = 32.3% |  |  |
| **Analysis of Variance:** |  |  |  |  |  |
| **Source** | **DF** | **SS** | **MS** | ***F*** | ***p*** |
| Regression | 4 | 5,289.4 | 1,322.4 | 6.85 | &lt; 0.001 |
| Residual Error | 45 | 8,691.4 | 193.1 |  |  |
| Total | 49 | 13,980.9 |  |  |  |
| **Source** | **DF** | **Seq SS** |  |  |  |
| Weight | 1 | 3,021.9 |  |  |  |
| Age | 1 | 2,182.6 |  |  |  |
| Height | 1 | 61.9 |  |  |  |
| BMI | 1 | 23.0 |  |  |  |

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780123694928500182)

URL: https://www.sciencedirect.com/science/article/pii/B9780123694928500182

## [Multiple Regression](https://www.sciencedirect.com/science/article/pii/B9780128230435000084)

Donna L. Mohr, … Rudolf J. Freund, in [Statistical Methods (Fourth Edition)](https://www.sciencedirect.com/book/9780128230435/statistical-methods), 2022

### 8.7.2 Other Methods

Another approach is to perform multivariate analyses such as principal components or factor analysis on the set of independent variables to obtain ideas on the nature of the multicollinearity. These methods are beyond the scope of this book (see Freund *et al.*, 2006, Section 5.4).

An entirely different approach is to modify the method of least squares to allow biased estimators of the regression coefficients. Some biased estimators effectively reduce the effect of multicollinearity so that, although the estimates are biased, they have a much smaller variance and therefore have a larger probability of being close to the true parameter value. One such biased regression procedure is called ridge regression (see Freund *et al.*, 2006, Section 5.4).

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780128230435000084)

URL: https://www.sciencedirect.com/science/article/pii/B9780128230435000084

## [Numerical Prediction](https://www.sciencedirect.com/science/article/pii/B9780124166325000104)

Robert Nisbet Ph.D., … Ken Yale D.D.S., J.D., in [Handbook of Statistical Analysis and Data Mining Applications (Second Edition)](https://www.sciencedirect.com/book/9780124166325/handbook-of-statistical-analysis-and-data-mining-applications), 2018

### Collinearity Among Variables in a Linear Regression

When two variables are highly correlated to each other, the plots of these variables lie on nearly the same line. The total of all the collinearity between variable pairs is called *multicollinearity.* You can assess this effect by comparing the square of the sum of the Pearson simple correlation coefficients for all variables with the coefficient of determination (*R*2). The *R*2 value measures the combined effect of all the variables in explaining the variance in the dependent (response) variable. The Pearson simple correlation coefficients measure the degree of correlation between a single variable and the dependent variables. The degree to which the squared sum of the simple correlation coefficients exceeds the *R*2 value is a measure of the amount of collinearity between the variables. Relatively high multicollinearity in a regression analysis will make it difficult if not impossible for the algorithm to find a single optimum solution. Because the interacting effects vary with the values in the variables, there may be several “optimum” solutions, depending on the relative frequencies of values among collinear variables. A good rule of thumb to follow in parametric statistical analysis is to eliminate one member of any pair of variables that is more than 80% correlated with the other. The other suggestion we can make is to limit the number of interaction variables to only those that are obvious.

[Read full chapter](https://www.sciencedirect.com/science/article/pii/B9780124166325000104)

URL: https://www.sciencedirect.com/science/article/pii/B9780124166325000104
