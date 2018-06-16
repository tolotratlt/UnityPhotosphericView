# Unity PhotosphericView
Photosphere view using procedural inverted normal sphere and custom unlit equirectangular shader to avoid big texture distorsion

## Getting Started
Original idea [Andrewnoske PanoramaViewer](http://www.andrewnoske.com/wiki/Unity_-_Panorama_Viewer)

* Put InvertedSphere.cs into /Assets/Editor folder
* Generate a procedural sphere (normal inverted) with custom radius (ex: 20) ( Menu > GameObject > Insert Other > Inverted Sphere... )
* Use equirectangular.shader as sphere's material

Essential source file [InvertedSphere](https://gist.github.com/tolotratlt/70e8a3790cfb1839a21587d70dd2fda2)


### Notes
* The problem with original idea is that texture present big distortion issue with conventional unlit shader, that's why custom equirectangular shader for inverted sphere was created
* shader uses shader model 3.0 and requires OpenGL ES 3.0 to work properly. If you want to compile for android, check manualy the API version to OpenGL ES 3.0. remove OpenGL ES 2.0 otherwise Unity will freeze.
* The generated sphere (manually with 3d modeling software or procedurally with unity) **MUST** be normal inverted otherwise it will not work
