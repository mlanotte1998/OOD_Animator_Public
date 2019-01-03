# OOD_Animator_Public

This repository has all of the information to use the end result of the "Easy Animator" from my Object Oriented Design class.

Due to the the instructors not wanting the code from the project to be public so they can continue using this project in the class, the code itself is not in this public repository. Instead, the jar file for the working project is here along with sample text files and the below instructions so that the animator can be used. 

## How to Use the Jar File 

In a terminal, move to the directory that contains the jar file and the given text files. Then type in:

```
java -jar OOD-EasyAnimator.jar -in textfile.txt -view aview -out output -speed number
``` 

The order of the -in, -view, -out, and -speed does not matter. Also, -speed is not required, and -out can only be used for the views of type "text" and type "SVG". 

### What Goes After the "-in"

  The argument that goes after -in is the text file that will be used in the animator for every type of view and is required for every view. An example of this input is all of the .txt files given in this repository, so an example of the input would be "-in buildings.txt"
  
  The text files given all follow a similar pattern that can be followed to make more text file animations. The pattern is bulleted below:
   
   * Declare the canvas with "canvas minX minY maxX maxY" where the four numbers after the word canvas are all integers. 
   * Then declare a shape by writing on a new line "shape name type_of_shape" where the word shape is always there followed by the name of the shape you are declaring and then the type of shape which is either a rectangle or ellipse. 
   * Then declare motions for a shape on a new line with "motion name_of_shape startingTime startingX startingY startingWidth StartingHeight startingRed startingGreen startingBlue endTime endX endY endWidth endHeight endRed endGreen endBlue". So, the word motion starts a new motion followed by the name of the shape that has to be already declared, and then all of e other words on the line are integers that describe the shape at the beginning of the motion and then at the end of the motion. Motions cannot overlap and motions must be in order of time and every motion after the first one for a shape must have a starting time that is the same as the last motion's end time. 
   * Motions and shape declarations can alternate in any way as long as motions for a shape happen after the shape has been declared. 
   * Shapes will show up above another shape if they overlap during the animation if they were declared after the other shape. 
   
### What Goes After the "-view" 

  There are only four options for the view input and one of them is required. The view is the way that the animation will be shown. Depending on which view is picked the -out field may be used. The four options are bulleted below: 
  
  * text : The text view displays the motions of each shape in order of the shapes that has a similar format of the motions are the input files. Text view descriptions if not given an output text file name will be written to the command line. If you want the description saved to a text file then include an name of a .txt file after the -out option. 
  * SVG : The SVG view outputs the animation in a text form that allows the animation to be played in a browser. If an ouput file is given then it will write the description to the file, otherwise it will be printed in the command line. If the description is in a .svg file then it can opened in a browser and the animation will play. If an output file is given it must be of the form .svg. A -speed input can be included and will alter the the description accordingly. The default speed is 1. 
  * visual : The visual view opens up a java window to play the animation and repeat it. The window can be closed to make the animation stop. This view should not have a -out option. A -speed input can be included to set the number of ticks per second. The default speed is 1. 
  * edit : The edit view is similar to the visual view but includes extra options to edit the animation, pause it, restart it, save it, etc. A more detailed description of all the options included in the edit view can be found later in the ReadMe. 
  
### What Goes After the -out

  The -out option is only to be used with a Text View or SVG view. The name of the file can be one that does or does not already exist. For the text view, a .txt file should be used, and for the SVG view a .svg file should be used. 
  
### What Goes After the -speed

  This option is the simply the speed of the animation. It can be included for all views except the text view. For every other view, if no speed is given, then each time in the text input file will equate that number of seconds. Inputting a speed of 2 will double the speed, 5 will mulitply the speed by 5, etc. Only integers can be included so a speed less than the original is not possible. 
  
## Edit View Explained 

The Edit View displays the animation the same way that the Visual View does but adds in multiple buttons so that the animation can be edited in different ways. The most basic buttons are on top of the java window and are the self explanatory start, pause, restart, and resume buttons. There is also a looping button that when colored the animation will restart on it's own when it ends and when off the animation will stay on the last frame of the motions. There is also a change speed button up top with these other named buttons that works when an integer is typed into the Desired Speed text box. The last item of importance in the upper window area is a scrubbar that moves as the animation runs and can be dragged to make the animation move further or rewind it. 

There is a java panel in the window that is below the previously mentioned buttons and on the left of the middle section that has the visualization of the animations. To the right of that there is three more panels that are more complicated than the buttons up top. The upper of the three panels shows every keyframe for every shape in the animation. A keyframe is all the specifics of a shape at a specific time. Another way to describe them is that every motion has a starting keyframe and an ending keyframe. The panel below that holds directions for how to use the buttons in the panel below that which have text boxes that go along with each button. In the panel at the bottom there are technically 9 buttons. The first 6 of them are explained in the middle panel. The non explained buttons are the Increase Layers button and the - and + buttons for shifting layers. Layers are an optional feature that can be added to the text input files so that shapes can be organized in layers. To make a animation layered, just add the word "layer" on  the top of the text file and then whenever you say the word "layer" next, all of the shapes below it will be in the next layer. If the input file was layered than the layer buttons can be used. Pressing the increase layer buttons adds an empty layer that can be visualized in the keyframe description panel. The shift layer allows an entire layer and all of the shapes in it to be shifted up or down. Include the layer number to be shifted and then press the + to move that layer up, and press the - to move it down. When the animation is layered, each layer is listed in the keyframe description and all of the shapes in a higher layer will be on top of the shapes in lower layers. By shifting for example layer 1 up, layer 1 will switch with layer 2 and the shapes that were previously in layer 1 will be in layer 2 and vice a versa. 

The last buttons of importance are up top but were not mentioned until now because they are very different than the simple start and pause etc. These two buttons are load and save. When load is pressed, a small pop up window will show up and ask the name of a new text file to load the animation without having to run the jar again. The save button also opens up a window and asks what name of a file you want and then if it should be a svg or txt file. Saving the animation creates either a .txt or .svg file similar to the text or svg output when given an output file. This can be useful for wanting to save a animation that was edited with new shapes or new layers or less keyframes or whatever else was done. If the save that is made is a .txt file, than that exact animation can be loaded in due to how similar the .txt output is to the input text files.  

## Thanks for reading and give the jar a try! 
