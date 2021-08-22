# Computer-Graphics
computer graphics using OPENGL

## LABORATORY SYLLABUS 📔 

## 1. Implement Brenham’s line drawing algorithm for all types of slope.  🕐
### DESCRIPTION
To display screen where the straight line segments are to be drawn. The
vertical axes show scan-line position and the horizontal axes identify pixel
columns
### OBJECTIVE
* To understand Brenham’s line drawing algorithm
### OUTCOME
* Students will be able to draw a line for all types of slope.

## ALGORITHM
**Bresenham’s Line-Drawing Algorithm** for |m| < 1.0
1. Input the two line endpoints and store the left endpoint in (x0, y0).
2. Set the color for frame-buffer position (x0, y0); i.e., plot the first point.
3. Calculate the constants _x, _y, 2_y, and 2_y − 2_x, and obtain the starting value or the decision parameter as p0 = 2_y − _x
4. At each xk along the line, starting at k = 0, perform the following test: If pk < 0, the next point to plot is (xk + 1, yk ) and pk+1 = pk + 2_y Otherwise, the next point to plot is (xk + 1, yk +1) and pk+1 = pk + 2_y − 2_x
5. Repeat step 4 _x − 1 more times.

<br>

## 2. Create and rotate a triangle about the origin and a fixed point.
## DESCRIPTION 🕑
A triangle is transformed from its original position to the desired
transformation using the composite- matrix calculations in procedure
transformVerts2D.
## OBJECTIVE
To understand rotation of a triangle about the origin and a fixed point
To understand the method of drawing triangle object using simple GL
primitives.
## OUTCOME
Students will be able to rotate triangle.

<br>

## 3.Draw a colour cube and spin it using OpenGL transformation matrices. 🕒
## DESCRIPTION
The program draws a cube using GL_POLYGON primitive. For each
vertex of the cube different color is given so that the cube becomes colorful.
Whenever mouse left, right, or middle buttons are pressed the cube will spin
along x axis, y axis or z axis respectively.
## OBJECTIVE
To understand rotation transformation
To understand the method of drawing 3D objects using simple GL primitives.
## OUTCOME
Students will be able to animate 3D colored objects.
## ALGORITHM
1. Initialize vertices, normal’s and colors of the color cube. Also initialize theta and axis.
2. Define main()
* Enable display mode as double and depth buffer.
* Register mouse and idle callback function.
* Enable depth test.
3. Define reshape () enabling glOrtho.
4. Define mouse callback mouse(), coding for left, middle and right buttons for x, y and z axis respectively.
5. Define idle callback spincube()
* Increment theta for every click.
* Reinitialize theta
If theta > 360 then theta 0
* Call display()
6. Define callback function display()
* Load identity matrix.
* Define rotation function for x, y & z axis.
* Draw the color cube using right hand rule.
* Swap buffers for there is animation in the scene

<br>

## 4.Draw a color cube and allow the user to move the camera suitably to experiment with perspective viewing. 🕓
## DESCRIPTION
The program creates a cube using GL_POLYGON primitive. For
each vertex of the cube different color is given so that the cube looks
colorful. x, X, y, Y, z and Z keys are used to move camera for
perspective viewing. Whenever mouse left, right, or middle buttons are
pressed the cube will rotate along x axis, y axis or z axis respectively.
## OBJECTIVE
Understand perspective viewing model with respect to camera
movements.
## OUTCOME
Students will be able to implement perspective viewing model with
respect to
camera movements.
## ALGORITHM
1. Initialize vertices, normals and colors of the color cube. Also initialize theta, axis and viewer position.
2. Define main()
* Enable display mode as double and depth buffer.
* Register mouse and keyboard callback function.
* Enable depth test.
3. Define reshape(). Enable either glFrustum or gluPerspective for perspective viewing.
4. Define mouse callback mouse()
* Program for left, middle and right buttons for x, y and z axis respectively.
* Increment theta for every click.
* Reinitialize theta If theta > 360 then theta ->0
* Call display()
5. Define keyboard callback keys() Program for moving the viewer towards or away from the object by incrementing or decrementing by 1, for x, y & z keys for respective directions accordingly.
6. Define callback function display()
* Load identity matrix and gluLookAt for viewer.
* Define rotation function for x, y & z axis.
* Draw the colorcube using righthand rule.
* Swap buffers for there is animation in the scene.

