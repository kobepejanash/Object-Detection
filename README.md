# STAT-154-Project-2
The repository of project 2 from class STAT 154, with all the necessary plots, texts and other types of information.

- Discription：

	In this project, we explore the properties of the cloud data by looking into their correlations and plots. The other main goal is to find classifiers that fit the data best and identify the labels accurately. This can help us effectively distinguish the cloud-free region from the clouds, by classifying the labels of data.


- Contents:

   1. Data Collection and Exploration
   
      (a)Paper Summary
      
      (b)Data Summary & Plots
        
      (c)EDA
      
   2. Preparation
   
      (a)Data Splitting
      
      (b)Trivial Classifier
       
      (c)"Best Features"
       
      (d)CVgeneric Function
      
   3. Modeling
      
      (a)Classification Methods on CV
      
      (b)ROC Analysis
      
      (c)PR Curve Analysis
      
   4. Diagnostics
     
      (a)Analysis of Classificatoin Models
     
      (b)Analysis of Misclassification Errors
     
      (c)Better Classifier/Features
     
      (d)Splitting Modification
     
      (e)Conclusion
     
   5. Contributions and Credits
      
      (a)Contributions
      
      (b)Sources of References

- Procedure:

	First, we plot the cloud data and observe if there’s any pattern associated with a certain distribution. From the figures, we conclude that the cloud data isn’t identically and independently distributed across the three images, but the cloud itself follows i.i.d. in each of the image. Next, we develop two different methods of splitting that doesn’t violate the conclusion before. 
	

	We then find the three physical features to be the best predictors, due to their high associations with each labels. After knowing the characteristics of the data, we fit a variety of classification methods and select the best ones based on their algorithms and performances. After trying methods including Neural Network, QDA and Adaboost, we gather their results and do a series of in-depth analysis, such as parameter convergence. In the end, we find the Random Forest to be the best predictor of cloud data, and the GBM to be the second best in this case. They not only have the highest test accuracy(95.9%) among all, but also avoid issues like overfitting. 


	Next, we continue improving the Random Forest method by finding better features. We try increasing the power of each features and find their squares to be the better features: x2, y2, NDAI2, CORR2, and SD2. 


- Conclusion:

	Nonetheless, this doesn’t suggest that the Random Forest is a perfect classifier. It still has limited test accuracy and feature improvement, as shown in 4(c). The reason for its accurate fit to the cloud data is that the dataset already meets the assumption for Random Forest method. Therefore, it is possible that this algorithm may not work well for other types of dataset. 

	To summarize, there’s no perfect algorithm that can do classification with 100% test accuracy. All we can do is by following the PQRS principle, to make sure that the model is in accordance with the population and question in the domain, with the representativeness of samples and scrutiny of the process.
