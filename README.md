# High-Performance-Computing
High performance computing module at University of Bristol. Implemented coding solutions using the University of Bristol's 600 teraflop supercomputer - Blue Crystal phase 4.

For assignments, the weighted 5-point stencil problem was used. [more info](https://github.com/ya17227/High-Performance-Computing/blob/main/src/README.md)

<br/>

| <img src="https://github.com/ya17227/High-Performance-Computing/blob/main/images/blueCrystal.png" width=500> |
| :-: |
| *UoB's Blue Crystal* |

<br/>
<br/>

## Assignment 1: Serial Optimisation
Applied serial optimisations like compiler choice, compiler flags, data layouts, data types, vectorisation, etc to improve performance of a 5-point stencil code run on a single CPU core.

[click here for report](https://github.com/ya17227/High-Performance-Computing/blob/main/Serial%20Optimisation/report.pdf)


<img src="https://github.com/ya17227/High-Performance-Computing/blob/main/images/compilerFlag.png" width=1000> | <img src="https://github.com/ya17227/High-Performance-Computing/blob/main/images/stencil.png" width=900> |
:-------------------------:|:-------------------------: 
 *compiler flags* | *Stencil image (1024x1024)*


<br/>

## Assignment 2: Distributed memory parallelism with MPI
Programmed a multi-core system using Message Passing Interface (MPI) and Single Program Multiple Data (SPMD) to achieve distributed memory parallelism. 

- Single Program meaning all processing units (cores) execute the same instruction at any given clock cycle. Multiple Data meaning each processing core can operate on a different data elements.
This approach is best suited for specialised problems characterised by a high degree of regularity, such as graphics/ image processing. Since stencil is an image problem SIMD would be perfect here.
- The Message Passing Interface (MPI) protocol was used to achieve point-to-point communication among processes.
- The Stencil code was run on one core up to all the 56 cores of 2 compute nodes.

[click here for report](https://github.com/ya17227/High-Performance-Computing/blob/main/MPI/report.pdf)

<br/>

| <img src="https://github.com/ya17227/High-Performance-Computing/blob/main/images/scatter.png" width=300> |
| :-: |
| *multi-core approach : scattering and gathering data* |


<br/><br/><br/>


 <img src="https://github.com/ya17227/High-Performance-Computing/blob/main/images/1core.png" width=600> | <img src="https://github.com/ya17227/High-Performance-Computing/blob/main/images/56core.png" width=600>
:-: | :-: 
 *code running on 1 core* | *code running on 56 cores*