<br>

## 5. Clip a lines using Cohen-Sutherland algorithm. 🕔
## DESCRIPTION
The program draws a clipping window with the line which has to be clipped and calls Cohen- Sutherland line-clipping algorithm. The
algorithm divides a two-dimensional space into 9 regions, and then efficiently determines the lines and portions of lines that are visible in
the center region of interest (the viewport). The clipped line and clipping window will be scaled and displayed as output.
## OBJECTIVE
* To understand the concept of clipping
* Learning Cohen-Sutherland line-clipping algorithm
## OUTCOME
* Students will be able to implement Cohen Sutherland line clipping
algorithm and
**compare the same with Liang barsky algorithm.**
## ALGORITHM
1. Given a line segment with endpoint and
2. Compute the 4-bit codes for each endpoint. If both codes are 0000,(bitwise OR of the codes yields 0000 ) line lies completely inside the window: pass the endpoints to the draw routine. If both codes have a 1 in the same bit position (bitwise AND of the codes is not 0000), the line lies
outside the window. It can be trivially rejected.
3. If a line cannot be trivially accepted or rejected, at least one of the two endpoints must lie outside the window and the line segment crosses a window edge. This line must be clipped at the window edge before being passed to the drawing routine.
4. Examine one of the endpoints, say p1=(x1,y1), read p1's
4-bit code in order: Left-to-Right, Bottom-to-Top.
5. When a set bit (1) is found, compute the intersection I of the
corresponding window edge with the line from p1 to p2 Replace p1 with I and repeat the algorithm.

<br>

## 6. To draw a simple shaded scene consisting of a tea pot on a table. Define suitably the position and properties of the light source along with the properties of the surfaces of the solid object used in the scene. 🕕
## DESCRIPTION
The cube is scaled in different axis’s to form walls, table legs and table
top. The Tea pot is placed on the table. Color and shading for all the
objects and Lightning are provided with the help of OpenGL functions.
## OBJECTIVE
* Understand the complexities of Lighting and shading
* Learn to use openGL function to draw 3D objects.
## OUTCOME
* Students will be able to demonstrate how real-world
lighting
conditions are approximated by OpenGL
* Able to render illuminated objects by defining the different properties
of light and material.
## ALGORITHM
1. Initialize ambient, diffuse, specular & shininess material properties. Also initialize light intensity & position.
2. Define main()
* Enable display mode as single, RGB and depth buffer.
* Register shading with GL_SMOOTH.
* Use viewport for (0,0,xmax,ymax)
* Enable LIGHTING, LIGHT0, depth test & normalize.
* Define reshape by gluLookAt() & clear() with color & depth buffer bit.
4. With the help of glutSolidCube () form a table (legs &top) and 3D wall. Use transformation functions translate, rotate and scale
prefixed and suffixed by glPushMatrix() and PopMatrix() respectively.
5. Define display()
* Set ambient, diffuse, specular & shininess for glMaterials ().
* Set light intensity & position for glLightfv()
* Call draw_wall() & draw_table().
* Use glutSolidTeapot() to place it on the table.

<br>

## 7. Design, develop and implement recursively subdivide a tetrahedron to form 3D sierpinski gasket. The number of recursive steps is to be specified by the user. 🕖
## DESCRIPTION:
When the user provides a number as input, this number specifies the number of times tetrahedron has to be subdivided to form 3D
Sierpinski gasket. This algorithm finds midpoint of each edge of tetrahedron and with the help of one vertex of tetrahedron and
midpoints it divides the tetrahedron. The process of finding midpoints and subdividing tetrahedron is a recursive process.
## OBJECTIVE:
* To analyze and draw 3D objects
* Learning 3D Sierpinski gasket algorithm
## OUTCOME:
* At the end of this lab session, the student will be able to Students will be able create 3D geometric figures using
openGL function.
## ALGORITHM
1. Initialize 4 vertex points of tetrahedron.
2. Define main()
a. Enable display mode as single and depth buffer.
b. Enable depth test.
3. Define Reshape() with glOrtho.
4. Define display()
* Call tetrahedron() where 4 different colors are given for each face and call divide_triangle() for each face.
* In divide triangle each face is recursively sub-divided into 3 triangles using midpoint of edges, n number of times.
* In triangle() a triangle is plotted using polygon primitives

