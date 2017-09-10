
# **Finding Lane Lines on the Road** 

## Writeup 


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

I created a function named pipeline that holds all necessary parameters and call the helper- functions in the right order. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function.
First with an if structure that filters the points of the left and the right line via the computed slope of the lines.
Then it add the points into seperate lists.
After that i read the min and max Values and map them to the cv2.line function whitch add the lines to the target Image.


![alt text][/examples/gray.png]
![alt text][/examples/blur.png]
![alt text][/examples/canny.png]
![alt text][/examples/complete.png]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there are no Lines with the requested slope found. The routine will crash.

Another shortcoming is when there is no solid Line it will Connect the max and min Values well but then there is no solid Line Drawn to the bottom of the Image.   


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to scale the drawed lines up to the bottom and/or to a defined limit(the top border of the masked area for example.

When driving into a Curve the Lines will not drawn correctly because only the outer Points will be evaluated.



```python

```
