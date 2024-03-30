# piEstimation
Short code that uses monte carlo simulation to estimate pi

The code selects points randomly in a unit square, with uniform distribution, and calculates how many of them land inside a quarter circle of radius 1, based at (0,0). Let alpha = |number of points in circle|/|total number of points|. Then alpha = pi/4. Our estimate of pi = 4*alpha.

To select points randomly in a unit square choose the x-coordinate and y-coordinate from the open unit interval using random.random(), from the python random module. The distribution on these two random variables is uniform. It doesn't matter whether points are selected from [0,1] or from (0,1) because the probability measure on {0} and {1} is zero. 

Finally, see that the product X\times Y of the random variables is a uniform distribution over a unit square. Both X and Y have the probability density distribution \rho (which is uniform). The density distribution of X\times Y is \rho\tensor\rho:I^2\rightarrow[0,\infty). Let (a,b) be an arbitrary point in the unit square. \rho\tensor\rho(a,b)=\rho(a)*\rho(b), which is the same for all (a,b). Therefore the distribution is uniform. 
