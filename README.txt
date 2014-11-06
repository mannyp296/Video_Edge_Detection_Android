					README
By: Manuel Perez
ECE 150 HW 3

Design:

Activity Class:
The activity class holds most of the application's functionality. It
starts by creating the layout and then sets a camera view listener.
The display is initially made up of a camera preview with a button
on top with the text "Edge Detection". If the button is pressed then
the fucntion goes on  the onclick function and executes code where the
onChangeView fucntion sets either the view into edge detection or back
to the original view. When the view changes to edge detection, the text
on the button changes to "Go To Preview" and when the view mode changes
to the original view the button changes back to "Edge Detection". The
alternating modes is set by modifying the mViewMode whihc determines the
view of the camera. Using mViewMode we are able to trasnlate eveyr frame
of the video through the function onCameraFrame(). If the camera is
going back to the original view, then the camera just gets acolor image.
However when function calls for the edge dection the native
cannyEdgeDetection() fucntion is called.

cannyEdgeDetection() (C++):
This fucntion contians jlong objects which are the adresses to the Mat
type objects used in the function. The Mat variables are invoked and they
are used in the Canny() to create the edge detection preview. As the
adresses of the variables were passed ther eis no need to return a
variable.

Note: The OpenCV Tutorial 2 - Mized Processing sample from the OpenCV
Library-2.4.8 was used as  base for this application.

Question:

Example:
Log.i(TAG, "OpenCV loaded successfully");

This code prints "OpenCV loaded successfully" when OpenCV is loaded
sucessfully on the Manager connector. The string is pritned to LogCat
which displays the messages from the code as the applicaiton runs
through the code. The Log.i is what the directs the text to the
Logcat as green text for information. Mewhile a Log.e is used for
errors and exceptions and prints as red text.

TO download OpenCV 2.4.8 visit opencv.org