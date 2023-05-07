Download Link: https://assignmentchef.com/product/solved-homework-assignment-3-cs696-applied-computer-vision
<br>
Overview

The goal is this problem is to practice the sliding window method for template matching.

<strong>Review of sliding window algorithm</strong>

<em>Figure 1. Template matching with sliding window. Left: cropped template image; Middle: scaled template image; right: query image.  </em>

Given a template image, e.g., left eye, our task is to find the most similar sub-region in the query image.

To do so, we will exploit all possible sub-regions of the query image, and calculate the similarities between these sub-regions and the template image.  The key is how to define the similarity metric.

In the class meeting, we introduced four different metrics.

<ul>

 <li>Correlation</li>

 <li>Zero-mean correlation</li>

 <li>Sum Square Difference (SSD)</li>

 <li>Normalized Cross Correlation (NCC)</li>

</ul>

Usually SSD and NCC  are better choices.

<strong>Image Data</strong>

We provide three images (data folder) as query images.  You are strongly encouraged to find sample images on your own.

Convert these query images into grayscale.  You can visualize your final results in the RGB images if you like.

Crop template images from the query images.   The size of the template image will be varying, e.g., 10 by 10 pixels, 20 by 20 pixels, 30 by 30 pixels.

Save the center position of each template image in the query image.  This will be used to evaluate your template matching algorithm.

Resize the template images with a few factors (e.g., 2, 1, 0.5), and match each of them to the query image.

<strong>Evaluation</strong>

Once you localized a template image, calculate the Euclidean distance between the estimated locations to the ground-truth location (saved when you cropped the template images),  i.e.  <em>localization error</em>.

<strong>Coding requirement</strong>

You will deal with two cases.

Case-1: template matching with fixed scale: match the cropped template to the query image

<ul>

 <li>Implement the sliding window method for matching a template image to a query image.</li>

 <li>Try to use three different  metrics Zero-mean correlation,  SSD and NCC</li>

 <li>Calculate the localization errors for each metric.</li>

</ul>

Case-2: template matching with pyramid representation:

<ul>

 <li>Resize the template images with multiple scaling factors (e.g., 0.5, 1.0, 2.0) to get the pyramid representation of the template image.</li>

 <li>Implement the sliding window method for matching each of the pyramid images (scaled image) to the query image.</li>

 <li>Use the metrics Zero-mean correlation,  SSD and NCC</li>

 <li>Calculate the localization errors for each metric.</li>

</ul>




<strong>Useful functions</strong>

<ul>

 <li>normxcorr2()</li>

</ul>

<strong>Forbidden functions</strong>

<ul>

 <li>none</li>

</ul>

<strong> </strong>

<strong>Write-up</strong>

In the report you will describe your algorithm and any decisions you made to write your algorithm a particular way. Then you will show and discuss the results of your algorithm.




In the case of this problem set , show the results of your localization results while using different metrics.  Calculate and compare the localization errors in each case.




For some cases (e.g. scaled, metrics), you might fail to localize the template images.  Please try to explain the reasons.




Also, discuss anything extra you did. Feel free to add any other information you feel is relevant<u>.</u>




How to submit

<ul>

 <li>Submit your source codes and writeup through SDSU Blackboard</li>

 <li>Two submissions are allowed.</li>

</ul>


