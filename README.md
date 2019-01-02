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
  
  * Text : The text view displays the motions of each shape in order of the shapes that has a similar format of the motions are the input files. Text view descriptions if not given an output text file name will be written to the command line. If you want the description saved to a text file then include an name of a .txt file after the -out option. 
  * SVG : The SVG view outputs the animation in a text form that allows the animation to be played in a browser. If an ouput file is given then it will write the description to the file, otherwise it will be printed in the command line. If the description is in a .svg file then it can opened in a browser and the animation will play. If an output file is given it must be of the form .svg. A -speed input can be included and will alter the the description accordingly. The default speed is 1. 
  * Visual : The visual view opens up a java window to play the animation and repeat it. The window can be closed to make the animation stop. This view should not have a -out option. A -speed input can be included to set the number of ticks per second. The default speed is 1. 
  * Edit : The edit view is similar to the visual view but includes extra options to edit the animation, pause it, restart it, save it, etc. A more detailed description of all the options included in the edit view can be found later in the ReadMe. 
  
### What Goes After the -out
