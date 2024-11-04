# MangoLeafBD

Project Title: MangoLeafBD Dataset Analysis and Classification Report

Introduction
Entails the identification and classification of plant diseases which timely diagnosis can either prevent the losses of crops or improve the quantity and quality of the entire harvest in agriculture. Mango (Mangifera indica) is one of the most popular tropical fruits, but it is also tragically susceptible to numerous leaf diseases that can negatively affect development and productivity. We have also developed a dataset, called MangoLeafBD, for the classification of mango leaf diseases consisting of 4,000 images organized into seven disease classes and one healthy class. The number of images for each class is 500 so that all classes are balanced. The images show from four separate orchards in Bangladesh, a variety of visual data, from healthy leaves to leaves with a specific type of disease.
This dataset enables both two-class (healthy vs. diseased) and multi-class (specific disease) classification tasks, which are essential for real-world disease management in mango cultivation. Machine learning models, especially those focused on image classification, can leverage the rich visual data in MangoLeafBD to learn and identify disease patterns. By automating this classification process, we can provide a powerful tool for early disease detection, which would assist farmers and agricultural professionals in making informed decisions for disease control and crop management.

Dataset Overview

The MangoLeafBD dataset comprises 4,000 images of mango leaves, organized into eight categories, representing seven diseases and one healthy condition. Each category contains 500 images of size 240x320 pixels, with images captured across four mango orchards in Bangladesh. This dataset supports both two-class (healthy vs. diseased) and multi-class (specific disease) classification tasks.
Part 1: Exploratory Data Analysis (EDA)
1. Data Overview
•	Total Images: 4,000
•	Image Dimensions: Standardized to 100x100 for analysis
•	File Format: JPG
2. Class Distribution
The dataset is balanced, with 500 images per class. Each category represents either a specific mango leaf disease or a healthy leaf condition. A balanced dataset ensures that all classes have equal representation, which is beneficial for training machine learning models effectively.

Class	Count
Anthracnose	500
Bacterial Canker	500
Cutting Weevil	500
Die Back	500
Gall Midge	500
Healthy	500
Powdery Mildew	500
Sooty Mould	500


3. Sample Visualization
Sample images from each category were displayed, giving insights into the visual differences among healthy and diseased leaves. This visualization highlights distinctive patterns, colors, and textures associated with each disease type, aiding in understanding the dataset visually before modeling.
4. Color Distribution
An analysis of color channels across sample images was conducted, showing that different diseases exhibit unique color intensities. This distinction suggests that color features may significantly impact model predictions.

Part 2: Model Training and Classification
To classify mango leaf diseases, we used two machine learning models:
1.	Decision Tree Classifier
2.	Random Forest Classifier

1. Data Preprocessing

	Image Normalization: All images were scaled to a [0, 1] range by dividing pixel values by 255.
	Label Encoding: Disease categories were encoded to numerical labels for model training.
	Train-Test Split: The dataset was divided into 80% training and 20% testing sets.

3. Model Training and Evaluation
   
Model 1: Decision Tree Classifier

	Accuracy: 0.68
	Classification Report:
	Precision, recall, and F1-scores were provided for each class.
	The model showed reasonable performance but struggled with some disease classes due to high variance.

Model 2: Random Forest Classifier

	Accuracy: 0.90
	Classification Report:

The Random Forest model outperformed the Decision Tree across all classes.
	Precision, recall, and F1-scores were notably higher, with Random Forest providing more stable and generalizable results due to its ensemble approach.
	Comparison: A bar chart was created to compare the accuracy of the Decision Tree and Random Forest models. The Random Forest model achieved higher accuracy, making it the preferred model for mango leaf disease classification.

Conclusion

The first step when we examined the dataset named MangoLeafBD is exploratory data analysis (EDA) where we found that those images are evenly perfectly distributed into eight categories with 500 images each. This balance during model training is useful, as it guarantees that all the disease types (and healthy leave) are equally represented helping to alleviate class bias in the model predictions. Upon comparing with sample images from each class, the crucial patterns, textures and color distributions related to different diseases were reinforced when visually examining the image classes. These properties indicate that the classes can be correctly learned and separated by a machine learning model as the categories have distinct visual characteristics.
As far as the model performances are concerned, Random Forest classifier is more accurate and stable than the Decision Tree model. With the ensemble approach of Random Forest, which combines the outputs of many decision trees, more robust decision boundaries can be created. The averaging helps mitigate overfit, a common issue with single Decision Tree models, particularly on tasks of this complexity.
In terms of model comparison, it is suggested a Random Forest classifier is appropriate mango leaf disease classification. It helps as well as it helps in generalizing better hence it can be more consistent on the unseen data. Such robustness allows Random Forest to be a good candidate for real world mango leaf disease detection applications as the accuracy of disease identification can be an important factor to consider.