<br>

## 8.Develop a menu driven program to animate a flag using Bezier Curve algorithm. 🕗
## DESCRIPTION
A simple Bezier Curve algorithm.
## OBJECTIVE
* To learn Bezier Curve algorithm.
## OUTCOME
* Students will be able to implement Bezier Curve algorithm.

<br>

## 9. Develop a menu driven program to fill the polygon using scan line algorithm. 🕘
## DESCRIPTION
A simple polygon with four edges is created and color is filled
with the help of scan- line area filling algorithm
## OBJECTIVE
* To learn scan line polygon fill algorithm.
## OUTCOME
* Students will be able to implement scan-line area filling algorithm to fill irregular objects.
## ALGORITHM
1. Define main ( ) having display mode as Single Buffer and myinit ( ) having gluOrtho2D.
2. Draw a desired polygon.
3. Initialize left edge to xmax of window and right edge to zero.
4. Conduct edge detect test for all sides of the polygon to compute the left and right edge boundary coordinates for each scan line of the scene.
5. For y <-0 to ymax
If le[y] less than
re[y] then
For i
<-le[y] to
re[y]
Draw pixel(I,y)
End for

## What Is OpenGL?
OpenGL is a software interface to graphics hardware. This interface consists of about 150
distinct commands that you use to specify the objects and operations needed to produce
interactive three-dimensional applications.
OpenGL is designed as a streamlined, hardware-independent interface to be implemented
on many different hardware platforms. To achieve these qualities, no commands for
performing windowing tasks or obtaining user input are included in OpenGL; instead, you
must work through whatever windowing system controls the particular hardware you're
using. Similarly, OpenGL doesn't provide high-level commands for describing models of
three-dimensional objects. Such commands might allow you to specify relatively.
complicated shapes such as automobiles, parts of the body, airplanes, or molecules. With
OpenGL, you must build up your desired model from a small set of geometric primitives -
points, lines, and polygons.
A sophisticated library that provides these features could certainly be built on top of
OpenGL. The OpenGL Utility Library (GLU) provides many of the modeling features,
such as quadric surfaces and NURBS (Non-Uniform Rational B-Splines) curves and
surfaces. GLU is a standard part of every OpenGL implementation. Also, there is a higher-
level, object-oriented toolkit, Open Inventor, which is built atop OpenGL, and is available
separately for many implementations of OpenGL.

## OpenGL-Related Libraries
OpenGL provides a powerful but primitive set of rendering commands, and all higher-
level drawing must be done in terms of these commands. Also, OpenGL programs have to
use the underlying mechanisms of the windowing system. A number of libraries exist to
allow you to simplify your programming tasks, including the following:

* The OpenGL Utility Library (GLU) contains several routines that use lower-level
OpenGL commands to perform such tasks as setting up matrices for specific
viewing orientations and projections, performing polygon tessellation, and
rendering surfaces. This library is provided as part of every OpenGL
implementation. GLU routines use the prefix glu.

* For every window system, there is a library that extends the functionality of that
window system to support OpenGL rendering. For machines that use the X
Window System, the OpenGL Extension to the X Window System (GLX) is
provided as an adjunct to OpenGL. GLX routines use the prefix glX. For Microsoft
Windows, the WGL routines provide the Windows to OpenGL interface. All WGL
routines use the prefix wgl. For IBM OS/2, the PGL is the Presentation Manager to
OpenGL interface, and its routines use the prefix pgl.

* The OpenGL Utility Toolkit (GLUT) is a window system-independent toolkit,
written by Mark Kilgard, to hide the complexities of differing window system
APIs. GLUT routines use the prefix glut.

