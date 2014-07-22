---
layout: post
title: H Bridge and Safety
---

One issue I have been thinking about is how fast should the one motor spin backwards while turning? Wicker has suggested testing with actual hardware and seeing which one just looks right. I have written some code for this exact testing. It has a lot of... issues for now.

I have not figured out a good system to deal with naming. LTR should not be a variable name but here we are. The primary reason for all the weird variable names is that there are multiple copies of everything so I name them by location. This means LTR translates to the pin controlling the Left Top Right Transistor. Some of this could be eliminated by creating different names, but the more I abstract away from the hardware and diagrams the more difficult it is to ensure I know what is happening. I am not sure I believe that I know what is going on now.

On top of that, it is difficult to know how to name variables which will be used to define others. Right now, I have the eyeballs providing an integer value which will control the motors. Eyeball (techincally eyeballLeft and eyeballRight) is reading from the pin and writing to a new variable which will be manipulated to give an integer in the range the motors read. I want all three of these variables to be named eyeball, but that will just make the code harder to read. Also, I do not think C will let me do that since one of them is not an integer. It is a... pin reading? maybe?

Should I force safe state at the beginning of the loop? By safe state I mean 'turn all the transitors off' or 'make sure none of the transistors are conducting'. If I do, yay safe state which will protect the transistors and possibly other things I do not yet know are vulnerable. I think I have found a way to protect everything without safe state, but its only about 8 lines less than if I add safe state. Another option is to add a way for the program to know previous state of the loop, which would allow me to remove safe states. Oh crap, I just realized in my current code, I used ifs instead of elifs. I need to fix that, because even with current safe states, that is ineffecient.

Additionally, I still do not know how transistors work. So far I can use the successfully but that just feels like saying 'my ignorance has not yet led to any noticable problems'.

Next step, I need to make the chassis so I can begin testing on the ground.
