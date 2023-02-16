# 3d-printing-image-processing

## Description of the file data_processing.m: 

This MATLAB code is used to process a set of image files and compute the proportion of yellow pixels 
in different regions of the image for each image in the set. The images are loaded using the imread function,
and then the proportion of yellow pixels is calculated for each of 13 bars in the image using a nested loop.

The code uses a for loop to iterate over a range of values of k,
which are used to construct the filenames of the image files.
For each value of k, the code constructs a filename string based on the value of k and loads the image using the imread function.
The image is then processed to compute the proportion of yellow pixels in each of 13 bars in the image.

The code uses a series of conditional statements to determine which bar each pixel in the image belongs to.
The proportion of yellow pixels is then calculated for each bar using the formula yellow(k/20-109,n)/(black(k/20-109,n)+yellow(k/20-109,n)),
where n is the index of the bar.

The resulting proportion of yellow pixels for each bar is stored in the proportion array,
and a plot of the proportion of yellow pixels in each bar is generated for each value of k.
The plot is saved to a file with a filename based on the value of k. Finally, the plot is closed and the loop moves on to the next value of k.


## Description of the file extension_combination.m

This MATLAB code is used to load data from several mat files and compute the average value of a set of proportions stored in the loaded data.
The code loads data from six mat files using the load function, and then computes the mean of the proportion values
for each file using the mean function. The resulting means are stored in six separate variables.

The code then uses a for loop to compute a weighted sum of the means for each bar in the image.
The resulting sum is stored in the proportion_signal_dynamic array, where each element corresponds to a different bar in the image.

The weights used in the computation of the sum are determined by the interval of values for each loaded mat file. 
For example, the mean proportion values for the proportion_0_100 mat file are multiplied by a weight of 50,
since the range of values for that file is 0 to 100.

## extension_data_processing decription: 

This code is used for image processing and analysis. It loads a set of image files,
and then for each file it extracts certain features from the image and calculates the proportion of certain colors
(black and yellow) in different parts of the image. The code then plots the proportion of black pixels in
each of the 13 regions of the image, and saves the resulting plot as an image file.

## 

