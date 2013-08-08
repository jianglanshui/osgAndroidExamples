osgAndroidExamples
==================

List of examples combining OpenSceneGraph and Android. 

Architecture of the samples are based on the original code from osgAndroidExampleGLES2 developed by Jorge Izquierdo Ciges (distributed with OSG). You will find each feature demonstrated in osgAndroidExampleGLES2 in separated examples as well as additionanl examples (location, sensor, camera, etc.).


Tested with: OpenSceneGraph-3-2.0 + NDKr9 + Nexus 10.

The source code come as Android 2.3.1 (API 9) project, ABI platform 9, armeabiv7-a, neon on (modify Android.mk, Application.mk
and Eclipse project configuration for any changes).

Basic
-----
OpenGL ES 2.0 Rendering with OSG.


OsgGLView: create an activity, instantiate a default GL View and GL Renderer, call init, update, resize native functions.You get a default OSG renderer.

OsgGLView2: same as before but use a layout configuration (main_activity.xml) to associate the View to the main activity.

OsgDisplayGeometry: display a basic (drawable) sphere with a really simple shader.

OsgDisplayGeometry2 (coming soon)

OsgDisplayText: display a basic text with a really simple shader.

OsgGLViewNative (coming soon)

OsgGLViewES3 (coming soon)


Basic Viewer
------------
Rendering with standard OSG viewer (support touch, keyboard input, camera manipulators).


OsgUITouch: display touch values as osgText::Text ("mouse" input). See OSGGLView and updateTouch method.

OsgUITouch2 (coming soon)

OsgUIKeyboard:display keyboard values as osgText::Text. See OSGGLView. See OSGGLView and updateTouch method.

OsgViewer: use touch + keyboard information for the viewer.


Android Resources
-----------------
Access Android resources (sensors, resources management) from a native OSG application. 

OsgLocation: display location values as osgText::Text. see updateLocation method.

OsgSensor: display sensor values as osgText::text. show the orientation sensor. see updateOrientationSensor method.

OsgCamera: display camera image on an osg::Texture. see updateCamera method.

OsgBitmap: display bitmap from resources on an osg::Texture. see updateBitmap method.

OsgVideoMedia (coming soon)


Basic GUI
---------

OsgUIMenu:

OsgUIToast:


-------------------------------------
Raphael Grasset
http://www.raphaelgrasset.net
