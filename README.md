
# A step-by-step guide on AWS AutoPilot

## Why AutoML?
In many use cases and scenarios machine learning is a great tool for some key users but they probably are not ready to apply it. Their knowledge on the problem and the data can be very rich and can produce very helpful insights for businesses, but they do not know enough about ML methodology nor feature engineering to work in a machine learning workflow. AutoML will help them to extend their knowledge domain, allowing them to apply some classification or regression models on a dataset and reaching some good results with no relevant effort. 

AutoML is related to produce machine learning solutions without doing data science tasks like data processing, feature selection, model selection, model training and deploying. Some AutoML tools are intended to boost the performence of our ML experiments on a dataset, using very advanced techniques and data preprocessing tasks but some others are focused on bringing the ML experience to a user in just a few clicks producing an initial model, a baseline model. But later the user or a more advanced user can improve the ML workflow and compare the performance of new experiments to the baseline model.

As machine learning is getting more and more attention, these tools have become a must in the portfolio of the great tech companies like Amazon Web Services. 

## Introduction about Amazon SageMaker AutoPilot
Amazon SageMaker package contains the AutoPilot toolkit, a very easy and simple framework to launch AutoML projects. You just need a bunch of data files, choose your target feature and wait for AutoPilot to process your data and return a predictive model with a good enough performance. Even you can deploy the model in one click, providing your users with a REST service to test your solution.

But behind the doors, AutoPilot analyzes your data, identifies which kind of problem are you facing, then processes, transforms and selects the most relevant features and finally runs hundreds of experiments, tunes many models with different parameters and data processing strategies. It generates an inference pipeline you can deploy to predict and solve your problem. 
One of the most interesting features of AutoPilot is the visibility in the data processing and model tuning stages it provides. You can get two notebooks: one for the data analysis and another one for data processing, model building and tuning process. As a result, you can analyze and include your own techniques or knowledge to the notebooks and even run your own experiments trying to outperform the results

## Problem Statement
We will guide you on how to use AWS AutoPilot in SageMaker, using the Studio UI or the SDK. We will show its features and capabilities, and all the artifacts and outputs you can get from an AutoPilot job.

## Dataset
For this example, we download a dataset from Kaggle, Bank Marketing, "The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit (variable y).", Kaggle Bank Marketing dataset description.

This dataset is publicly available for research. The details are described in:
[Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, In press, http://dx.doi.org/10.1016/j.dss.2014.03.001

We are not going to process the dataset, we have just downloaded it and uploaded it to an Amazon S3 bucket, splitting it in two sets: train and test. The train dataset contains about 38,000 records and the test set 3,000. It is required to store the data in CSV format in S3 for AutoPilot to use it. You can upload it from the S3 console in AWS or using AWS CLI or a notebook and the SageMaker SDK.

## Notebooks

The Jupyter notebook, **Train_deploy_test_AutoPilot_job** describes how to launch an AutoPilot job using SageMaker SDK, deploy an endpoint and make predictions for a test dataset. 

## License
This repository is under the GNU General Public License v3.0.

This repository was developed by Eduardo Muñoz Sala 