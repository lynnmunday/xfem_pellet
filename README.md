This simulation uses MOOSE combined app

The cubit journal file creates pelletonly4.e 
This mesh with a nodeset in the center to remove rotations.  modify the file to refine the mesh

The dummy edge crack exodus file make_edge_crack_in.e that is needed by the xfem mesh cutter is created by running
combined-opt -i make_edge_crack.i --mesh-only 

The simulation is now ready to run:
combined-opt -i xfem_crack_pelletonly.i

This is the output available in the following report

```text
@techreport{osti_2000030,
  author       = {Spencer, Benjamin W. and Munday, Lynn Brendon and Singh, Gyanender and Prithivirajan, Veerappan},
  title        = {Initial Fracture Propagation Modeling of Graphite Components with Grizzly},
  institution  = {Idaho National Laboratory (INL), Idaho Falls, ID (United States)},
  annote       = {Graphite has historically been extensively used in power reactor cores and will be used in multiple types of advanced reactors currently under development. These graphite structural components can experience significant stresses due to nonuniform volumetric strains induced by irradiation and thermal expansion, which can lead to fracture. Robust tools for predicting fracture initiation and propagation in graphite structural components in nuclear reactors are important for evaluating component integrity, developing design standards, and interpreting experimental results to characterize graphite performance. The U.S. Department of Energy’s Nuclear Energy Advanced Modeling and Simulation program has been developing degradation models for other structural components in nuclear reactors within the Grizzly and BlackBear codes. This report documents an effort to develop initial capabilities for modeling graphite fracture within these codes, building on prior efforts to model fracture in other materials. Major elements of this effort include developing a new system for modeling fracture nucleation and growth in two dimensions using the extended finite element method and incorporating a damage and plasticity model. These capabilities are applied here to model a representative graphite component and a splitting disc experiment used to obtain tensile strength.},
  doi          = {10.2172/2000030},
  url          = {https://www.osti.gov/biblio/2000030},
  place        = {United States},
  year         = {2023},
  month        = {06}}
```

output versus field data:

![9hr_flow](https://github.com/lynnmunday/xfem_pellet/blob/main/figures/stress.png)

![9hr_temp](https://github.com/lynnmunday/xfem_pellet/blob/main/figures/temperature.png)
