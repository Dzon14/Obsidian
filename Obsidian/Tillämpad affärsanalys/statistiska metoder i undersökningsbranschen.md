---
tags:
  - affärsanalys
---
# Statistiska metoder i undersökningsbranschen

## Statistics
![[Pasted image 20240130132337.png|500]]
- ”The science of analyzing and drawing conclusions from data.” 
- ”... the discipline that involves the collection, analysis, interpretation and presentation of data.” 
- With data, we mean information that is sampled from an underlying population. 
- We can use methods from probability and inference theory assuming randomness in the sample.
- Other methods, primarily descriptive statistics and exploratory modelling can be used for non-random samples.

## Statistical methods used in marketing research
- se [[analystekniker]]

#### [[chi-square test]]
- Determine the strength of relationships between qualitative variables
- Compare an observed distribution with an expected theoretical distribution.
#### [[regressionsanalys]]
- Independent variables ($X_{1},X_{2},...$) $\Rightarrow$ Dependent variable Y
- Estimate the effect of the independent variable(s) on the response $Y = f(x_{1},x_{2},..., x_{k}, \varepsilon)$
- Common estimation methods: Ordinary least squares and Maximum likelihood

#### Cluster analysis (segmenteringsanalys)
- Important for market research
- Grouping observations into meaningful homogenous clusters based on selected variables.
- Method: Measure the similarity (or distance) between points in the data space; then group the most similar points (those with smallest distances) into clusters. 
**Examples:** 
1) Based on consumption and perception data, the households are classified into various types of consumer groups.
2) Based on symptoms and other relevant clinical variables, the patients are classified according to severity groups, e.g. mild – primary – acute.

#### Discriminant analysis
- Assign observations into predefined groups on the basis of selected covariates. (for ex. mild - primary - acute , patient groups) 
- Determine which variables best predict group membership. 
- Method: For each observation, estimate its measure of belonging to each group on the basis of its values on the covariates. Assign the observation to the group with the corresponding highest measure.
**Examples:**
- Using marketing survey and/or behavioural data, assign consumers to the established consumer segments.
- Given observed symtomps and clinical data, the doctor wants to assign the patient to one of the 3 treatment groups (according to the severity of the condiition). 

#### Logistic regression
- Alternative to discriminant analysis for allocating to two classes.
- Used to estimate conditional probabilities given one or several predictors, to assign an observation to one of the two calsses.
**Examples:**
1. Logistic model for brand purchase (Yes, No) based on survey data on perceptions. 
2. How likely is a patient going to be in acute condition based on clinical variables and symptoms?

#### Conjoint analysis
- Survey-based method that determines how consumers value different attributes of a product or service 
- Can be used to predict consumers’ choice between several competing alternatives 
- Method: measure the consumers’ utility values of attributes or features in the choice between several products and services
**Example:** 
1. Purchasing a car entails many factors for consideration: brand, model, color, fuel consumption, taxation, etc. 
2. Prospective smart phone buyers value several characteristics differently: price, features, camera, memory, size, design, etc.

#### Factor analysis
- Used to reduce a large set of variables to a smaller set of underlying unobservable common factors
- Method: use a dimension reduction technique such as principal component approach (singular value decomposition) to find fewe dimensions which describe the variable. 
**Example:**
1. Given a set of statements describing consumption practices, one would like to check if these statements can be grouped under various factors. 
2. Based on qualitative studies, 60 Likert statements were used in a survey used to describe brand equity. It is of interest to see if these statements are connected through underlying dimensions.

#### Multidimensional scaling (MDS)
- A graphical/visualization method that shows the degree of similarity between sets of stimuli (e.g., brands and companies)
- Method: given information about tue similarities between points, create a map of the relative positions of points in a low-dimensional Cartesian space
**Example:**
1. Market positioning of brands
2. Image placements of companies

