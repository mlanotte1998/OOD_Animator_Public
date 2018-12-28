# OOD_Animator_Public

This repository has all of the information to use the end result of the "Easy Animator" from my Object Oriented Design class.

Due to the the instructors not wanting the code from the project to be public so they can continue using this project in the class, the code itself is not in this public repository. Instead, the jar file for the working project is here along with sample text files and the below instructions so that the animator can be used. 

### How to Use the Jar File 

In a terminal, move to the directory that contains the jar file and the given text files. Then type in:

```
java -jar OOD-EasyAnimator.jar -in textfile.txt -view aview -out output -speed number
``` 

The order of the -in, -view, -out, and -speed does not matter. Also, -speed is not required, and -out can only be used for the views of type "text" and type "SVG". 

# What Goes After the "-in"

  The argument that goes after -in is the text file that will be used in the animator for every type of view and is required for every view. An example of this input is all of the .txt files given in this repository, so an example of the input would be "-in buildings.txt"
  
  The text files given all follow a similar pattern that can be followed to make more text file animations. The pattern is bulleted below:
   
   * Declare the canvas with "canvas minX minY maxX maxY" where the four numbers after the word canvas are all integers. 
   * 
