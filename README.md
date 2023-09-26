# Opticalflow_CME
In this project we are trying to track the CMEs using optical flow technique(a computer vision algorithm)
Intially we go through the different techniques available and we realise lucas kanade algorithm works best in this case thus we apply that
We start with tracking object's movement and trace its path and then inculcate its magnitude too.
For corner detection we use the Shi Tomsai algorithm over Harris(not much difference except for the R factor calculation).
After storing them(the magnitudes of veloctiy) in the form of csv 
we do data preprocessing to analyse it.
When shifting to real LASCO C2 data which is very noisy we resort to Bilateral filtering
and analysing.

The model given above uses RNN with LTSM on csv files(with time series and Magnitudes of velocity alone) and predicts
the presence of a CME event in the given sequence.

You could train it and load the model and the inptus should be a csv file you get after running optical flow on the 
Bilateral filtered CME video you get.

The videos and frames that were analysed to train this CME detection model is given here: https://rb.gy/7e50h

Library mainly used here is opyflow by Dr.Gauthier : https://github.com/groussea/opyflow
