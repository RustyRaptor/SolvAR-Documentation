# Design Document

---

## Project Architecture Recap

### Arch Diagram.

![Model View Controller](diagrams/SolvARarch.png)

### Explanatory Text.

Our project’s architecture is based on the Model-View-Controller style in which three key components interact: the Model, the central component that manages the data, logic, and rules of the application; the View, the visual representation; and the Controller, input from the user that converts it into commands for the model and a subsequent update to the view.

In our project, the model consists of the Unity 3D platform that integrates ARFoundation, ARCore, and the data structures of our project including scriptable objects, to form the data, logic, and rules for SolvAR.

The view is the visual representation of SolvAR and it consists of the live AR experience of a UI and 3D Blender models.

The controller is input from the user. It consists of live feedback from the user’s phone’s camera and movement sensors, as well as information given by the user for each object, such as a name, description, and chosen 3D model to represent the object in SolvAR.

---

## Description of class-level design of system.

Solvject :: Scriptable Object - contains data regarding representation of the IRL object (regarding position, rotation, given user data such as a name or description, and the mesh applied to the object).

CreateSolvject :: Singleton Monobehavior - instantiates list of Solvjects at runtime at specific locations in regards to the camera from given user input

SolvjectManager :: Singleton Monobehavior - calculate distances and update UI

---

## Discuss control issues: Are you using threading? Is there external communication that affects control?

There is no external communication, since all of the data is from user input. For threading, we will be utilizing the phone's notification system to notify the user whenever an object is a certain distance away from them.

---
