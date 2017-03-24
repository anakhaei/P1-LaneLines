#**Finding Lane Lines on the Road** 

##Writeup Template

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

My pipeline consisted of 5 steps:
- Convert image to grayscale
- GaussianBlur to reduce the noise
- Apply Canny filter
- Masking
- HoughLinesP filter by using the parameters recommended in the course

 
It resulted in a nice line detector.

To stitch the lines together, I used a very simple algorithm which is not certainly a generi approach. To save time, I simply extrapolates the left and right lines by the average slope of the right and left lines.


###2. Identify potential shortcomings with your current pipeline


- The masking will not work if we have curves
- The extrapolation will not work for the curves


###3. Suggest possible improvements to your pipeline

A possible improvement stitching the lines instead of drawing one line with the average slope.
