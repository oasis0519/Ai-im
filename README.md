# Gender-Detection

## Dataset
- Images and Meta Data : https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/static/wiki.tar.gz

- Cropped Images : https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/static/wiki_crop.tar

## Data Preprocessing
- Few of the Images were corrupted and hence had to be removed from the dataset.
- Face Detection Algorithm (Cascade Classifier) is used to check if an image is valid or not.
- If a face is detected in the Image, Collect the required details (Full path and Gender) of the Image.
- Store the required data in a different .csv file.

## Framework/Library used
- Keras with Theano backend.
- OpenCV2 for Image Processing Algorithms.
- Pandas and NumPy for .csv and mathematical computations.

### Keras
- Is a Deep Learning Library which supports Theano and TensorFlow at backend.
- Keras is easier to install compared to other frameworks and had a better Documentation.
- https://keras.io/

## Data Model
- VGG-16 data model is used for training and testing.
- Such a data model contains a 16 layer network.
- Weights of the VGG16 Model used from : https://drive.google.com/file/d/0Bz7KyqmuGsilT0J5dmRCM0ROVHc/view?usp=sharing

## Results and Outcome
- A live video captures an image if a face detected in the frame.
- The cropped image (face) is sent to the pipeline where the a prediction is made with already saved model which is loaded globally.
- An additional layer (Sigmoid) is added at the flatten layer of the model.
- The Prediction lies between 0-1.
- Values near to 0 signifies Female. Values near 1 signifies Male.
- A Cross Validation Accuracy of 90.92% is achieved on the Dataset trained.

## Team Members
- Mohit Reddy (mohitreddy1996)
- Ambareesh Prakash (AeroDeath)
- Vilas M Bhat (vilas897)
- Aneesh Aithal (aneesh297)
- Somnath Sarkar (somnathsarkar)


+++++++++++++++++++++++++++++++++++++++++++
It’s missing extraction from some cards important numbers.
This is an example.
{
    "Analysis":
    {
        "PreProcessTime":"0.000",
        "RecognitionTime":"9.010",
        "TypeID":"15",
        "RegionID":"12",
        "RegisterID ":"-1",
        "SubID":"61"
},
    "CardInfo":
    {
        "Type":"BIRTH",
        "Region":"AUS_WA",
        "Register_Number":"",
        "Child_Surname":"Marsh",
        "Child_Given_Names":"Trisha Anne",
        "Child_Date_Of_Birth":"26 July 1976",
        "Child_Place_Of_Birth":"Regional Hospital, Narrogin, Western Australie.assrziia",
        "Child_Sex":"Female",
        "Mother_Surname":"Marsh",
        "Mother_Given_Names":"Hazel Dawn",
        "Mother_Maiden_Surname":"Fraser",
        "Mother_Usual_Occupation":"",
        "Mother_Age_Or_Date_Of_Birth":"19 Years",
        "Mother_Place_Of_Birth":"",
        "Father_Surname":"Marsh",
        "Father_Given_Names":"Colin Patrick",
        "Father_Usual_Occupation":"Loader Driver",
        "Father_Age_Or_Date_Of_Birth":"28 Years",
        "Father_Place_Of_Birth":"Wyalkatchem, Western Austraiia, Australie",
        "Parents_Date_Of_Marriage":"3 March 1976",
        "Parents_Place_Of_Marriage":"Narrogin, Western Australia, Austraka",
        "Issue_Date":"11 Jan 2014"
    }
}

Registration number etc missing.
TAS Certificates dates say “Registered on 8th November 1985 by C.Blurns” should be 8th November 1985.
    ⁃    Make all date formats DD/MM/YYYY
Certificates
    ⁃    missing Registered Date and Registered Number
Medicare
    ⁃    Missing card color - in Engine 4
	
+++++++++++++++++++++++++++++++++++++++++++++++++++++++