* Open Inventor is an object-oriented toolkit based on OpenGL which provides
objects and methods for creating interactive three-dimensional graphics
applications. Open Inventor, which is written in C++, provides prebuilt objects and
a built-in event model for user interaction, high-level application components for
creating and editing three-dimensional scenes, and the ability to print objects and
exchange data in other graphics formats. Open Inventor is separate from OpenGL.
## Include Files
For all OpenGL applications, you want to include the gl.h header file in every file. Almost
all OpenGL applications use GLU, the aforementioned OpenGL Utility Library, which
requires inclusion of the glu.h header file. So almost every OpenGL source file begins
with
#include <GL/gl.h>
#include <GL/glu.h>

* If you are directly accessing a window interface library to support OpenGL, such as GLX,
AGL, PGL, or WGL, you must include additional header files. For example, if you are
calling GLX, you may need to add these lines to your code
#include <X11/Xlib.h>
#include <GL/glx.h>

* If you are using GLUT for managing your window manager tasks, you should include
#include <GL/glut.h>

* Note that glut.h includes gl.h, glu.h, and glx.h automatically, so including all three files is
redundant. GLUT for Microsoft Windows includes the appropriate header file to access
WGL.
## GLUT, the OpenGL Utility Toolkit
As you know, OpenGL contains rendering commands but is designed to be independent of
any window system or operating system. Consequently, it contains no commands for
opening windows or reading events from the keyboard or mouse. Unfortunately, it's
impossible to write a complete graphics program without at least opening a window, and
most interesting programs require a bit of user input or other services from the operating
system or window system.

* In addition, since OpenGL drawing commands are limited to those that generate simple
geometric primitives (points, lines, and polygons), GLUT includes several routines that
create more complicated three-dimensional objects such as a sphere, a torus, and a teapot

This way, snapshots of program output can be interesting to look at. (Note that the
OpenGL Utility Library, GLU, also has quadrics routines that create some of the same
three-dimensional objects as GLUT, such as a sphere, cylinder, or cone.)

## Important features of OpenGL Utility Toolkit (GLUT)
* Provides functionality common to all window systems.
* Open a window.
* Get input from mouse and keyboard.
* Menus.
* Event-driven.
* Code is portable but GLUT lacks the functionality of a good toolkit for a specific
platform.
* No slide bars.
* OpenGL is not object oriented so that there are multiple functions for a given
logical function :
glVertex3f
o glVertex2i
o glVertex3dv

* Underlying storage mode is the same easy to create overloaded functions in C++
but issue is efficiency.

## OpenGL Interface
o GL (OpenGL in Windows)
o GLU (graphics utility library)
uses only GL functions, creates common objects (such as spheres)
o GLUT (GL Utility Toolkit)
interfaces with the window system
o GLX: glue between OpenGL and Xwindow, used by GLUT

* Window Management
Five routines perform tasks necessary to initialize a window.

glutInit(int *argc, char ** argv) initializes GLUT and processes any command line
arguments (for X, this would be options like -display and -geometry). glutInit()
should be called before any other GLUT routine.

## glutInitDisplayMode(unsigned int mode) specifies whether to use an RGBA or
color-index color model. You can also specify whether you want a single- or
double-buffered window. (If you're working in color-index mode, you'll want to
load certain colors into the color map; use glutSetColor() to do this.) Finally, you
can use this routine to indicate that you want the window to have an associated
depth, stencil, and/or accumulation buffer. For example, if you want a window
with double buffering, the RGBA color model, and a depth buffer, you might call
glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB | GLUT_DEPTH).

* glutInitWindowPosition(int x, int y) specifies the screen location for the upper-
left corner of your window.

* glutInitWindowSize(int width, int size) specifies the size, in pixels, of your
window.

* int glutCreateWindow(char *string) creates a window with an OpenGL context. It
returns a unique identifier for the new window. Be warned: Until glutMainLoop()
is called (see next section), the window is not yet displayed.
The Display Callback
glutDisplayFunc(void (*func)(void)) is the first and most important event callback
function you will see. Whenever GLUT determines the contents of the window need to be
redisplayed, the callback function registered by glutDisplayFunc() is executed. Therefore,
you should put all the routines you need to redraw the scene in the display callback
function.
If your program changes the contents of the window, sometimes you will have to call
glutPostRedisplay(void), which gives glutMainLoop() a nudge to call the registered
display callback at its next opportunity.
Running the Program
The very last thing you must do is call glutMainLoop(void). All windows that have been
created are now shown, and rendering to those windows is now effective. Event
processing begins, and the registered display callback is triggered. Once this loop is
entered, it is never exited!.

