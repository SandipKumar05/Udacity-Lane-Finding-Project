# Udacity-Lane-Finding-Project

Pipeline that finds lane lines on the road

1. I convert the image in grayscale.
2. Apply Gaussian, make the image smooth
3. Apply canny, make edge in image
4. Apply mask in image, obtain only area that have lane lines
5. Huage_line find lines in image. using draw line, I draw the lines (lane lines) on a blank image
6. Weighted_image merge the line image(blank image with lines) with color image

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

1. I take all the lines and divided in two part based on the slope of line (Right line and left line).
We can easily see in the image that left line (positive slope) and right line (negative slope)
2. I take average of all the lines
3. I find the top point and bottom point of lines.
4. I get two point, using cv2.line I draw the line in blank image
