# User Stories

## 1 Download Application on Android

As a parent, I tend to lose my keys and other smaller objects a lot. I would like to find an application that could locate and receive visual feedback about these objects.

#### Elaboration

Users should have the ability to use a small bluetooth device in tandem with an Android device to find small objects, by displaying a visual representation of the object in a 3D environment. 

#### Constraints

Must be able to download/install onto an Android device.

#### Effort Estimation

Less than an hour

#### Acceptance Test

Download the APK from an external source onto an Android device, install the application and run the application on the phone.

## 2 Select Type of Objects

As a visual person, I would like an application that would give visual feedback in regards to what type of object I am looking for.


#### Elaboration

Users should have the ability to select an image on the screen of what type of object they wish to track so that the object will display with the location data.

#### Constraints

none

#### Effort Estimation

4 person-hours

#### Acceptance Test

Use the user interface to select an image, and use pre-allocated location data to test the visual feedback.


## 3 Visualize Location Data

As a forgetful person, I often lose small items such as my keys and would like a way to visualize where they are in a room to find them easier.


#### Elaboration

In the augmented reality scene process location data to be able to display where the object is within the scene and help guide the user to the object.


#### Constraints

Distance to the user, if the object is too far from the user it may be impossible to receive data from the transmitter.


#### Effort Estimation

4-5 hours

#### Acceptance Test

Provide pre-determined location data to the application to see if it displays the object in the correct location in the scene.

## 4 Save Location Data

As someone who works with inventory and tracking valuable assets I would like to be able to store logs of object locations for liability reasons.

#### Elaboration

Save a simple log file of location data that’s been transmitted to the app. 


#### Constraints

The data is limited to the precision and consistency of the tracking we use.


#### Effort Estimation

2 person-hours

#### Acceptance Test

Save the location history of more than 1 object and test that the saved log is accurate.

## 5 See Metadata of Each Object

As a user trying to find an object I would like to be able to see the details of the object such as its name.


#### Elaboration

Tapping on an object’s 3D gizmo on screen displays details about the object that the user registered. 

#### Constraints

If the object is not in view you can’t tap on it. 

#### Effort Estimation

2 person-hours

#### Acceptance Test

Register an object in the app then tap on it while it’s in the AR scene.


## 6 Receive Notifications about Object Proximity

As a person who recently had their house broken into I’m paranoid about having my valuables stolen and would like an application which can notify me when that might be happening.


#### Elaboration

Track the acceleration of the object and when it reaches a certain threshold it will notify the user that the item might be stolen or missing.


#### Constraints

If the user is too far from the object to track it then notification is not possible.

#### Effort Estimation

3-5 person hours

#### Acceptance Test

Run away with a transmitter object and see if the application notifies the user.
