# Problem Statement

## Problem
Location is a valuable piece of information that brings peace of mind. In an ideal world, we would always know the location of our precious belongings.
Losing an object of value as an abstract problem applies to many scenarios. For example, keys and wallets should always be where you last left them, but they seem to have a mind of their own! People living with dementia or cognitive deficits may need a little more help keeping track of their belongings. Pets, livestock, or endangered animals may need to be tracked to ensure their safety and wellbeing.

The core problem we want to define for our project is user-friendly object tracking for objects in close proximity.

## Current Solutions
Current solutions to the problem of object tracking are not effective for the problem of tracking objects in close proximity and representing their location in 3D space in a useful manner. 

Map-oriented solutions, like FindMyPhone for mobile devices and the Tile tracker, display the current location of the tracked object on a map. This approach is not useful if you already know the geographic location of your object (say, your phone gets lost in your house), but you don’t remember where you left it last and you can’t find it in a cluttered environment.

Sound-oriented solutions, like the Samsung Galaxy Pods’ and the Apple AirPods’, will have the tracked object play a sound to help find its location. This approach is limited in its effectiveness, among other factors, by the environmental noise level, the user’s hearing, and the user’s mobility.

## Our Solution
Our approach to the problem of close proximity, user-friendly object tracking is to develop a mobile application that can display the location of select objects of interest in augmented reality. This approach takes away the guesswork from finding your belongings, as it will display the direct location of the object.

To give a brief description of this experience, you attach a tracker to a belonging you want to track, like your keys. You open up the SolvAR application and try it out. Your camera opens and your phone displays your room, without your keys in shot. You turn your phone to have your keys in frame, and over your keys you see a 3D model of a question mark, because your tracked keys aren’t registered in the app. You register your keys in the app, select a key 3D model and assign its name as “car keys”. After registering and later losing your keys, you open SolvAR, walk around your house, and find them in your cluttered desk, as pictured above.

## Actual Plan
The main components of this project are the SolvAR app, which consists of the program, the user interface, and AR, 3D models, and the object-tracker pair.

The following describes the data flow for our project. First, we will simulate the object and the tracker pair with a position interface that serves dummy position data that is relevant to Unity and an ID unique to each object-tracker pair. This position interface will feed this data to Unity Out-of-Process, then to Unity in C# code. 

Our app and the user interface will be built in Unity 3D, which allows us to easily export our project as an Android app. The object’s location will be tracked and displayed as a 3D model in augmented reality using ARFoundation, which is an extension of ARCore. 

We will prepare 3D models using Blender3D, a free and open source 3D modeling software, to build representations of groups or types of objects and render them in Unity3D’s AR scene using vertex shaders.

These models have a spatial mapping wireframe/vertex shader that draws edges onto the model so it will be easier to detect in AR. These wireframes will scale with distance in relation to the phone (distance is a constant variable per object), and will continuously appear whether or not it is behind an object. Some examples of models we will create are keys and small electronics.

Since trackers are expensive and difficult to prototype with we are going to only emulate the local positioning data in order to show a proof of concept. The primary objective of this program is to deliver the local position of an object being tracked in a way that’s useful to a user.

The position emulator will emit the position and Unique ID of multiple objects being tracked. The details of what each object is is specified by the user on the app and stored as an ID + details pair in a database or config file.

The details the user can add include the name of the object, a 3D model, color code, and ownership. Then whenever the application receives the location of that ID from the emulator it will display the corresponding details in the AR scene. If a user hasn’t registered the ID yet it will display a question mark to indicate that there is an object being tracked that hasn’t been registered yet. The user can then choose to register the new id.
