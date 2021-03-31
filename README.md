# Multi-class Classification Model

The aim of this project is to classify *E. coli* proteins using the amino acid sequences in their cell localization sites. This can be used to predict how a protein will bind to a cell based on its chemical composition before it is folded.

This project implements scikit-learn, pandas, seaborn, Matplotlib and NumPy.

### Data description

File name: [ecoli.csv](https://github.com/agolikova/Multi-class-classification-model/blob/main/ecoli.csv). This dataset was adapted from Kenta Nakai and Paul Horton's, used in their 1996 paper titled [“A Probabilistic Classification System For Predicting The Cellular Localization Sites Of Proteins”](https://pubmed.ncbi.nlm.nih.gov/8877510/).

The proteins belong to one of 5 classes:

* cp: cytoplasm
* im: inner membrane without signal sequence
* pp: periplasm
* imU: inner membrane, non cleavable signal sequence
* om: outer membrane

The input features are described as follows:

* mcg: McGeoch’s method for signal sequence recognition
* gvh: von Heijne’s method for signal sequence recognition
* lip: von Heijne’s Signal Peptidase II consensus sequence score
* chg: Presence of charge on N-terminus of predicted lipoproteins
* aac: Score of discriminant analysis of the amino acid content of outer membrane and periplasmic proteins
* alm1: Score of the ALOM membrane-spanning region prediction program
* alm2: Score of ALOM program after excluding putative cleavable signal regions from sequence

### Code

This project consisted of 2 parts:

#### Evaluate machine learning models

* Explore *E. coli* dataset
* Define a test harness for evaluating candidate models
* Evaluates the following ML models: 
  * Random Forest
  * k-Nearest Neighbours
  * Linear Discriminant Analysis
  * Support Vector Machine

#### Train & test data using chosen model

* Use model identified as having the best performance during model evaluation (random forest classifier)
* Trained & test model on *E. coli* dataset
* Visualize results of prediction as a confusion matrix
