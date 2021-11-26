# human_activity_recognition
Human Activity Recognition from triaxial Accelerometer Data captured through iPhone 12 mini

# Abstract
Activity Recognition describes a broader research field that aims to recognize an agents' motions from sensor data. It was formulated as a classification problem in 2005 by a group of researchers at the State University of New Jersey. In a laboratory setting, test subjects performed various activities such as walking, sitting, or standing while equipped with a triaxial accelerometer. The captured motion data was then used to train and evaluate a set of classification algorithms available at that time, such as K-nearest Neighbour, Naïve Bayes, or Hidden Markov (Ravi et al., 2005).
	
  Through the introduction of smartphones in the early 2000s, the accelerometer has found its way to billions of users. Ever since, the collection of such gyroscope data has become more convenient and inexpensive. In addition, the availability of free applications and interfaces to extract motion data from smartphones has boosted the research field. One of the many replications of Ravi’s experiment using smartphone data was conducted by Kwapisz et al. at Fordham University. Similarly, 35 test subjects captured triaxial accelerometer data while performing various activities. The publicly available data set is the source of inspiration for this term project (Kwapisz et al., 2010).
	
  During the initial phase of this project, the records are investigated using principal component analysis in combination with silhouette score. Both methods provide an indication of which activities are more or less likely to be classified accurately. Walking and stair-climbing were found to pose the most significant challenge for classification. In a second stage, the data is used to train and evaluate the following six classification models: Decision Tree, Random Forest, Logistic Regression, Gaussian Naïve Bayes, and Support Vector. The best results were achieved using the random forest classifier, as it reached an accuracy of 92%.
	
  To fully understand the end-to-end data collection process, a small-scaled self-experiment is conducted, where the author replicated the experiment using the accelerometer of an iPhone 12 mini. Like the data mentioned earlier, the captured data reflects the motions when walking, running, sitting, standing, lying, stairs climbing, and descending. The decision tree used for classifying the achieved a high accuracy of 99%, which may also be the result of including only one test subject. Nevertheless, when looking at the feature importance, it was found that the 75% quartile of the accelerometers X- and Y-axis largely contributes to the classification accuracy. Since Kwapisz et al. did not use these metrics, this finding may contribute to the research discipline of activity recognition. Ultimately, this project demonstrates how motion-sensing experiments can be conducted with little effort and few resources nowadays.


**Data Collection**
the phone was carried in the front right leg pocket, as the data was collected at a rate of 20Hz, which means that 20 data points are captured per second by each axis. The extracted csv files are then pre-processed by slicing them into overlapping time windows of size 30 so that for each activity between 300 and 500 observations are generated. For each axis in each observation the statistical measurements are calculated using the pandas function df.describe().


**Mobile App for Accelerometer Data Capturing**

https://apps.apple.com/us/app/accelerometer/id499629589

**References**

Kwapisz, J. R., Weiss, G. M., & Moore, S. A. (2010). Activity recognition using cell phone accelerometers. Proceedings of the Fourth International Workshop on Knowledge Discovery from Sensor Data, 10–18.

Ravi, N., Dandekar, N., Mysore, P., & Littman, M. (2005). Activity Recognition from Accelerometer Data. 3, 1541–1546.
