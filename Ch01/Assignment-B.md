**Q**. What are Channels and Kernels (according to VisionAI course)?
<br>**A**. Channels: Channels are the discrete set of information that are combined to create the color information for that pixel. 
There can be different types of channels that can be used. Example of channesl are RGB, RGBA, CMYK, etc. IF we take the RGB as the
indicator for defining the colors present in the image then each pixel value can be said to be a combination of a set of Red, Green and Blue values.
Hence, Red, Green and Blue can be referred to as channels

Kernels: Kernel is a matrix, that is used to extract a feature from the given image.

**Q**. Why should we (nearly) always use 3x3 kernels?
<br>**A**. Lets examine kerenls of diff sizes:
<br>**1x1 Kernel**: We would be trying to make sense from the smallest unit itself and it wouldn't give use any relevent information.
Like if we were to do an edge detection, we can never be able to make out with the single pixel itself.
<br>**2x2 Kernel or 4x4 Kernel**: The receptive field would be asymmetric for the pixel in process. Hence, missing on a lot of information.
<br>**5x5 Kernel**: Processed pixel will have a symmetric receptive field, hence the information would be better, However the number of pixels in the next layer would be less and hence fewer features would be extracted.
<br>**3x3 Kernel**: Processed pixel will have a symmetric receptive field and would have more pixels to work with in the next layer so more complex features can be extracted.
<br>Also: 3x3 kernel would be computationally less expensive that 5x5. ex for a 200x200 image:
5x5 uses 10* 3x3 computations on avg.

**Q**. How many times to we need to perform 3x3 convolutions operations to reach close to 1x1 from 199x199 (type each layer output like 199x199 > 197x197...)
<br>**A**. Each layer loses 2 pixels width and column wise. 199/2 = 99 convolutions

**Q**. What happens during the training of a DNN?
<br>**A**. During the training of the DNN the labelled data is used to tell the network what we are trying to make it learn. 
The nueral network runs on the sample data to make sense of it and based on this learning the neural network would be able to identify the similar patterns in the unlabelled data automatically, 
without any further supervision.
