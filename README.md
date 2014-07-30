ADisc_hemisphere_segmentation
=============================

Adaptive disconnection method for brain MRI hemisphere segmentation 

The 'Brain Hemisphere Segmentation' package is designed to use the Adaptive
Disconnection method to segment the brain volume in 3D MRI into the left 
cerebral hemisphere, right cerebral hemisphere, left cerebellum, right 
cerebellum and brainstem. The method is described in 

L. Zhao, U. Ruotsalainen, J. Hirvonen, J. Hietala and J. Tohka.
Automatic cerebral and cerebellar hemisphere segmentation in 3D MRI:
adaptive disconnection algorithm. Medical Image Analysis, 14(3):360-372, 
2010.

http://www.ncbi.nlm.nih.gov/pubmed/20303318

L. Zhao and J. Tohka. Automatic compartmental decomposition for 3D MR 
images of human brain. Proc. of 30th Annual International Conference 
of the IEEE Engineering in Medicine and Biology Society, EMBC08, pages
3888-3891, Vancouver, Canada, August 2008.

http://www.ncbi.nlm.nih.gov/pubmed/19163562

and it was part of Lu Zhao's PhD work in the group led by Jussi Tohka.

To use the package, first, you should compile the 'Info_Map_Gen.c' file 
into mex-file (mex file for 32-bit and 64-bit Windows are included already). This 
can be done, most of the time, by using the matlab script: 
'mex Info_Map_Gen.c'. 

The main function is 'Adaptive_Disconnection.m'. To implement the segmentation, 
input the tissue fraction estimates and the voxel size of the processed image
into 'Adaptive_Disconnection.m'. The output is a matrix containing the 
segmented(labeled) brain volume. It is recommended to produce the tissue 
fraction estimates using 

https://github.com/jussitohka/pvemri

Matlab's image processing toolbox is also required.
