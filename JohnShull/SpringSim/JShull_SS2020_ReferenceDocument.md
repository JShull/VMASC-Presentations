# Spring Sim 2020 XR Tutorial Reference Document

This document is to accompany the presentation given by [John Shull](JShull@odu.edu). Please see the below content for a light summary of what was gone over including step by step setup instructions for Unity3d and MRTK.

A Back-up recorded session was captured and has been posted to [YouTube](https://youtu.be/CaLRp9AmjYg).

## Unity3D Setup

* Download [Unity3d](https://unity3d.com/get-unity/download)
  * Version used for the presentation was 2019.3.13f1
  * Unity will install other libraries associated with Visual Studio 2019 Community, Android Studio, and others.
* More information on [getting familiar with Unity](https://learn.unity.com/)
* Example Documentation [Unity3D gives out for Educators](https://connect-prd-cdn.unity.com/20190618/9ae41f5a-3249-401e-809e-a9ddf939dadf_Scope_and_Sequence.pdf)

## Microsoft Mixed Reality Toolkit Setup

* [MRTK is one of the most advanced extended reality toolkits](https://microsoft.github.io/MixedRealityToolkit-Unity/README.html) available that follows an open-source approach.
* It provides a set of components and features that drastically decrease development time and increase better experiences for users.
* It is completely customizable and all of the code is provides to you via Microsoft
* MRTK sits between Unity3D and your computer drivers. It is a bridge to allocate and gather data about the current XR system you have enabled on your computer.
* It acts like a bridge between your application and the various drivers supported by your selected runtime build environment.
* MRTK works with Android ARCore and on Android devices, Oculus Headsets, HoloLens headsets, Valve Headsets, HTC Headsets, and also works with iOS ARKit on Apple devices.
* MRTK provides a wide range of user centered components that allow for rapid prototyping and fully deployable software solutions within the Extended Reality Space.
* For Installation and setup see the information below
  * For the presentation I am using the prebuilt [Unity3d packages and Version 2.3.0 of MRTK](https://github.com/Microsoft/MixedRealityToolkit-Unity/releases)
    * Under the Assets table you will find 8 different downloadable packages we will be utilizing four of them
    * [MRTK Foundation]("https://github.com/microsoft/MixedRealityToolkit-Unity/releases/download/v2.3.0/Microsoft.MixedReality.Toolkit.Unity.Foundation.2.3.0.unitypackage")
    * [MRTK Tools]("https://github.com/microsoft/MixedRealityToolkit-Unity/releases/download/v2.3.0/Microsoft.MixedReality.Toolkit.Unity.Tools.2.3.0.unitypackage")
    * [MRTK Extensions]("https://github.com/microsoft/MixedRealityToolkit-Unity/releases/download/v2.3.0/Microsoft.MixedReality.Toolkit.Unity.Extensions.2.3.0.unitypackage")
    * [MRTK Examples]("https://github.com/microsoft/MixedRealityToolkit-Unity/releases/download/v2.3.0/Microsoft.MixedReality.Toolkit.Unity.Examples.2.3.0.unitypackage")
  * For [Microsoft specific documentation]("https://microsoft.github.io/MixedRealityToolkit-Unity/Documentation/GettingStartedWithTheMRTK.html")

### Unity & MRTK Setup Installation (10 Minutes)

* Create a new Unity Project - following the traditional 3D setup.
* Make sure you have already downloaded the Unity Packages from MRTK in the links above.
* With Unity Open, in the top toolbar go to Assets-->Import Package-->Custom Package
  * Find the MRTK Foundation Package first and install it, when prompted make sure to import all
  * After a few iterations a pop up window will launch asking you to *Apply Default Settings* hit _Apply_
  * You should now see a series of _MixedRealityToolkit_ folders in your Project tab.
  * Repeat this sequence for the other 3 MRTK packages: Tools, Extension, and Examples
* Import Text Mesh Pro Essentials, in the top toolbar go to Window-->TextMeshPro-->Import TMP Essential Resource
* Close and reopen the project after all assets have been imported

### MRTK Examples (10 Minutes)

* After reopening Unity navigate to the MixedRealityToolkit.Examples folder in the Project tab
  * Demos-->HandTracking-->Scenes-->HandInteractionExamples.unity
  * Notice the difference in examples on interaction
  * Two handed interaction vs. one handed interaction
  * Audio feedback and visual responsiveness

### MRTK Custom Profiles (10-15 Minutes)

* MRTK excels at their profile management system.
* Camera
* Input
  * Input Data Providers: where you hook in to the various input systems you need for your service
    * Windows Mixed Reality Device Manager, OpenVR Device Manager, Unity Joystick Manager, Unity Touch Device Manager, Windows Speech Input, Windows Dictation Input, Hand Joint Service, Input Simulation Service, Windows Mixed Reality Eye Gaze Provider, Input Recording Service, Input Playback Service
  * Pointers
    * Tied to the Controller type - hand/device
  * Input Actions
    * Core piece to customization and mapping of actions back to hand/device
  * Controllers
    * Define customization on 3D models and this is based upon the type of device that is activated
    * Here's where you would customize content around the user's input based on what the system sees as available.
  * Gestures
    * On the HoloLens 2 you can utilize hand gestures for interaction - this kit allows you to program them and sync them - just like you would with a button press on a controller
  * Speech
    * Simple command based approach in which you can automatically bring up content based upon user driven commands
  * Hand Tracking
* Boundary
* Teleport
* Spatial Awareness
* Diagnostics
* Scene System
* Extensions
* Editor

### MRTK Interaction Settings (10 Minutes)

* Navigate to the MixedRealityToolkit.Examples folder in the Project tab
  * Demos-->UX-->PressableButton-->Scenes-->PressableButtonExample.unity
* Look at the RoundButtons in the Scene
  * [PressableRoundButton Documentation](https://microsoft.github.io/MixedRealityToolkit-Unity/Documentation/README_Button.html)
  * Collider
  * Interactable
  * Pressable Button
  * Audio Source
  * Near Interaction Touchable

### Spatial Conceptual Model Using MRTK (10 Minutes)

* Internal project utilizing MRTK and the features I showed here
* Cut production time down significantly: had spent 4 months working towards something, recreated that in 1 week using MRTK.

#### Additional Information

* This project was built with some internal funding provided by VMASC and with a ton of guidance by [Dr. Beth Cardier.](http://info.bethcardier.com/index.php/models/)
