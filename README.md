# Programming-project_partial-differential_eq

#### The project presents a technique for numerically solving a broad class of partial differential equations (PDEs) and PDE systems using deep neural networks. The solved PDE is Burgers equation.

## Introduction
#### Partial differential equations (PDEs) are used to model a variety of phenomena in the natural sciences. Common to most of the PDEs encountered in practical applications is that they cannot be solved analytically but require various approximation techniques. Traditionally, mesh based methods such as finite elements (FEM), finite differences (FDM), or finite volumes (FVM), are the dominant techniques for obtaining approximate solutions. These techniques require that the computational domain of interest is discretized into a set of mesh points and the solution is approximated at the points of the mesh. The advantage of these methods is that they are very efficient for low-dimensional problems on regular geometries. The drawback is that for complicated geometries, meshing can be as difficult as the numerical solution of the PDE itself.  
The idea of solving differential equations by means of machine learning was introduced in 1996 by Isaac Lagaris, Aristidis Likas and Dimitrios Fotiadis (University of Ioannina, Greece).
They saw the following advantages in this approach: 
•	The solution learned by a neural network has a differentiable, closed analytic form.
•	The method is general.
•	Efficient implementation on parallel architectures 
They noted the further additional advantages of the method: 
•	The neural network solution showed good generalization properties on unseen points
•	A high accuracy could be achieved with much fewer parameters
