# Vehicle Fitness Test
The goal of this project is to automate the various steps involved in vehicle fitness tests.  
  
## Technologies Used
We have used technologies such as:
* Object detection 
* Object Localisation
* Pixel per meter and Trianguar Distance Measurement
* OCR  
* Google Translate API
  
## Flask Webpage  
The Flask Webpage can be executed by running the app.ipynb notebook  
The WebPage contains:  
* Login for Normal User and RTO Officer  
* Documents Upload for OCR - RC Book and PUC Certificate  
* Vehicle Registration Plate detection using OCR    
* Tyre Condition estimation - Normal, Worn Out, Cracked etc..  
* Headlights On/Off Detection
* Indicator Blinking Detection    
* Geo-Location  
  
## Car Parts Detection 
Download the weights from drive link and place it in _CarPartsDetectionChallenge-master\Data\Model_Weights_ folder  
Run the first block of code on Test_parts.ipynb for Car Parts detection. It performs MultiClass Object Localisation and detection using the YOLO Architecture to identify the following parts in the car:  
* Wheel  
* Head Lights  
* Door  
* Windshield  
* Rear View-Mirror  
* Glass - Front and Rear  

## Tyre defect Classification  
Run the "Tyre" block of code in the Test_parts.ipynb for executing the Tyre defect classification. It performs Multiclass Image Classificiation with the simple Convolutional Neural Network into 6 different categories:  
* Normal  
* Exposed  
* Tread Wear  
* Linear Air  
* Cracked Tyres  
* Bulges  

## Headlights ON/OFF Classification  
Run the "Headlights" block of code in the Test_parts.ipynb for executing the Headlights On/Off classification. It performs Binary Image Classification with a simple Convolutional Neural Network.  
## Horn detection
Run the horn_pitch_detection.ipynb in the horn_detect folder. The audio file should be in wav format and the path of it should be mentioned in the ipynb file.For testing, the 2 wav files in the horn_detect folder can be used.Here the algorithms AMDF(Average Magnitude Difference Function) and CAMDF(circular average magnitude difference function)are used.
  
## OCR for Vehicle Registartion Plate detection and Document Verification  
Refer to the OCR.ipynb for the OCR Tesseract code implementation. The details Extracted from the documents are:  
* Vehicle Plate Registration Number  
* Engine Number and Chassis Number
* Manufacturing Date of Vehicle and its Age
* Owner Information  

## Break test Automation
Refer to CarND-Vehicle-Detection-master folder to run the break tests for a given video. Distance w.r.t to camera and Speed of the Vehicle is be measured using Triangle Similarity and pixel per meter estimation. The braking distance is calculated based on the difference in the distance of the vehicle at 40kmph and at 0kmph.  

## Geolocation
Current location of the user is fetched from the geocoder library and compared with the location of the predefined location of the RTO. 
For location, latitude and longitude coordinates are used. 
The distance between them is calculated and returned in kilometers.
The distance calculation is done using the haversine library.


## Dataset used:
* Tyre condition testing: https://drive.google.com/drive/folders/1VxH_IP3-GHgj6tcykzbnZtpfHkALMv9p
* Indicator testing: The video has been uploaded in the repository
* Horn testing: The audio files are uploaded in the repository
* OCR: The test images are uploaded in the repository
* Headlights: The train and test images are uploaded in the repository
* License plate: The test images are uploaded in the repository
* Car parts detection: The train and test images are uploaded in the repository
