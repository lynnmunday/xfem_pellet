This simulation uses MOOSE combined app

The cubit journal file creates pelletonly4.e 
This mesh with a nodeset in the center to remove rotations.  modify the file to refine the mesh

The dummy edge crack exodus file make_edge_crack_in.e that is needed by the xfem mesh cutter is created by running
combined-opt -i make_edge_crack.i --mesh-only 

The simulation is now ready to run:
combined-opt -i xfem_crack_pelletonly.i
