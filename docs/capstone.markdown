---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Project Overview
permalink: /capstone/
---


## Abstract
In this study, we will be exploring the gut microbiome of Latin American immigrants to determine what factors of their gut microbiome affect metabolic diseases. The goal of our project is to determine what metabolic diseases/disorders an individual has based on their gut microbiome and other supporting information on the individual. To achieve our goal, we will be exploring machine learning and data analysis techniques to summarize the key points of the data and understand the patterns and relationships in the data. 

## Introduction
Metabolic diseases afflict millions of people in the US, with diseases such as diabetes, high blood pressure, and obesity affecting Latinos and other ethnic minority groups at a significantly higher rate. One factor contributing to this multifaceted disparity is the fact that minority groups are severely underrepresented in clinical research and health studies, resulting in a continued lack of insight and solutions for these groups. Our project seeks to further metabolic disease research and expand representation in such fields by studying how the gut microbiomes of Hispanic populations are correlated with the prevalence of certain diseases. As the field of gut microbiome research has grown, scientists have discovered links between gut microbiomes and diseases like diabetes and obesity, as well as differences in gut microbiomes by race and ethnicity (Duvallet, et al.; Ross, et al.). Machine learning solutions that can accurately determine these links and scale across diverse gut microbial populations could provide useful general and specific solutions for different diseases and different groups. As such, the main goal of our project is to use the Study of Latinos (SOL) gut microbiome dataset to implement and train machine learning models that can determine an individual’s metabolic disorders based on their gut microbiome. 

## Data Description
For the purposes of this project, we will be using the gut microbiome dataset collected by the Study of Latinos (SOL). The SOL is a population-based study of Hispanic/Latino adults from the ages of 18-74 who were selected from randomly sampled census block areas within Chicago, IL; Miami, FL; Bronx, NY; San Diego, CA (Lavange, et al.). The study focused on gathering information on the health status of the US Latino/Hispanic population in order to address the lack of research on minorities. For our project, we will be using 1835 self-collected stool samples that is broken into two main parts, (1) the frequency table of genomic sequences and (2) the metadata. The dataset is available on Qiita (https://qiita.ucsd.edu/) ID: 11666.

(1) A genomic sequence is the information given by an organism's DNA/RNA, each column in our frequency table corresponds to an organism's genomic sequence (in our case some sort of bacteria in our gut). The frequency table of genomic sequences counts the number of times that a unique genomic sequence appears in a sample. 

(2) The metadata contains information about the participants socioeconomic conditions, their country of origin, and their medical history which includes information about whether or not a given sample had a certain metabolic disease. A subset of the diseases will be selected as our classification targets and a few metadata columns such as age and gender will be used as features in addition to the entire feature table of genome sequences. 


## Exploratory Data Analysis
After dropping the samples with missing values and identifying the samples that existed in both the feature table and metadata, we found 1750 samples that we could use for our analysis.

We will then do some preprocessing on the amount of features (columns) of our feature table. We plotted the count/frequency of samples that each feature appears on in our feature table dataset. By looking at this plot we see that alot of our features have very low sample frequencies, which means that theres a lot of irrelevant features/columns that have little importance and could be dropped in our data. 

Insert Images/Plots here

Within the 1750 samples, we can see in the graph below, pre-cvd had by far the lowest presence within our dataset, indicating that there might be a large class imbalance within the pre-cvd colum. This class imbalance will need to be addressed in our pre-processing in order to prevent our model from overfitting.

Insert Plots Here 

After further data exploration, we found that many samples have varying amounts and varying combinations of diseases, as can be seen in the graph below, which means a binary classifier (predicting what disease someone has) would not work.

Insert plot here

## Machine Learning Models

## Results

## Dimensionality Reduction

## Model Performance

## Conclusion
Overall, due to the difficulty of multi-label classification tasks, the high count of disease co-occurence, the complexity of microbiome and disease research, and the lack of substantial/balanced data, the results yielded by our model has a lot of room for improvement. The low accuracy of our model suggests a different multi-label machine learning model or further data pre-processing may be required.

Even though our project did not yield our desired results, our project still contributes to the field of gut microbiome research by performing analysis with Python and commonly used Python packages, lowering the barrier of entry for other data scientists and equipping current researchers with new tools such as qiime2.
# References
