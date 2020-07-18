# PackingFrustration_Refinement
Atomic packing frustratometer using Rosetta

User Guidance of Atomic Frustratomter

Atomic Frustratometer computes the frustration patterns of any input PDB files. 

1: System Requirements.

Rosetta 2019.12 or after; 
numpy;
Python 2.7; 
Pymol;
VMD; 
Biopython;

2: Installation Guide. 
In order to carry out the relevant calculations, users only need to install Rosetta (under academic license) on their local computers or clusters. 
The post-rosetta calculations are performed with python, and all the relevant pacakges can be installed via Conda.
To visualize the results using either VMD or Pymol, users are suggested to download the relevant software. 

3: Demo. 
Folder example_input contains the input files and relevant scripts to compute atomic frustration for TOP7 (PDBID: 1QYS). 
Folder example_output contains the example result files (using 50 decoys only, for real purposes, users are encouraged to use >=200 decoys to obtain converged results).
To obtain similar results as the example results:
cd example_input;
./job.sh 1QYS.pdb 50;


It's gonna to take around 15 mins to finish the calculations, but the time cost might vary based on the different platforms. 


4: Instructions for use.
please execute the shell script by using the following command after you have prepared your PDB file:
./job.sh pdbid decoy_num
After finishing the calculations, users shall visualize the results using VMD or Pymol using the following commands:

To visualize using pymol, please use the following command: $path2pymol/PyMOL example.pdb example.pml
To visualize using VMD, please use the following command: $path2vmd/vmd example.pdb -e example.tcl


example_output/result_demo.pse is the saved pymol session file after visulization using Pymol, and example_output/result_demo.png is the sceenshot. 

This project is covered under the Academic Free License v3.0.
