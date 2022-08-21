# Optical-flow-corona
In this project we are trying to track the CMEs using optical flow technique(a computer vision algorithm)
Intially we go through the different techniques available and we realise lucas kanade algorithm works best in this case thus we apply that
We start with tracking object's movement and trace its path and then inculcate its magnitude too.
For corner detection we use the Shi Tomsai algorithm over Harris(not much difference except for the R factor calculation).
After storing them(the magnitudes of veloctiy) in the form of csv 
we do data preprocessing to analyse it.

