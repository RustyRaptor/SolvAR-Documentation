# Test Report

---
## Component Testing


For each simulation of an object in our project, we tested the data structure for our objects by assessing the code structure, then printing each object’s data members to the console, and asserting that they matched the given data.

Each simulated object is assigned a 3D model to be shown in the app.
To test if the 3D model assigned to an object was correct to each object, we had a script instantiate all the created objects in the Unity AR Scene and we checked that each instantiated model is correct to each object.

---
## System Testing


The crux of the test plan for our project was the compilation of the project into an apk and a successful run of the app in real time.

Compiling the project into an apk in Unity requires the successful integration of all project components, including assets and scripts, without errors. 

Additionally, running the SolvAR app in real time requires all of the simulated objects to successfully instantiate with the correct models, UI with the correct data, and location.

---
## Acceptance Testing


Once we are able to get a successful run of SolvAR on an Android device, we can compare the live experience of the app and its features to our user stories to determine if the acceptance criteria for each user story is met and if a feature is accepted by a user. 
 
#### Last updated: Dec 2, 2020.

User Story | Accepted?
---------- | ---------
Download Application on Android | accepted as completely implemented
Select Type of Objects | not accepted as completely implemented
Visualize Location Data | accepted as completely implemented
Save Location Data | accepted as completely implemented
See Metadata of Each Object | not accepted as completely implemented
Receive Notifications about Object Proximity | not accepted as completely implemented
