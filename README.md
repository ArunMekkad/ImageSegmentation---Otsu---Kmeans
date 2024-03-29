# Image Segmentation with Otsu's Thresholding and K-means Clustering

This repository contains a Python script that demonstrates image segmentation using two techniques: Otsu's thresholding and K-means clustering. The script uses libraries such as NumPy, Matplotlib, scikit-image, and scikit-learn.

## Program Overview

The script performs the following steps:

1. **Load the Image**: The script begins by loading an image using the `imread` function from the `skimage.io` module.

2. **Convert to Grayscale**: The image is then converted to grayscale using the `rgb2gray` function from the `skimage.color` module. This grayscale image is used for Otsu's thresholding.

3. **Otsu's Thresholding**: The `threshold_otsu` function from the `skimage.filters` module is used to perform Otsu's thresholding on the grayscale image. This method provides a clear distinction between the foreground and the background.

4. **K-means Clustering**: The image is reshaped into a 2D array and the `KMeans` function from the `sklearn.cluster` module is used to perform K-means clustering. This method captures more detail within the objects.

5. **Display the Images**: Finally, the script uses Matplotlib to display the original and segmented images.

## Testing and Comparison

Three types of images were used for testing: a real-life traffic scene, a distorted monochromatic photo of a person, and a well-lit, noise-free portrait. Each image was segmented using both Otsu's thresholding and K-means clustering, and the results were compared.


![Result1](https://github.com/ArunMekkad/ImageSegmentation---Otsu---Kmeans/blob/main/Result1.png)

![Result2](https://github.com/ArunMekkad/ImageSegmentation---Otsu---Kmeans/blob/main/Result2.png)

![Result3](https://github.com/ArunMekkad/ImageSegmentation---Otsu---Kmeans/blob/main/Result3.png)


**Otsu's Thresholding** is particularly effective when there is a clear bimodal distribution in the grayscale histogram of the image, which makes it suitable for images with high contrast and distinct objects. It performed well on the real-life traffic scene and the well-lit, noise-free portrait.

**K-means Clustering**, on the other hand, is more flexible and can adapt to a wider range of scenarios. It performed better on the distorted monochromatic photo, where it was able to capture more detail within the objects despite the distortion and monochromatic nature of the image.

## Conclusion

In conclusion, Otsu's thresholding is best suited for images with high contrast and distinct objects, while K-means clustering is more versatile and can handle a wider range of images, including those with distortion or noise. However, the choice between the two would ultimately depend on the specific requirements of your project. If you need to simply distinguish objects from the background, Otsu's might be sufficient. But if you need more detailed segmentation, K-means would be a better choice. However, the performance of both methods can vary depending on the nature of the image, such as its lighting conditions and the presence of noise.
