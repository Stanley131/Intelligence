### 1. What is SVM?
  - SVM is a classifier formally defined by a separating hyperplane. An hyperplane is a subspace of one dimension less than
    its ambient space. The dimension of a mathematical space (or object) is informally defined as the minimum number of 
    coordinates (x,y,z axis) needed to specify any point (like each blue and red point) within it while an ambient space 
    is the space surrounding a mathematical object. A mathematical object is an abstract object arising in mathematics An
    abstract object is an object which does not exist at any particular time or place, but rather exists as a type of thing,
    i.e., an idea, or abstraction (wikipedia).
  
### 2. What is Kernel?
   - K(x, y) = <f(x), f(y)>. Here K is the kernel function, x, y are n dimensional inputs. f is a map from n-dimension 
    to m-dimension space. < x,y> denotes the dot product. usually m is much larger than n.
   - Kernel is a way of computing the dot product of two vectors 𝐱 and 𝐲 in some (possibly very high dimensional) feature 
     space, which is why kernel functions are sometimes called "generalized dot product". 
     Suppose we have a mapping 𝜑:ℝ𝑛→ℝ𝑚 that brings our vectors in ℝ𝑛 to some feature space ℝ𝑚. Then 
     the dot product of 𝐱 and 𝐲 in this space is 𝜑(𝐱)𝑇𝜑(𝐲). A kernel is a function 𝑘 that corresponds to this
     dot product, i.e. 𝑘(𝐱,𝐲)=𝜑(𝐱)𝑇𝜑(𝐲).
### Definition of a kernel function 
  - symmetry: 𝑘(𝑥,𝑦)=𝑘(𝑦,𝑥)
  - positive semi-definiteness.
    
  
### 3. Gussian Kernel 
  - Another interesting kernel examples is Gaussian kernel. Given two vectors, the similarity will diminish with
    the radius of 𝜎. The distance between two objects is "reweighted" by this radius parameter. 
    
### 4. Conveity 
  - f(a * x1 + (1 - a) * x2) <= a f(x1) + (1-a)f(x2) 
  - if second derivative is greater than 0 
  - Function of d variables 
    - value: number 
    - Derivative: d-dimensional vector 
    - Second derovative d x d matrix 
    - Hessian 
### 5. The Kernelk Trick Significance
    - dot rpoducts are a measure of similarity 
    - Convert to euclidean data from real world objects 
    - As long as the function that we build takes two objects and returns the user defined 
      simliarities. 
### 6. Perceptron adn linear Separability 
    - which perceptron is better when there are multuple percetrons?
    - which perceptron algo return? Find a better generalized data algorithm. 
    - perceptron cannot guarantee the best decision boundry but a legitimate one 
    - SVM will have the bias term unlike the perceptrons. 
    
### 7. SVM formmulation 
1. What does the distance between two parallel lines mean?
    - wx - b >= +1 if y = +1 
    - wx - b <= =1 if y = -1  
    - why not radius distance?
    
2. Math optimizatiom problem 
    - maximize 2/|w|
    - minimize |w| => square this to be make it easier to optimize 
    - sunch that y(xw - b) >= 1 
    - constrained optimization problem 
    - assumption is that no noise. 
   
3. How to generalize this problem(non-separable case)?
    - introduce to slack for the mis-classified points, and minimize the slack. 
    - you don't have to do any separate preporcessing
    - all variables so far: w, b, slack 
    - Also known as SVM standard(primal) from with slack: 
    - a primal form means only one variable. 
    - Introduce the slace: y(xw - b) >= 1 - theta 
    - what does it mean for any slack? it means any solutions 
    - minimize the |w|^2/2 + C sum of (theta)
    - why use linear slack? it depends on the problem, ut linear is easier 
4. How to solve it?
    - Cannot simply take the derivative w, b, theta and examine the stationary points 
    - Why? cuz Gradient not zero at the function minima respecting the constraints. 
    - The dimentsion is n+ d + 1. 
5. Detour : Constrained Optimization 
    - minize f(x)
    - Feasible problem: assume there is one x such that it satisfying the problem 
    - projection methods: start with a feasible solutions x0, and find x1 that is 
      slightly lower objective value, if xj violates the constraints, project back
      to the contraints.
    - Penalty methods 
    - The Lagrange Penalty Method: 
        L(x, lambda)  = f(x)  + sum  
   
   
   
   
   
   
   
   
   
   
   
   
   
    
    
    
