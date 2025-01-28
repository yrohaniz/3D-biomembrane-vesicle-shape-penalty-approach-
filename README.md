# 3D-biomembrane-vesicle-shapes-penalty-approach-
Neural network solver for the 3D shape of vesicles made of lipid bilayers (membrane) calculated by a phase-field approach to the Helfrich model

This is an NN solver for the 3D shape of vesicles that are made of lipid bilayers, which are modeled by a continuum model i.e., phase field. The governing PDE for the shape of the vesicle is the well-known Helfrich elastic bending energy subject to constraints on the surface area and the volume. We have also introduced another contstraint on the center of mass, which ensures that the vesicle remains anchored to the origin of the simulation box. The initial data for the shape is provided as trained parameters for a spherical vesicle in the saved_model_0 folder. 

The user needs to assign the required constraint on the volume or the surface area ideally using sys.argv[1]. This code is written for a serial implementation of applying constraints where for each new constraint a 20000-epoch training is recommended.

In the penalty approach, the constraints on the surface area, volume and center of mass are imposed by including penalty terms in the cost(loss) function used for training (optimizing the parameters of the NN).
