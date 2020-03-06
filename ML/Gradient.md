### Gradient method
  - In optimization, gradient method is an algorithm to solve problems of the form 
    min(f(x))
  - find minimum 
  - The loss function computes the error for a single training example, while the 
   cost function is the average of the loss functions of the entire training set.
  
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
  
  - Gradient Descent is the most common optimization algorithm in machine learning and deep learning. 
  It is a first-order optimization algorithm. This means it only takes into account the first derivative
  when performing the updates on the parameters. On each iteration, we update the parameters in the 
  opposite direction of the gradient of the objective function J(w) w.r.t the parameters where the 
  gradient gives the direction of the steepest ascent. The size of the step we take on each iteration
  to reach the local minimum is determined by the learning rate α. Therefore, we follow the direction 
  of the slope downhill until we reach a local minimum.
  
  source: https://towardsdatascience.com/gradient-descent-algorithm-and-its-variants-10f652806a3
    
  - Steps: 
      -  Initialize weight w and bias b to any random numbers.
      - Pick a value for the learning rate α. The learning rate determines
          how big the step would be on each iteration.
          - If α is very small, it would take long time to converge and become computationally expensive.
          - If α is large, it may fail to converge and overshoot the minimum.
          - The most commonly used rates are : 0.001, 0.003, 0.01, 0.03, 0.1, 0.3.
      - Make sure to scale the data if it’s on a very different scales. If we don’t scale the data, 
        the level curves (contours) would be narrower and taller which means it would take longer 
        time to converge 
      - On each iteration, take the partial derivative of the cost function J(w) w.r.t each 
        parameter (gradient)
          - w = w - alpha * gradient 
          - b = b - alpha * gradient
      - For the sake of illustration, let’s assume we don’t have bias. If the slope of the current 
        value of w > 0, this means that we are to the right of optimal w*. Therefore, the update will
        be negative, and will start getting close to the optimal values of w*. However, if it’s 
        negative, the update will be positive and will increase the current values of w to converge
        to the optimal values of w*
      - Continue the process until the cost function converges. That is, until the error curve 
        becomes flat and doesn’t change.
        
      - In addition, on each iteration, the step would be in the direction that gives the maximum
        change since it’s perpendicular to level curves at each step.
          
  - advantage: 
    -  The advantage of Batch Gradient Descent is that the algorithm is more computational
    efficient and it produces a stable learning path, so it is easier to convergence.
  - disadvantage: However, Batch Gradient Descent takes longer time when the training set is large.
  
  
### 2. Batch Gradient Descent
  - Batch Gradient Descent is when we sum up over all examples on each iteration when performing
    the updates to the parameters. Therefore, for each update, we have to sum over all examples:
    - for i in range(num_epochs):
        grad = compute_gradient(data, params)
        params = params — learning_rate * grad
  - Advantage: 
      - We can use fixed learning rate during training without worrying about learning rate decay.
      - It has straight trajectory towards the minimum and it is guaranteed to converge in theory
        to the global minimum if the loss function is convex and to a local minimum if the loss
        function is not convex.
      - It has unbiased estimate of gradients. The more the examples, the lower the standard error.
      
  - Disadvantage: 
      - Even though we can use vectorized implementation, it may still be slow to go over all 
        examples especially when we have large datasets.
      - Each step of learning happens after going over all examples where some examples may be
        redundant and don’t contribute much to the update.
     
### 3. Mini-batch Gradient Descent
  - Instead of going over all examples, Mini-batch Gradient Descent sums up over lower number of 
    examples based on the batch size. Therefore, learning happens on each mini-batch of b examples:

### 4. Stochastic gradient descent
  - Stochastic gradient descent (often abbreviated SGD) is an iterative method for optimizing an objective
  function with suitable smoothness properties (e.g. differentiable or subdifferentiable).
  It can be regarded as a stochastic approximation of gradient descent optimization, 
  since it replaces the actual gradient (calculated from the entire data set) by an 
  estimate thereof (calculated from a randomly selected subset of the data).[1] Especially
  in big data applications this reduces the computational burden, achieving faster iterations
  in trade for a slightly lower convergence rate.[2]
  
  - Instead of going through all examples, Stochastic Gradient Descent (SGD) performs the 
    parameters update on each example (x^i,y^i). Therefore, learning happens on every example:
  
  - Shuffle the training data set to avoid pre-existing order of examples.
  - Partition the training data set into m examples.
      - for i in range(num_epochs):
      -    np.random.shuffle(data)
      -    for example in data:
      -    grad = compute_gradient(example, params)
      -    params = params — learning_rate * grad
   - Advantages: It adds even more noise to the learning process than 
      mini-batch that helps improving generalization error. However, this would increase the run time.
  
### 5. Stochastic gradient descent  with SGDM 
  - Momentum or SGD with momentum is method which helps accelerate gradients vectors in the right
    directions, thus leading to faster converging. It is one of the most popular optimization algorithms
    and many state-of-the-art models are trained using it. 
    
   - SGD has trouble navigating ravines, i.e. areas where the surface curves much more steeply
    in one dimension than in another [1], which are common around local optima. In these 
    scenarios, SGD oscillates across the slopes of the ravine while only making hesitant 
    progress along the bottom towards the local optimum as in Image below. This helps 
    accelerate SGD in the relevant direction and dampens oscillations. 
 
 ### 6. Nesterov accelerated gradient
  - While Momentum first computes the current gradient (small blue vector in Image 4) and 
    then takes a big jump in the direction of the updated accumulated gradient (big blue
    vector), NAG first makes a big jump in the direction of the previous accumulated gradient
    (brown vector), measures the gradient and then makes a correction (red vector), which
    results in the complete NAG update (green vector). This anticipatory update prevents 
    us from going too fast and results in increased responsiveness, which has significantly
    increased the performance of RNNs on a number of tasks

### Adaptive Gradient
  - 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
