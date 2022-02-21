Brief Explanation on how to assemble and run the project
--------------------------------------------------------
The project is tested and is run on Google Colab.
Firstly we should upload all the files given in this folder in the Google drive.
The code files are there in the folder named "Colab Notebooks".
In Colab Notebooks there will be 5 files and brief explanation and working is given below:

IP Project - This is the initial file where all the codes are kept in one file. That is CNN, ORB Detector, SIFT detector are kept under one file. This is presented for Review-2.In Review-3 we modularised the code and made a code for evaluating the accuracy.

User Classification - It contains the code for CNN which is trained and then the trained model is saved in a file called identify_sign.h5.

identify_sign.h5 - Here the trained model of CNN is saved and is used in various files like Forgery detection - eval, Forgery_detection.

Forgery_detection - This file contains the ORB, SIFT detectors and is imports the CNN model, we give a query image and then the CNN classifies the user then the genuine images of the users are compared with query image using ORB and SIFT detector and then the query image is classified into Genuine or Fraudulent Images.

Forgery detection - eval - This file automates the process of Forgery_detection and helps us to calculate the Accuracy of CNN, ORB detector and SIFT detector.

There are 2 dataset folders namely Signature_classify, Signatures_detect.
Signature_classify: Contains the training and testing data for the users. All the images here are genuine images.
Signatures_detect: Contains images apart from training and testing and it contains 5 genuine images and 5 fraudelent images.

The Format of the Image name: 0XX0N00U
Where, 
XX - signed by user
N - Sample Number
U - Signature of (Owner of the signature)
-----
NOTE:
-----
In case of error in SIFT detector, this happens as SIFT detector is available only in older versions.
Hence to access SIFT please Use the below code:
!pip3 uninstall opencv-python
!pip3 install -U opencv-contrib-python==3.4.15.55

----------------------------THANK YOU----------------------------