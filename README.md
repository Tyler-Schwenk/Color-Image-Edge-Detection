# Color Image Edge Detection

## Objective
To design a good edge detection method for color images, highlighting the edge of objects of a certain color, using MATLAB

## Solution
I found the desired object by its color which is given by the user. I then binarize the image, keeping the desired pixels as white(1) and others black(0). Next I fill in any holes in the white part of image, then take only the edges of the white parts, using Sobel’s method. Finally I take only the largest edge to filter out objects taken in error. Lastly I overlay the outline as blue over the original image. 

## Limitations/Growth Potential
Because I did this as an assignment for a computer vision class in college, I had limited time and needed to be satisfied with only completing what was required. With that being said, the code could be altered for other uses, for example:

- More universal detection of objects with a change of criteria
  - I currently accept 'r','o','y','g','b','i', and 'v' as input in order to search for an object of any color in the rainbow. I could instead take an RGB value to get a more specific color, which could be useful if this code were used as part of a more complicated image processing program.
  - Could be adapted to find multiple objects instead of just one.
- More robust search for object
  - If necessary, the detection of the object could be more strict by being fed more information. For example if given an estimate of the shape of the object, a Hough transform could be added to help verify selected canidates.

## Example Input and Output
![](/ColorEdgeDetectionOutput.jpg)
