# human_activity_recognition
Human Activity Recognition from triaxial Accelerometer Data captured through iPhone 12 mini

# Abstract
Activity Recognition describes a broader research filed that aims to recognize an agents motions from sensor data. It was formulated as a classification problem in 2005 by a group of researchers at the State University of New Jersey. In a laboratory setting test subjects were performing various activities such as walking, sitting, or standing while being equipped with a triaxial accelerometer. The captured motion data was then used to train and evaluate a set of classification algorithms available at that time such as, K-nearest Neighbour, Naïve Bayes, or Hidden Markov (Ravi et al., 2005).

Through the introduction of smart phones in the early 2000s, the accelerometer have found their ways to billions of users. Ever since, the collection  of such gyroscope data has become more convenient and inexpensive. The availability of free applications to and interfaces to extract motion data from smartphones has boosted the research field. One of the many replications of Ravi’s experiment using smart phone data was conducted by Kwapisz et al. at Fordham University. Similarly, 35 test subjects captured triaxial accelerometer data while performing various activities. The publicly available data set is the source of the inspiration for this term project (Kwapisz et al., 2010).

To gain a full understanding of the end-to-end data collection process, a small-scaled self-experiment is conducted, were the author replicated the experiment using the accelerometer of an iPhone 12 mini.The data that was captured reflects the motions when walking, running, sitting, standing, laying, stairs climbing and descending. The decision tree used for classifying the achieved a high accuracy of 99%, which however, may also be the result of including only one single test subject. Nevertheless, when looking at the feature importance, it was found that especially the 75% quartile of the accelerometers X- and Y-axis largely contribute to the classification accuracy.

**Data Collection**

the phone was carried in the front right leg pocket, as the data was collected at a rate of 20Hz, which means that 20 data points are captured per second by each axis. The extracted csv files are then pre-processed by slicing them into overlapping time windows of size 30 so that for each activity between 300 and 500 observations are generated. For each axis in each observation the statistical measurements are calculated. However, they slightly differ from the research data frame as they contain quartiles, global maxima and minima.


**Mobile App for Accelerometer Data Capturing**

https://apps.apple.com/us/app/accelerometer/id499629589

**References**

Kwapisz, J. R., Weiss, G. M., & Moore, S. A. (2010). Activity recognition using cell phone accelerometers. Proceedings of the Fourth International Workshop on Knowledge Discovery from Sensor Data, 10–18.
Ravi, N., Dandekar, N., Mysore, P., & Littman, M. (2005). Activity Recognition from Accelerometer Data. 3, 1541–1546.
