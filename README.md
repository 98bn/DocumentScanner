# DocumentScanner
My first openCV project - a personal document scanner !!

Before performing the actual work of extracting the document in the image, the image is first converted from BGR to Grayscale.

The document scanner performs image manipulation in 4 steps -

1 Finding the edges    
  -> OpenCV library is used for the canny edge detection in the image. You can find the documentation here (https://docs.opencv.org/trunk/da/d22/tutorial_py_canny.html)
   
2 Finding the contours of the paper

 -> Includes finding all the contours in the image and then minimizing it to the conclusion of selection only that contour with 4 points   If the approximated contour has four points, then we can assume that we have found our document. 

3 Applying perspective transform-to obtain top view of the image as a document.

  -> Four-point-transform was used to transform the document into top-down view which includes the point ordering which orders the four points in the image to assign their repective position as top-left, top-right , bottom-left and bottom-right and then transform this image with these points to a warped image. These functions are given in file tranform.py.
