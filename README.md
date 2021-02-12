# Programming-project_partial-differential_eq

#### The project presents a technique for numerically solving a broad class of partial differential equations (PDEs) and PDE systems using deep neural networks. The solved PDE is Burgers equation.

## Introduction
#### Partial differential equations (PDEs) are used to model a variety of phenomena in the natural sciences. Common to most of the PDEs encountered in practical applications is that they cannot be solved analytically but require various approximation techniques. Traditionally, mesh based methods such as finite elements (FEM), finite differences (FDM), or finite volumes (FVM), are the dominant techniques for obtaining approximate solutions. These techniques require that the computational domain of interest is discretized into a set of mesh points and the solution is approximated at the points of the mesh. The advantage of these methods is that they are very efficient for low-dimensional problems on regular geometries. The drawback is that for complicated geometries, meshing can be as difficult as the numerical solution of the PDE itself.  

#### The idea of solving differential equations by means of machine learning was introduced in 1996 by Isaac Lagaris, Aristidis Likas and Dimitrios Fotiadis (University of Ioannina, Greece).
They saw the following advantages in this approach: 
•	The solution learned by a neural network has a differentiable, closed analytic form.
•	The method is general.
•	Efficient implementation on parallel architectures 
They noted the further additional advantages of the method: 
•	The neural network solution showed good generalization properties on unseen points
•	A high accuracy could be achieved with much fewer parameters.

## Outline of the technique:

#### An important theoretical result that sheds some light on why neural networks perform well is the universal approximation theorem. In simple terms, this result states that any continuous function defined on a compact subset of R can be approximated arbitrarily well by a feed forward network with a single hidden layer. 
The current method approximates the solution to the PDE of interest with a deep neural network. With this parameterization, a loss function is set up to penalize the fitted function’s deviations from the desired differential operator and boundary conditions. The approach takes advantage is performed using stochastic gradient descent. The main insight of computational graphs and the back propagation algorithm to efficiently compute the differential operator while the boundary conditions are straightforward to evaluate. 
For the training data, the network uses points randomly sampled from the region where the function is defined and the optimization of this approach lies in the fact that the training data consists of randomly sampled points in the function’s domain. By sampling mini-batches from different parts of the domain and processing these small batches sequentially, the neural network “learns” the function without the computational bottleneck present with grid-based methods. This circumvents the curse of dimensionality which is encountered with the latter approach.

