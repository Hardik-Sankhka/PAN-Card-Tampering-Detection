# PAN-Card-Tampering-Detection
The purpose of this project is to detect tampering of PAN card using computer vision. This project will help different organization in detecting whether the Id i.e. the PAN card provided to them by thier employees or customers or anyone is original or not.
For this project we will calculate structural similarity of original PAN card and the PAN card uploaded by user.
STEPS ARE --
1. Loading original and user provided images.
2. Converting the format of tampered image similar to original image.
3. Then, we checked the format and size of the original and tampered image.
4. Converting the size of tampered and original image.
5. Orginial PAN card image used for comparision.
6. User provided image which will be compared with PAN card.
7. Reading images using opencv.
8. Converting images into grayscale using opencv. Because in image processing many applications doesn't help us in identifying the important, edges of the coloured images also coloured images are bit complex to understand by machine beacuse they have 3 channel while grayscale has only 1 channel.
9. Structural similarity index helps us to determine exactly where in terms of x,y coordinates location, the image differences are. Here, we are trying to find similarities between the original and tampered image. The lower the SSIM score lower is the similarity.
10. Find contours works on binary image and retrive the contours. This contours are a useful tool for shape analysis and recoginition. Grab contours grabs the appropriate value of the contours.
11. Bounding rectangle helps in finding the ratio of width to height of bounding rectangle of the object. We compute the bounding box of the contour and then draw the bounding box on both input images to represent where the two images are different or not.

Summary --
Finding out structural similarity of the images helped us in finding the difference or similarity in the shape of the images. Similarly, finding out the threshold and contours based on those threshold for the images converted into grayscale binary also helped us in shape analysis and recognition.
As, our SSIM is ~31.2% we can say that the image user provided is fake or tampered.
Finally we visualized the differences and similarities between the images using by displaying the images with contours, difference and threshold.

Scope --
This project can be used in different organizations where customers or users need to provide any kind of id in order to get themselves verified. The organization can use this project to find out whether the ID is original or fake. Similarly this can be used for any type of ID like adhar, voter id, etc.
