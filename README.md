# canal-transportation
image processing generate and compare start-end intersection by linear input

# version
v.1.2

# How to use
1. prepare your before & after images in same scale.
2. put it in folder source and name it "before{x}.jpg", "after{x}.jpg" where {x} is running number.
3. open app.exe
4. browse your image by click "next" and "back"
5. click any 2 points on image for start point and end point of line (in order)
6. click "confirm" to create line from selected points, or you may click "cancel" to decline points.
7. you may click more points on image to create multiple line.
8. you may click "reset" to remove every created lines.
9. click process to generate result from created lines, this process may take 3-5 seconds depend on image size and lines.
10. result will be saved in folder "result" and also shown on popup (you could close this popup).

# limitation
1. before and after images must be in same scale.
2. images name running number must be continuously.
3. app start with image number 0.
4. reprocess any image replace previously result.
5. result might be incorrect caused from invalid detection if image have low contrast.

# patch note

v.1.1
- fix bug  
- add grid on result image

v.1.2
- add 3 parameters input
1. edge detection threshold (default 300) (should be 1-500)  
decreasing this value for easier edge detection. (for the case result is not exists enough)  
increasing this value for harder edge detection. (for the case result is on wrong place (calculated on noise edge))  
3. minimum width filter (default 20) (should be 1-50)  
If edge's width is not reach this value, it will be removed.  
decreasing this value for less width-filter, thinner edge will be appear more.  
4. minimum length filter (default 40) (should be 1-100)  
If edge's length is not reach this value, it will be removed.  
decreasing this value for less length-filter, shorter edge will be appear more.  
