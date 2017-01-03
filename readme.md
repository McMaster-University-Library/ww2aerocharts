# Leaflet Index Integrated Welcome and Guidance
*created by Lihong Li for McMaster University Library*

## Functionalities ##
This Welcome Modal is designed to display a popup window--with introduction and guidance information--overtop of the background web map (in the main window). The modal is made up of slides, containing images and text. The main functionalities are as follows:
* The user can click the left and right arrow in the slide to progress through the slides.
* The user can click “X” in the right top of the popup window or click wherever on the background window to close it.
* A button (reading “Click here for help”) is created on the left top corner of the background window. The user can click the button at any time to re-display the Welcome Guidance popup window.

## Technical Introduction ##
The Welcome Modal is implemented by using Html, CSS and Java Script technology. The files are as following –
* **index.html** : the main HTML file, implementing all functionalities described above. 
* **style.css** : a CSS file, implementing style control of the main html.
* **window.js** : a Java Script file, implementing dynamic functions.
* **image0.jpg, image1.jpg, image2.jpg…** : a series of image files to be shown in each slide. The recommendation is for all images to have width and height dimensions of 1200*600 pixels. 

## Integration Guidance ##
For the Welcome Modal integrated with another window, the main work will be as follows:

1. Copy above files to the target root dir. If there are conflicts of file name, you should change file name accordingly.
2. Open the file of index.html.
3. Copy the code line 4, 5 as below, then paste them to the related position in the main html file of background window.
    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" href="style.css">
    ```
4. Copy the code of from line 8 to line 69, then paste them to the related position in the main html file of background window.
5. Edit the main html file of the background window, you can change contents of every slide or add slides according to the code comments of modal.
6. Launch the main html file of the background window in browser to check the effect, you maybe need to change the position of both windows, so modify “position” and “z-index” style attribute in div. 

In the example below, the z-index value of the welcome/guidance modal is set to a higher number than the main map window, ensuring that it will be displayed above it. 
    ```html
    <div id="map" style="position:absolute; z-index:1">
    </div>		
    <div id="myModal" class="modal" style="position:absolute; z-index:2">
    ```