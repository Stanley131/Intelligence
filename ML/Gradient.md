### Gradient method
  - In optimization, gradient method is an algorithm to solve problems of the form 
    min(f(x))
  - find minimum 
  
### 1. Gradient descent（steepest descent）
  - Gradient descent is a first-order iterative optimization algorithm for finding
  a local minimum of a differentiable function. To find a local minimum of a 
  function using gradient descent, we take steps proportional to the negative 
  of the gradient (or approximate gradient) of the function at the current point.
  But if we instead take steps proportional to the positive of the gradient, we 
  approach a local maximum of that function; the procedure is then known
  as gradient ascent. Gradient descent was originally proposed by Cauchy in 1847.
  
  - Gradient is a vector that is tangent of a function and points in the direction of 
  greatest increase of this function. Gradient is zero at a local maximum or minimum 
  because there is no single direction of increase. In mathematics, gradient is defined
  as partial derivative for every input variable of function. For example, we have a
  function:
  
  - advantage: 
    -  The advantage of Batch Gradient Descent is that the algorithm is more computational
    efficient and it produces a stable learning path, so it is easier to convergence.
  - disadvantage: However, Batch Gradient Descent takes longer time when the training set is large.

### 2. Stochastic gradient descent
  - Stochastic gradient descent (often abbreviated SGD) is an iterative method for optimizing an objective
  function with suitable smoothness properties (e.g. differentiable or subdifferentiable).
  It can be regarded as a stochastic approximation of gradient descent optimization, 
  since it replaces the actual gradient (calculated from the entire data set) by an 
  estimate thereof (calculated from a randomly selected subset of the data).[1] Especially
  in big data applications this reduces the computational burden, achieving faster iterations
  in trade for a slightly lower convergence rate.[2]
  
  - 
  
  
  
  
  
  