## Instructions for using OpenGL and GLUT for Windows XP machines with Microsoft Visual Studio.Net 2003
If you are using OpenGL on your computer at home:
* All Windows systems since Windows 98 have OpenGL preinstalled.
* Download GLUT. Go to the CSCI 4250 pages web site
(http://www.mtsu.edu/~csjudy/4250) and visit the “Links to OpenGL sites”. You
will find a site for downloading GLUT.

* When you down load it, it will be a zip file. You will have to unzip it. Then place
the glut32.dll file in the windows\system32 directory.

* If your system is configured like the ones at MTSU, you will need to place the
glut.h file in the \Program Files\Microsoft Visual Studio .Net
2003\vc7\PlatformSDK\Include\ GL folder and the glut32.lib file in the
Program Files\Microsoft Visual Studio .Net 2003\vc7\PlatformSDK\Lib folder.
To use Microsoft Visual Studio.Net 2003:

* Start Microsoft Visual C++ -- click on Start, Programs, Microsoft Visual
Studio .Net 2003, Microsoft Visual Studio .Net 2003

* Create a new project by selecting FileNewProject...Visual C++ Projects
 Win32 Project. Give your project a name (use your last name followed by the
number of the project for the name of the project), select the appropriate disk or
hard drive, and click on OK. On the subsequent window, select Application
Settings. In the next window, select Empty Project and Console Application
then click on Finish.

* To create the files that should be placed in the project, you should select Project,
Add New Item, and then select the type of files that you are creating.

To create an executable, compile Build Build Solution or Build  Rebuild
Solution (Compiles and Links.)

You can then run your executable by typing (CTRL + F5) or selecting Debug Start Without Debugging
Graphics Programming Using OpenGL in Visual C++
* Opengl32.dll and glu32.dll should be in the system folder.
* Opengl32.lib and glu32.lib should be in the lib folder for VC++.
* gl.h and glu.h should be in a folder called GL under the include folder for VC++.
* Get glut32.lib, glut32.dll and glut.h from the course homepage and put them in the
same places as the other files.
* Fire up visual studio.
* Create a new project as the following :
File  New  Project (input your project name, then a directory (workspace) with
the same name will be built)
* Win32 Console Application
* An Empty Application
* In the workspace click on “File View” to access (expand) the source code tree.
* In “Source Files”, add in the source code (*.cpp files).
* Select Project  Settings  Link and in “Object/library modules” add
“Opengl32.lib glu32.lib glut32.lib”.

* Press “F7” to build “your_project.exe”.
Basic OpenGL Elements - Programming 2D Applications
A vertex is a location in space
glVertex** is in the form of nt or ntv
n is the number of dimensions
t denotes the data type:
integer (i), float (f), or double (d);
pointer to an array (v)
## Examples :
glVertex2i(GLint xi, GLint yi)
glVertex3f(GLfloat x, GLfloat y, GLfloat z)

GLfloat vertex[3]
glVertex3fv(vertex)
OpenGL Object Examples
glBegin (mode);
glVertex2f (x 1 , y 1 );
glVertex2f (x 2 , y 2 );
glVertex2f (x 3 , y 3 );
glVertex2f (x 4 , y 4 );
glEnd ();
where mode = GL_POINTS, GL_LINES, GL_LINE_STRIP, GL_POLYGON,
GL_LINE_LOOP, etc.
Lines of zero length are not visible.
A vertex is considered to be just a location with zero mass.
Only 10 of the OpenGL functions are legal for use between glBegin and glEnd.

## Examples:
glBegin(GL_LINES);

glVertex2f(x1, y1);

glVertex2f(x2, y2);

glEnd();

glBegin(GL_POINTS);

glVertex2f(x1, y1);

glVertex2f(x2, y2);

glEnd();

## Graphics Functions
## Primitive functions:
points, line segments, polygons, pixels, text, curves, surfaces
Attributes functions: color, pattern, typeface
### Some Primitive Attributes
glClearColor (red, green, blue, alpha); - Default = (0.0, 0.0, 0.0, 0.0)

glColor3f (red, green, blue); - Default = (1.0, 1.0, 1.0)

glLineWidth (width); - Default = (1.0)

glLineStipple (factor, pattern) - Default = (1, 0xffff)

glEnable (GL_LINE_STIPPLE);

glPolygonMode (face, mode) - Default = (GL_FRONT_AND_BACK, GL_FILL)

glPointSize (size); - Default = (1.0)

## Viewing functions:
position, orientation, clipping
Transformation functions: rotation, translation, scaling

Input functions: keyboards, mice, data tablets
Control functions: communicate with windows, initialization, error handling

Inquiry functions: number of colors, camera parameters/values
## Matrix Mode
There are two matrices in OpenGL:
## Model-view: 
defines COP and orientation
## Projection:
defines the projection matrix
glMatrixMode(GL_PROJECTION);

glLoadIdentity();

gluOrtho2D(0.0, 500.0, 0.0, 500.0);

glMatrixMode(GL_MODELVIEW);

## Control Functions
* OpenGL assumes origin is bottom left
* glutInit(int *argcp, char **argv);
* glutCreateWindow(char *title);
* glutInitDisplayMode(GLUT_RGB | GLUT_DEPTH | GLUT_DOUBLE);
* glutInitWindowSize(480,640);
* glutInitWindowPosition(0,0);
* OpenGL default: RGB color, no hidden-surface removal, single buffering
Obtaining Values of OpenGL State Variables
glGetBooleanv (paramname, *paramlist);

glGetDoublev (paramname, *paramlist);

glGetFloatv (paramname, *paramlist);

glGetIntegerv (paramname, *paramlist);

## Saving and Restoring Attributes
glPushAttrib (group);

glPopAttrib ( );

where group = GL_CURRENT_BIT, GL_ENABLE_BIT, GL_LINE_BIT,

GL_POLYGON_BIT, etc.

## Projection Transformations

glMatrixMode (GL_PROJECTION);

glLoadIdentity ( );

glFrustum (left, right, bottom, top, near, far);

gluPerspective (fov, aspect, near, far);

glOrtho (left, right, bottom, top, near, far);

- Default = (-1.0, 1.0, -1.0, 1.0, -1.0, 1.0)
- 
gluOrtho2D (left, right, bottom, top);

## Modelview Transformations
glMatrixMode (GL_MODELVIEW);

glLoadIdentity ( );

gluLookAt (eye_x, eye_y, eye_z, at_x, at_y, at_z, up_x, up_y, up_z);

glTranslatef (dx, dy, dz);

glScalef (sx, sy, sz);

glRotatef (angle, axisx, axisy, axisz);

## Writing Bitmapped Text
glPixelStorei (GL_UNPACK_ALIGNMENT, 1);

glColor3f (red, green, blue);

glRasterPos2f (x, y);

glutBitmapCharacter (font, character);

where font = GLUT_BITMAP_8_BY_13, GLUT_BITMAP_HELVETICA_10,

etc.
## Managing the Frame Buffer

glutInit (&argc, argv);

glutInitDisplayMode (GLUT_RGB | mode);

glutInitWindowSize (width, height);

glutInitWindowPosition (x, y);

glutCreateWindow (label);

glClear (GL_COLOR_BUFFER_BIT);

glutSwapBuffers ( );

where mode = GLUT_SINGLE or GLUT_DOUBLE.

## Registering Callbacks
glutDisplayFunc (callback);

glutReshapeFunc (callback);

glutDisplayFunc (callback);

glutMotionFunc (callback);

glutPassiveMotionFunc (callback);

glutMouseFunc (callback);

glutKeyboardFunc (callback);

id = glutCreateMenu (callback);

glutMainLoop ( );

## Display Lists

glNewList (number, GL_COMPILE);

glEndList ( );

glCallList (number);

glDeleteLists (number, 1);

## Managing Menus

id = glutCreateMenu (callback);

glutDestroyMenu (id);

glutAddMenuEntry (label, number);

glutAttachMenu (button);

glutDetachMenu (button);

where button = GLUT_RIGHT_BUTTON or GLUT_LEFT_BUTTON.



