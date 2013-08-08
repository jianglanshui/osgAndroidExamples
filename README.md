osgAndroidExamples
==================

List of examples combining OpenSceneGraph and Android. 

Architecture of the samples are based on the original code from osgAndroidExampleGLES2 developed by Jorge Izquierdo Ciges (distributed with OSG). You will find each feature demonstrated in osgAndroidExampleGLES2 in separated examples as well as new examples (location, sensor, camera, etc.).


Tested with: OpenSceneGraph-3-2.0 + Nexus 10.

The source code come as Android 2.3.1 (API 9) project.

Basic
-----
OsgGLView: create an activity, instantiate a default GL View and GL Renderer, call init, update, resize native functions.You get a default renderer.

OsgGLView2: same as before but use a layout configuration (main_activity.xml) to associate the View to the main activity.

OsgDisplayGeometry: display a basic sphere with a really simple shader.

OsgDisplayGeometry: display a basic text with a really simple shader.

Basic Viewer
------------
OsgUITouch:

OsgUIKeyboard

OsgViewer

Android Resources
-----------------
OsgLocation: display location values as osgText::Text.

OsgSensor: display sensor values as osgText::text.

OsgCamera:

OsgBitmap:

OsgVideoMedia:


Basic GUI
---------


-------------------------------------
Raphael Grasset
http://www.raphaelgrasset.net
