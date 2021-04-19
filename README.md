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

This application utilizes various technologies listed below. It begins by connecting to the individuals computer webcam and then snapping a picture of the individuals face. If webcam is not assesible , an individual can upload an image in the form of .jpg or png.  It then recognizes which regions in the picture are indicative of skin color and extracts the pixel-based color and finds the dominant colors. It does this through unsupervised learning including K-Means Clustering Algorithm. After extracting the colors in the form of RGB, the values are then compared to a dataset with over 3,000 foundation shades and it will recommend a foundation that is most similar. The recommender is using cosine similarity of the hex values of the skin compared to the dataset of foundations. 




### Data Sources
* [`allShades.csv`](./Data/allShades.csv):  | Description of the [data](https://github.com/the-pudding/data/tree/master/makeup-shades)
* [`allshades_updated.csv`](./Data/allshades_updated.csv): An Updated Version of the dataset with the converted HEX values to RGB 




### **Data Dictionary**

|Feature|Type|Dataset|Description|
|---|---|---|---|
|Foundation|object|allShades_updated|The Name of The Brand and the Product and The Product Number| 
|URL|object|allShades_updated|The URL to the Product online| 
|Shade|object|allShades_updated|The Name of Product Shade| 
|HEX|object|allShades_updated|The Tuple of the converted HEX values| 
|Hue|float|allShades_updated|The Hue Value of the shade| 
|lightness|float|allShades_updated|The Lightness Value of the shade| 
|red|int|allShades_updated|The red value of the RGB from the converted HEX Code| 
|green|int|allShades_updated|The green value of the RGB from the converted HEX Code| 
|blue|int|allShades_updated|The blue value of the RGB from the converted HEX Code| 



### Technology Requirements 
This includes the following:
- python 3.6 or later
- pandas
- numpy
- open cv 
- colors
- Scikit learn 
- Counter
- imutils
- pprint
- matplotlib
- pickle
- joblib



### Conclusions and Recommendations
In conlcusion our algorithm is able to extract the image and determine the skin color, and make a recommendation based on cosine similarities. The next steps include building out the application in Flask. Also would increase the sample size of images on the algorithm. 
