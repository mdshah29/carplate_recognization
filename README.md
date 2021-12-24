# carplate_recognization
Read car Plate and its annotations , Based on that recognize number of car plate


Approach:
- car_cnn contains 433 car images with number plates  
- annotations folder contains number plate box place and dimention

- Access cars images from google drive 
 
- As a start I have taken 1 image and applied few pre-processing steps like resizing, thresholding, blurring and tried to find contour using findcontour 
- but in problem they have already provided annotations xml for all images which i have used for finding rectangle box of number plate.

- splitted data in train and test and fit the data using model VGG16 using cnn.

- found score oof 72% using this approach and accuracy of .85 using batchsize and epochs as 20, almost took 1 hour to train this model 

- Based on this fitted model applied this model on some test data and checked accuracy , its near by but not exact ..

- once we got rectangle box from above model used easyocr to read number from rectangle box.

-- Help for VGG model 
https://machinelearningmastery.com/use-pre-trained-vgg-model-classify-objects-photographs/


Detected number is MH 20EE 7598

To Improve Results: 

- Can train model with 50 epochs and batches on same VGG16 
- Trying to apply VGG19 



