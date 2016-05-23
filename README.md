# PhotoCheck
This readme will help detail certain things that may help you to when coding the Photocode.
This code first starts being applicable and necessary in quadrant 2, hwoever, there is no harm in making it start working immediately. Therfore this code should be integrated near the start of the robots running.
This code should continue to operate until the robot reaches quadrant 4.
NOTE Quadrant four is now marked by a red square. Testing must be run to see what values we get for the color red in respoinse to different lighting. The best way I can see this working is by the code comparing the white and black value, then if the value of red is not within the normal values(of a which it wont be) it will therefore switch to IR. To be safe we could also have them robot take a step forward. 
We will be able to tell when we have entered quadrant 3 by the value of start of white and end of white being massive, possibly even the entire photo length. THis is because there is a "t" interesection at the start of this quadrant. At this point we should integrate the interesction navigator code.
-We need to get the course correction equation working ASAP.
Here I shall put a step by step method of what the method should do so that we can follow it when coding and so that we can use this in the final report.
+ = done
/+ = work in progress
/ = not done

- Initialises all the necessary variables +/
- Takes the photo + 
- Finds the white line and stores its position in an array +
- Then finds the start of the white line and the end of the white line so that the center of the white line can be calculated +
- Takes the curtrent value of the center of white in the picture and compares it against the "ideal" center of white. /+
- This is where it gets complex: +/
- "pid" Only we dont use "i" in this scenario
- "p" The current error will equal the current center of white - the "ideal" center of white(retest the ideal center of white) /+
- "d" The opposite direction of the direction robot is currently going. Never be larger than "p". THIS ALL REQUIRES TRIAL AND ERROR. For the coding team this is what we must come in and test. We need to puit in random values for d and p and see if it works, then adjust as necessary. /
- "i" The total error will equal the error value of the current photo plus the error value of previous photos. Treat this like a running total. // NOT NECESSARY
- The final step between is between this code and the integration of this code into the program.
