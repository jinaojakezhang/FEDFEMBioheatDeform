# Fast computation of soft tissue thermal response under deformation based on fast explicit dynamics finite element algorithm for surgical simulation (MIT License)

![fig1](https://user-images.githubusercontent.com/93865598/147800686-7eff7605-090f-4865-add3-94d4fd37b47d.PNG)

This is the source repository for the paper:

Zhang, J., & Chauhan, S. (2020). Fast computation of soft tissue thermal response under deformation based on fast explicit dynamics finite element algorithm for surgical simulation. Computer Methods and Programs in Biomedicine, 187, 105244. [doi:10.1016/j.cmpb.2019.105244](https://www.sciencedirect.com/science/article/abs/pii/S0169260719311344).

which is based on the works of [doi:10.1016/j.ijthermalsci.2019.01.030](https://www.sciencedirect.com/science/article/abs/pii/S1290072918317186) [[Code]](https://github.com/jinaojakezhang/FEDFEM), and [doi:10.1080/10407790.2019.1627812](https://www.tandfonline.com/doi/abs/10.1080/10407790.2019.1627812) [[Code]](https://github.com/jinaojakezhang/FEDFEMBioheat).

Please cite the above paper if you use this code for your research.

# Environment:
•	Windows 10

•	Visual Studio 2017

•	OpenMP
# How to build:
1.	Download the source repository.
2.	Visual Studio 2017->Create New Project (Empty Project)->Project->Add Existing Item->BioheatDeform.cpp.
3.	Project->Properties->C/C++->Language->OpenMP Support->Yes (/openmp).
4.	Build Solution (Release/x64).
# How to use:
1.	(cmd)Command Prompt-> ![fig2](https://user-images.githubusercontent.com/93865598/147800688-6464dded-72c5-44e2-a883-7e72acb47030.PNG)
2.	Output: T.vtk, U.vtk, and Undeformed.vtk
# How to visualize:
1.	Open T.vtk and U.vtk. (such as using ParaView)

![fig3](https://user-images.githubusercontent.com/93865598/147800691-66567c43-9659-4f7f-9a72-3ae46178564b.PNG)
# Boundary condition (BC):
1.	Node index: Disp, FixP, HFlux, FixT.
2.	Element index: Perfu, BodyHFlux.
3.	All Elements: Gravity, Metabo.
# Notes:
1.	Node and Element index can start at 0, 1, or any but must be consistent in a file.
2.	Liver_Iso.txt, node and element index start at 0; Liver_Iso_n1.txt, node and element index start at 1.
