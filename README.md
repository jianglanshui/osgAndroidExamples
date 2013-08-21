osgAndroidExamples
==================

A list of examples combining [OpenSceneGraph](http://www.openscenegraph.com) and Android. 

The architecture of the samples are based on the original code from [osgAndroidExampleGLES2](https://github.com/openscenegraph/osg/tree/master/examples/osgAndroidExampleGLES2) developed by Jorge Izquierdo Ciges (distributed with OSG, using embedded viewer). 
You will find some of the features demonstrated in osgAndroidExampleGLES2 in separated examples here as well as additionanl examples (location, sensor, camera, etc.).


Tested with: **OpenSceneGraph-3-2.0 + Android NDKr9 + Nexus 10**.

The source code come as Android 2.3.1 (API 9) eclipse project, ABI platform 9, armeabiv7-a, neon on (modify the Android.mk, Application.mk
and Eclipse project configuration files for any changes).

Basic
-----
OpenGL ES 2.0 Rendering with OSG.

Note: The OsgDisplay examples correspond to traditional OSG examples find in a lot of common tutorials, if you know well OSG they are not really relevant for you (main difference here is related to ES 2.0 shaders).


**OsgGLView**: basic osg renderer. Create an activity, instantiate a default GL View and GL Renderer, call init, update, resize native functions.You get a default OSG renderer.

**OsgGLView2**: basic osg renderer. Same as OsgGLView but use a layout configuration (main_activity.xml) to associate the View to the main activity.

**OsgDisplayGeometry**: basic osg geometry rendering. Display a triangle (geometry, vertex array) with a simple shader (no lighting, default vertex transfo, hardcoded color). 
Shader code use gl_ binding automatically converted by OSG (lazy mode) and default binding (osg_Vertex for binding vertex array).

**OsgDisplayGeometry2**: basic osg geometry rendering. same as OsgDisplayGeometry without using automatic conversion: you need to use and declare osg_ variable in your shaders 
and use default attrib binding (e.g. osg_Vertex automatically binds to a vertex array declaration).

**OsgDisplayGeometry3**: basic osg geometry rendering. same as OsgDisplayGeometry2 without using automatic conversion and default binding: you need to do the binding yourself between
shader attributes and your arrays.

**OsgDisplayGeometryColor**: basic osg geometry rendering with color. Same as OsgDisplayGeometry using a uniform for the color.

**OsgDisplayGeometryColor2**: basic osg geometry rendering with color. Same as OsgDisplayGeometry using color array.

**OsgDisplayGeometryTexture**: basic osg geometry rendering with texture. same as OsgDisplayGeometry using a built in texture.

**OsgDisplayGeometryLighting** (coming soon)

**OsgDisplayText**: basic text. Display a basic text with a really simple shader.

**OsgDisplayTransfo**: basic osg transformation. Same as OsgDisplayGeometry with a MatrixTransform applied to the triangle.

**OsgDisplayAnim**: basic osg animation. Same as OsgDisplayGeometry with an update of triangle orientation in the main loop.

**OsgDisplayAnim2** (coming soon)

**OsgGLViewNative** (coming soon)

**OsgGLViewES3** (coming soon)


Basic Viewer
------------
Rendering with standard OSG viewer (support touch, keyboard input, camera manipulators).

Note: please note that using camera manipulator will modify default CS (without: OpenGL standard, with: GIS standard).

**OsgUITouch**: touch input. Display touch values as osgText::Text ("mouse" input). See OSGGLView and updateTouch method.

**OsgUITouch2** (coming soon)

**OsgUIKeyboard**: keyboard input. Display keyboard values as osgText::Text. See OSGGLView. See OSGGLView and updateTouch method.

**OsgViewer**: basic viewer. Use touch + keyboard information for the viewer, can be use for creating handlers.

**OsgViewe2**: basic viewer with stats. Enable stats with decorator from Aurelien Albert ([decorator with shader](http://lists.openscenegraph.org/pipermail/osg-submissions-openscenegraph.org/2013-February/009873.html)).

**OsgViewer3**: basic viewer with camera manipulator. Use touch + keyboard informatino for the viewer with a camera manipulator (Trackball).

Android Resources
-----------------
Access Android resources (sensors, resources management) from a native OSG application. 

**OsgLocation**: location input. display location values as osgText::Text. see updateLocation method.

**OsgSensor**: sensor input. display sensor values as osgText::text. show the orientation sensor. see updateOrientationSensor method.

**OsgCamera**: camera input. display camera image on an osg::Texture. see updateCamera method.

**OsgCameraBackground**: camera input. display camera image in the background of an osg view.

**OsgCameraOverlay**: camera input. display camera image in front of an osg view.

**OsgBitmap**: bitmap resources. display bitmap from resources on an osg::Texture. see updateBitmap method.

**OsgVideoMedia** (coming soon)


Basic GUI
---------

**OsgUIMenu**  (coming soon)

**OsgUIControlOverlay**  (coming soon)

**OsgUIToast**  (coming soon)


-------------------------------------
Raphael Grasset
http://www.raphaelgrasset.net
