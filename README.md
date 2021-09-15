# Implemented MISLnet to detect camera model from which image was shot

The idea is to remove the _content_ of an image which leaves only the forensice traces. We train our model on these traces to find the camera model from which the input image is shot. 

The _content_ of the image is removed by using a custom CNN filter called Constrained Convolution Layer which is inspired from prediction error filters. Basically, we try to predict the value of a pixel using its surrounding pixels and find the difference between the pixel value and the predicted value. This difference is error and contain the forensic traces of the image. Our custom convolution layer does this. 



Reference Paper: https://misl.ece.drexel.edu/wp-content/uploads/2018/04/BayarStammTIFS01.pdf
