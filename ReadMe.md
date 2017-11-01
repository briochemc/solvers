# MATLAB solvers

These solvers were edited from the solvers available at [this link](http://www.siam.org/books/fa01/), where you can find MATLAB code written by C. T. Kelley (2003). These solvers attempt to solve f(x)=0 for large sparse nonlinear systems.

Differences with original code:
- The jcobians are now computed numerically using MATLAB's built-in `numjac`. 
- The code indentation has been corrected.
- The unused subfunctions have been cut.
- The factorization of the jacobian by `lu` has been replaced by the use of MATLAB's `linfactor` which I believe adds an extra permutation step speeding things up.

## To do
- [ ] Include the complex derivative for numerical precision of the gradient (only for when f is twice differentiable in C (needed for complex numbers to go through the derivative).
- [ ] Allow for color groups `G` to be used as input to avoid the first slow numjac calculation.
