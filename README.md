# document-scanner-open-cv
It is an intelligent document scanner which made with the help of opencv.
Change path as per your input image file (line-53).
Run the document_scanner_opencv.py file.

 load the image and compute the ratio of the old height
 to the new height, clone it, and resize it



 convert the image to grayscale, blur it, and find edges
 in the image



 find the contours in the edged image, keeping only the




 loop over the contours



 if our approximated contour has four points, then we
 can assume that we have found our screen


 show the contour (outline) of the piece of paper



 apply the four point transform to obtain a top-down

warped = four_point_transform(orig, screenCnt.reshape(4, 2) * ratio)

four_point_transform method is written in document_scanner_opencv.py file 



 convert the warped image to grayscale, then threshold it
 to give it that 'black and white' paper effect



show the original and scanned images

