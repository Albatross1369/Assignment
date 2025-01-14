# isciml
Imaging using SCIentific Machine Learning (ISCIML) is intended to produce training data for three-dimensional imaging via inversion of magnetic data. The technology is broadly applicable and can be used in a variety of real-world situations, such as pipeline imaging, UXO identification, and mineral prospecting. To speed up and improve the efficiency of the calculations, the code uses parallel computing and sophisticated mathematical approaches.

The code first sets up the necessary tools using a number of Python libraries and modules, which makes it possible to perform the computations more quickly. To effectively handle huge three-dimensional models and lower computational complexity, the code makes use of parallel and distributed computing with MPI.

The code creates a Mesh class that creates nodes, tetrahedral nodes, centroids, and volumes for a mesh from a VTK file, a type of file used in 3D modelling. This aids in computing the magnetic field values.

Also, a class called MagneticAdjointSolver does calculations to determine the magnetic field values depending on input data. Using a Mesh object and a MagneticProperties object as inputs, the solution method of this class is called, and it returns the magnetic field values.

The isciml() function, which reads YAML configuration files, creates a Mesh object using a VTK file specified in the configuration file, a MagneticProperties object using a magnetic properties file specified in the configuration file, and solves for the magnetic field using the MagneticAdjointSolver object. A NumPy binary file is used to store the output.
