# What's Your Shade?
---

### Contents:

- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Data Sources](#Data-Sources)
- [Data Dictionary](#Data-Dictionary)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)
- [Requirements](#Requirements)
---

### Problem Statement:

Online shopping is a huge market. For individuals who wear make up, store closures have been a huge problem with testing and matching foundation shades. What if you don't need to go inside of a store to find a foundation that matches your skin tone? The purpose of this application is to match an individual to a shade of foundation sold by sephora or ulta (two of the biggest cosmetic stores within the United States) through image recognition. 



### Executive Summary

This application utilizes various technologies listed below. It begins by connecting to the individuals computer webcam and then snapping a picture of the individuals face. If webcam is not assesible , an individual can upload an image in the form of .jpg or png.  It then recognizes which regions in the picture are indicative of skin color and extracts the pixel-based color and finds the dominant colors. It does this through naive Bayes Classifier using the Guassian Distribution. After extracting the colors in the form of RGB, the values are then compared to a dataset with over 3,000 foundation shades and it will recommend a foundation that is most similar. The recommender is using cosine similarity of the hex values of the skin compared to the dataset of foundations. 




### Data Sources
* [`allShades.csv`](./Data/allShades.csv):  | Description of the [data](https://github.com/the-pudding/data/tree/master/makeup-shades)
* [`allshades_updated.csv`](./Data/allshades_updated.csv): An Updated Version of the dataset with the converted HEX values to RGB 





### **Data Dictionary**

|Feature|Type|Dataset|Description|
|---|---|---|---|
|brand|object|allShades|The Name of The Brand| 


### Technology Requirements 
This includes the following:
- python 3.6 or later
- pandas
- numpy
- mediapipe 
- open cv 
- colorsys
- Scikit learn 


### Conclusions and Recommendations
