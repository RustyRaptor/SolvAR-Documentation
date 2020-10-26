# Requirements Specification for SolvAR
## 1. Introduction
### 1.1 Purpose of Product
*A one-paragraph description of your product's purpose.*

The purpose of SolvAR is to provide a mobile application that can display the location of select objects of interest in augmented reality. SolvAR takes away the guesswork from finding lost belongings that are in close proximity, as it displays the direct location of the object.

### 1.2 Scope of Product
*A short description of your product's scope (what it includes and what it does not include). Part of your problem statement might be useful here, but focus on the scope of the product.*

Our project will be an Android application that is build in Unity 3D that will display the emulated location of select objects in augmented reality. The scope of this project covers the emulation of location from a bluetooth tracker, as well as building the scene, prefabs, and scripts in Unity to design the augmented reality experience and user interface.
This project does not include the actual integration of a bluetooth tracker to the app.

### 1.3 Acronyms, Abbreviations, Definitions
*Any important terms that are required to understand your project documents.*

AR - augmented reality

### 1.4 References
*Any external references needed to understand your project documents. Use URL links if possible.*

AR Foundation 2.2 Documentation - https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@2.2/manual/index.html

## 2. General Description of Product
*This section contains a longer but not exhaustive description of your product.*

### 2.1 Context of Product
*Context or environment that your product will be in.*

Our product will be an Android mobile app for AR Core-compatible phones used in the context where users have lost an object.

### 2.2 Domain Model with Description
*Display and describe your domain model.*

We emulate objects and generate location data in a dummy data generator that passes this formatted location data to the dummy data broadcaster using Python 2.7. THis is sent to Unity Out of Process, which is processed in C sharp and passed to AR Foundation, which renders it in the AR scene. The app also has a registration wizard and object filters that are connected to a database that track unique objects and the user’s preferences for those objects.

### 2.3 Product Functions (general)
The application will be used to track a bluetooth transmitter which is attached to an object of the user’s choice, ie. keys, phone, wallet, etc. The positioning of the object will then be rendered inside of the augmented reality environment projected by the users' phones.

### 2.4 User Characteristics and Expectations
Describe your users and their abilities.
Our users are mobile phone users that are able to navigate simple menus.

### 2.5 Constraints
Phones must be compatible with AR Core and have Android 11 or greater.

### 2.6 Assumptions and Dependencies
*Does your system depend on external software packages? System assumptions? If so, describe them.*

Our system depends on Unity’s ARFoundation, AR Core, Android 11 or later. 

## 3. Functional Requirements
In a standard requirements document, you would have a LONG list of functional requirements here. You should put a link to your user story page here.
https://github.com/RustyRaptor/SolvAR-Documentation/blob/gh-pages/userstories.md

## 4. System and Non-functional Requirements
### 4.1 External Interface Requirements (User,Hardware,Software,Communications)
*Describe what kinds of interfaces your product has, and what they do. Then list specific requirements using item numbers as NF.4.1.X.*

The product has a user interface that manages the user’s current experience and the user’s preferences for objects. The product must also manage emulated locations in Unity with AR Foundation.
NF.4.1.1 User interface must include option to register new devices.
NF.4.1.2 User interface must include button to reset scene.
NF.4.1.3 Devices must display user chosen 3D model over the emulated location.
NF.4.1.4 Models must display title given to each unique device by the user.
NF.4.1.5 SolvAR must interface with user’s phone
NF.4.1.6 SolvAR must interface with emulated device’s location
NF.4.1.7 SolvAR must interface with AR Foundation
NF.4.1.8 SolvAR must interface with AR Core
NF.4.1.9 SolvAR must interface with Python 2.7

### 4.2 Performance Requirements
*Describe your product's performance needs. Then list specific requirements using item numbers as NF.4.2.X.*

To have satisfactory performance, SolvAR needs to display objects in AR space within a reasonable margin of error and to update the location of the objects with a reasonable frequency. SolvAR supports one user at a time.
NF.4.2.1. SolvAR will display the location of emulated objects with a margin of error of no more than 1 meter.
NF.4.2.2. Update frequency of emulated location every 1.5 seconds.

### 4.3 Design Constraints
*Describe external requirements that will constrain your design choices. Then list specific requirements using item numbers as NF.4.3.X.*

External requirements that constrain our design choices include lack of access to compatible Android devices and limited version control in Unity.
NF.4.3.1. Not all of our team members have access to an Android device, so access to testing equipment is limited.
NF.4.3.2. Version control in Unity is limited. We have to export the project as a whole binary file, so version control has to be on entire versions of the Unity project.

### 4.4 Quality Requirements
*What quality expectations do your users have? Is your system life-critical? Describe such issues, then list specific requirements using item numbers as NF.4.4.X.*

Our system is not life critical. Quality expectations from our users are that SolvAR is user friendly, that it can show the position information and object information in a useful way and understandable, and accurate and timely position info. This product will require minimal training.

### 4.5 Other Requirements
Anything else you need to say. Use item numbers NF.4.5.X.

## 5. Appendices
Include external documents that describe domain or constraints or any necessary information. Use URL links if possible.
