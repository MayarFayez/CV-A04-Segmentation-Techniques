# CV-A04: Segmentation-Techniques

## Description:
A small web application based app developed with python and streamlit, to apply 
different image processing techniques.  

## Requirements:
• Python 3.  
• Streamlit 1.13.0  
• Numpy 1.23.4  
• Matplotlib 3.6.2  

## Running command:
Streamlit run server.py      
-The UI contains two main tabs Thresholding, Segmentation  
# Tab1:
• Optimal Thresholding  
• Otsu Thresholding  
• Spectral Thresholding  
• Local Thresholding  

### Optimal thresholding:
Minimize number of misclassified pixels if we have some prior 
knowledge about distribution of the gray levels values that make 
up the object and the background.
Is the one who divide histogram into two parts given that 
distribution of values at the same segment has minimum variance.  
![Screenshot (1476)](https://github.com/MayarFayez/CV_-Segmentation-Techniques-/assets/93496610/b8c38f77-4191-4ef1-a398-833c9a6aeb97)  
#### Basic steps for Optimal thresholding:
1. First approximation that the four corners of the image contain background pixels 
only and the reminder contains object pixels.  
2. At every step “t” compute mean of background and object gray level.  
3. Determine threshold value “T” at every step as the mid-point between the two 
means.  
4. Update the value of threshold until T(t+1) =T(t)
#### Results:
![Screenshot (1477)](https://github.com/MayarFayez/CV_-Segmentation-Techniques-/assets/93496610/c4fe0235-f851-4eba-95c0-405dba8d4d3a)  
### Otsu thresholding:
The algorithm iteratively searches for the threshold that minimizes the withinclass variance, defined as a weighted sum of variances of the two classes 
(background and foreground). The colors in grayscale are usually between 0-255 
(0-1 in case of float). So, if we choose a threshold of 100, then all the pixels with 
values less than 100 becomes the background and all pixels with values greater 
than or equal to 100 becomes the foreground of the image.  
The formula for finding the within-class variance at any threshold t is given by:  
𝝈2(𝒕) = 𝝎𝒃𝒈(𝒕)𝝈2𝒃𝒈(𝒕) + 𝝎𝒇𝒈(𝒕)𝝈2𝒇𝒈(𝒕) (1)  
![Screenshot (1478)](https://github.com/MayarFayez/CV_-Segmentation-Techniques-/assets/93496610/e51e13b1-03ae-4234-84cb-4dd7fe28bc39)  



