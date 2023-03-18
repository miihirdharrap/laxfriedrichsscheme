# laxfriedrichsscheme
This code gives a sense of traffic propagation over time and space for the given condition on the road patch.
Kindly go through the problem statement uploaded to get the idea of the initial conditions, boundary conditions and the time and space jump
The basic idea of the code is to first try and fit a curve to the given scatter plot between flow and density.
The scatter plot between flow and density has been extracted from the "Zurich - Sheet1"
I then divided the scatter plot into two parts as I felt it a bit teadious and difficult to fit a single curve on the dataset
I have used Scipy-curvefit and poly fit and tried fitting conic sections and polynomials 
Finally a deg 2 polynomial fits best to the given dataset.
#NOTE THAT :- In Matlab it is possible to fit a single 4th Degree polynomial or a 9th Degree polynomial and it fits better than the deg 2 polynomial.
Then the space time plot is defined and the initial and the boundary conditions are set onto the 2D matrix.
The dimensions can be found from the time and space jump given.
After this the lax friedrichs scheme is applied and the propagation can be seen in the csv file, "lax_friedrichs_output".
the next step is to view this in 3 Dimensions and have a sense of what's going on on the road patch.
A small curved-wave like curve can be seen signifying that the traffic is moving forward and the density is decreasing with time.
Then Finally the variation of density with respect to time is extracted at 4 time instances viz. 10, 30, 60, and 90 Minutes since the start of the road.
