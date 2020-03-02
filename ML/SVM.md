### What is SVM?
  - SVM is a classifier formally defined by a separating hyperplane. An hyperplane is a subspace of one dimension less than
    its ambient space. The dimension of a mathematical space (or object) is informally defined as the minimum number of 
    coordinates (x,y,z axis) needed to specify any point (like each blue and red point) within it while an ambient space 
    is the space surrounding a mathematical object. A mathematical object is an abstract object arising in mathematics An
    abstract object is an object which does not exist at any particular time or place, but rather exists as a type of thing,
    i.e., an idea, or abstraction (wikipedia).
  
### What is Kernel?
   - K(x, y) = <f(x), f(y)>. Here K is the kernel function, x, y are n dimensional inputs. f is a map from n-dimension 
    to m-dimension space. < x,y> denotes the dot product. usually m is much larger than n.
   - Kernel is a way of computing the dot product of two vectors 𝐱 and 𝐲 in some (possibly very high dimensional) feature 
     space, which is why kernel functions are sometimes called "generalized dot product". 
     Suppose we have a mapping 𝜑:ℝ𝑛→ℝ𝑚 that brings our vectors in ℝ𝑛 to some feature space ℝ𝑚. Then 
     the dot product of 𝐱 and 𝐲 in this space is 𝜑(𝐱)𝑇𝜑(𝐲). A kernel is a function 𝑘 that corresponds to this
     dot product, i.e. 𝑘(𝐱,𝐲)=𝜑(𝐱)𝑇𝜑(𝐲).
### Definition
  - symmetry: 𝑘(𝑥,𝑦)=𝑘(𝑦,𝑥)
  - positive semi-definiteness.
    
  
