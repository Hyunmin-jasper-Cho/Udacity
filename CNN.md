## Normalizing image inputs
Data normalization is an important pre-processing step.  
It ensures that each input (each pixel value, in this case) comes from a standard distribution.  
That is, the range of pixel values in one input image are the same as the range in another image.  
This standardization makes our model train and reach a minimum error, faster!  

Data normalization is typically done by subtracting the mean 
(the average of all pixel values) from each pixel, and then dividing the result by the standard deviation of all the pixel values. 
Sometimes you'll see an approximation here, where we use a mean and standard deviation of 0.5 to center the pixel values.
Read more about the Normalize transformation in PyTorch.

The distribution of such data should resemble a Gaussian function centered at zero. 
For image inputs we need the pixel numbers to be positive, so we often choose to scale the data in a normalized range [0,1].
