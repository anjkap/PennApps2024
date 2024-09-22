# MyDraw

## Inspiration

We were inspired by architecture prints. One of our team members' cousins spends a lot of time printing architecture blueprints. We aimed to create a similar automated drawing/printing web application that would speed up the process. This inspiration eventually evolved into MyDraw.

## What it does

MyDraw is an app that creates customized, meaningful coloring book pages. Users start by uploading a picture, which they can edit with deep generative models. We integrate a deep learning algorithm for edge detection called Holistically-Nested Edge Detection (Tu and Xie) which optimizes edge detection by taking semantics into account. This algorithm creates the coloring page itself, which can be printed to our CNC pen plotter machine for kids to color on.
Link to pretrained model (too big to upload to GitHub): https://vcl.ucsd.edu/hed/hed_pretrained_bsds.caffemodel

After the coloring page is generated, we provide insights on ways to color the page creatively. One option is to pick coloring styles for the image. Users can pick between several art styles, like watercolor, 
geometric, and pop art. A coloring guide will be generated, with an example finished coloring page in the style the user selected (or they can upload a custom style) and a color palette. The finished coloring page is generated with a style transfer model from Tensorflow Hub.

## How we built it

Our hardware component is a CNC pen plotter machine that uses a rack and pinion mechanism for linear motion along the X and Y axis and a motor rotating the pen holder for the Z axis movemet. Our software is a Flask application that generates the edited images and the images created to pass to the CNC machine.

## Challenges we ran into

We had a lot of issues getting our motors to work, because the quality of our motors and drivers were not the best and we had to be careful not to burn them out. We had problems troubleshooting with the electronics because we didn't know exactly which part was not working, as there were quite a few unreliable parts.

## Accomplishments that we're proud of

We're proud of pushing through even when things seemed hopeless when our electronics were not working at all. This determination allowed us to create a finished final product.

## What we learned

We learned that hardware projects have many points of failure, so it's best to research how each component connects beforehand. We should also test out the software and try to connect it to the electronics beforehand.

## What's next for MyDraw

We want the CNC machine to gain functionality to draw images with generated GCode. This was one of our intended functionalities, but we were unable to implement it due to incompatibility of our parts with the software.