#### Correspondence analysis
- Is "replacing" MDS.
- Used as an exploratory method to visualize relationships among 2 sets of categorical variables (e.g. brands and features)
- Method: Obtain the correspondence between rows and columns in a cross-tabulation or multiple frequency table. 
**Example:**
1. Positioning of brands and features
2. Placements of companies and image attributes

#### Turf analysis
- ”Total Unduplicated Reach and Frequency”
- Determine the market potential for a set of product alternatives by estimating the increment number of potential buyers for each product alternative. 
- Can also be used for media campaigns to estimate the share of customers who heard about the product through different media channels.
**Example:**
- A company has 10 candidate product offers or alternatives, and the marketing manager would like to know which subset of 5 alternatives has the largest aggregation of potential customers

#### Attribute position analysis
- Graphical classification of product or service attributes or features according to satisfaction and importance 
- Which product attributes are the key drivers for purchases? Which features need improvement? 
- Helps formulate strategies for better use of resources in improving the product, by looking into the importance and performance figures for the attributes
**Example:**
- A company wants to improve the image of its premium product to stimulate further sales using 10 key features. Which features are important for sales and which attributes need improvement?

## [[measurement scales]]
- [[chi-square test]]
- [[cross-tabulation]]

## Visualization: some examples of graphs

#### Boxplot: Internet usage and Usage of internet banking
![[Pasted image 20240130151449.png|550]]
**5-värdes-analysen:** min, max (range), $Q_{1}$, $Q_{2}$ (median) och $Q_{3}$

#### HATCO data: histograms for two groups with several levels
![[Pasted image 20240130154015.png|500]]

#### HATCO data: density histograms for two groups
$X_{1}$ (delivery speed) for $X_{8}$ (firm size)
![[Pasted image 20240130154348.png|500]]

## HATCO data: scatterplot for two groups
$X_{10}$ (satisfaction level) for $X_{8}$ (firm size)
![[Pasted image 20240130154456.png|500]]

## [[enkel linjär regression]]
![[Pasted image 20240130155132.png]]
##### Estimation in simple linear regression
![[Pasted image 20240130155732.png]]
![[Pasted image 20240130155748.png]]

#### What does simple linear regression estimate?
![[Pasted image 20240130155811.png]]
Simple linear regression is an estimation of the conditional mean given the value of the explanatory variable.

#### Analysis of variance (ANOVA)
![[Pasted image 20240130162424.png|500]]
![[Pasted image 20240130162443.png|600]]

#### Measures of dependence and goodness-of-fit
![[Pasted image 20240130163150.png]]
- För marknadsundersökningar är det svårt att få en hög förklaringsgrad ($R^{2}$), till och med 0,3 är bra (till skillnad från i fysik där man strävar mot 1).

#### SPSS HATCO regression output
![[Pasted image 20240130163827.png|500]]
#### Simple linear regression assumptions
![[Pasted image 20240130163900.png]]

#### Simple linear regression diagnostics
Ocular inspection of homoscedasticity (constancy of variance) Plot the residuals against the predicted Y values.
![[Pasted image 20240130163935.png]]
- Lägre varians för lägre X?
- Lösningar för en icke-konstant varians:
	- Variansstabiliserande transformation
	- Flera observationer vid varje sample

**How to check for normality of errors;** $\varepsilon \approx N(0, \sigma_{\varepsilon}^{2})$
(Normalfördelat?)
- Normal plot: shows the quantiles of the residuals against the quantiles of the normal distribution. Should the points fall close to or on the diagonal line, the residuals follow a normal distribution. 
- Overlay a normal probability distribution function over the histogram of the residuals. Check if the histogram follows the normal contour
![[Pasted image 20240130164405.png]]
The residuals seem to be approximately *Normal distributed*.

**How to check for outliers and influential cases:**
![[Pasted image 20240130164453.png|600]]
![[Pasted image 20240130164617.png|400]]
- Four observations seem worth looking closer at (and perhaps remove).