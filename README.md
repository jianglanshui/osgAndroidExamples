osgAndroidExamples
==================

A list of examples combining [OpenSceneGraph](http://www.openscenegraph.com) and Android. 

The architecture of the samples are based on the original code from [osgAndroidExampleGLES2](https://github.com/openscenegraph/osg/tree/master/examples/osgAndroidExampleGLES2) developed by Jorge Izquierdo Ciges (distributed with OSG, using embedded viewer). 
You will find each feature demonstrated in osgAndroidExampleGLES2 in separated examples as well as additionanl examples (location, sensor, camera, etc.).


Tested with: OpenSceneGraph-3-2.0 + Android NDKr9 + Nexus 10.

The source code come as Android 2.3.1 (API 9) project, ABI platform 9, armeabiv7-a, neon on (modify Android.mk, Application.mk
and Eclipse project configuration for any changes).

Basic
-----
OpenGL ES 2.0 Rendering with OSG.

The OsgDisplay examples correspond to traditional OSG examples find in a lot of common tutorials, if you know well OSG they are not really relevant for you (main difference here is related to ES 2.0 shaders).


**OsgGLView**: create an activity, instantiate a default GL View and GL Renderer, call init, update, resize native functions.You get a default OSG renderer.

**OsgGLView2**: same as before but use a layout configuration (main_activity.xml) to associate the View to the main activity.

**OsgDisplayGeometry**: basic osg geometry rendering. Display a triangle (geometry, vertex array) with a simple shader (no lighting, default vertex transfo, hardcoded color). 
Shader code use gl_ binding automatically converted by OSG (lazy mode) and default binding (osg_Vertex for binding vertex array).

**OsgDisplayGeometry2**: basic osg geometry rendering. same as OsgDisplayGeometry, without using automatic conversion: you need to use and declare osg_ bindings for attributes and matrix transformation)
and default binding (osg_Vertex for binding vertex array).

**OsgDisplayGeometry3**: basic osg geometry rendering. same as OsgDisplayGeometry2, without using automatic conversion and default binding: you need to do the binding yourself between
shader attributes and your arrays.

**OsgDisplayGeometryColor**: basic osg geometry rendering with color. Same as OsgDisplayGeometry, using a uniform for the color.

**OsgDisplayGeometryColor2**: basic osg geometry rendering with color. Same as OsgDisplayGeometry, using color array.

**OsgDisplayGeometryTexture**: same as OsgDisplayGeometry, using a built in texture.

**OsgDisplayGeometryLighting** (coming soon)

**OsgDisplayText**: display a basic text with a really simple shader.

**OsgDisplayTransfo**: basic osg transformation. Same as OsgDisplayGeometry, with a MatrixTransform applied to the triangle.

**OsgDisplayAnim**: basic osg animation. Same as OsgDisplayGeometry, with an update of triangle orientation in the main loop.

**OsgDisplayAnim2** (coming soon)

**OsgGLViewNative** (coming soon)

**OsgGLViewES3** (coming soon)


Basic Viewer
------------
Rendering with standard OSG viewer (support touch, keyboard input, camera manipulators).


**OsgUITouch**: display touch values as osgText::Text ("mouse" input). See OSGGLView and updateTouch method.

**OsgUITouch2** (coming soon)

**OsgUIKeyboard**:display keyboard values as osgText::Text. See OSGGLView. See OSGGLView and updateTouch method.

**OsgViewer**: use touch + keyboard information for the viewer.


Android Resources
-----------------
Access Android resources (sensors, resources management) from a native OSG application. 

**OsgLocation**: display location values as osgText::Text. see updateLocation method.

**OsgSensor**: display sensor values as osgText::text. show the orientation sensor. see updateOrientationSensor method.

**OsgCamera**: display camera image on an osg::Texture. see updateCamera method.

**OsgCameraBackground**: display camera image in the background of an osg view.

**OsgCameraOverlay**: display camera image in front of an osg view.

**OsgBitmap**: display bitmap from resources on an osg::Texture. see updateBitmap method.

OsgVideoMedia (coming soon)


Basic GUI
---------

OsgUIMenu:

OsgUIToast:


-------------------------------------
Raphael Grasset
http://www.raphaelgrasset.net
