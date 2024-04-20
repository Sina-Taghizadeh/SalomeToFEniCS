# SalomeToFEniCS
A Shell script for converting Salome med files to xml files for use in FEniCS

# Description

FEniCS is an open-source software for solving boundary and initial value problems using the finite element method based on the weak form or variational form of the problem. Since it is not possible to generate complex geometries with this software, it is necessary to use other CAD software such as FreeCAD and Salome interactively with FEniCS. In FreeCAD we can have a direct export to FEniCS, but since there is no possibility of marking and transferring to FEniCS, it is only applicable for single materials and for composites we have to use Salome software. The output format of Salome software is med file which is not directly usable by FEniCS and we need an intermediary software called Gmsh which converts the mesh file with med extension to a file with msh extension which can be converted to xml format files by the FEniCS converter.

# How to Use

After designing the geometry in Salome software and defining the desired groups in it, take the output file with med extension. For a simple and illustrative example, we design a binary composite as shown below in Salome and after meshing, we take the output file MyComposite.med which is placed in the repo.

![image](https://github.com/Sina-Taghizadeh/SalomeToFEniCS/assets/162900845/be3b06a9-7001-44af-b4d9-01bca0a1f5f5)

After giving the permission to run the med2xml program with the following command, we can get the msh file and the xml files required by Fenics.

```./med2xml YourMedFileName.med```

For example, in our example, by running this command, the MyComposite.med file is converted into four files MyComposite.msh, MyComposite.xml, MyComposite_facet_region.xml and MyComposite_physical_region.xml which are placed in the repo.
Now you can use the xml files in Fenics software.

# Collaboration

It is important to note that this code is written for Salome version 9.9.0, gmsh version 4.11.1, and the latest version of FEniCS Legacy. However, it may also work for other versions. If you have made any changes to it or have developed it for other versions, I would appreciate it if you could share the updated code.

sina.taghizadeh123@gmail.com

# Acknowledgments:

This code is an updated version of the code by Dr. Bilen Emek Abali in his book "Computational Reality". For more information about the FEniCS software, please refer to his valuable book.
