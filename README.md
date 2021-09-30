# barcode_reader_mathematica
About This is an implementation of the algorithm described in the paper "Robust Recognition of 1-D Barcodes Using Camera Phones Steffen Wachenfeld, Sebastian Terlunen, Xiaoyi Jiang Computer Vision and Pattern Recognition Group, Department of Computer Science, University of Munster, Germany"

This was coded in Mathematica (version 11.2.0.0 home edition). The location of the imput jpeg is set in the line

 image=Import["C:\\Users\\Gerard\\Desktop\\business\\barcodes\\barcode1_mbdb.jpg"];
 
 In the guardBars function, the intensity threshold for subsequent points can be set
 guardBars[scanline, 0.1];
 
 In the barcode function, the first argument is the  step and the last argument is the delta so the average bar lengths for black and white bars is varied  avgBarLength1 - delta to avgBarLength1 + delta in incremental steps of d
 
 barcode[0.1, bars, avgBarLength1, avgBarLength0, 0.0];
 
The results for the ten sample images are

size of images 600x400

Name			          I. Diff Found	    Step	Delta

barcode1_mbdb.jpg   0.1			False     0.1	  0.0

barcode2_mbdb.jpg	  0.1			True			0.1	  0.0

barcode3_mbdb.jpg	  0.5			True			0.1	  0.0

barcode4_mbdb.jpg	  0.01		True			0.1	  0.0

barcode5_mbdb.jpg	  0.01		True			0.1	  0.0

barcode6_mbdb.jpg	  0.1			True			0.1	  0.0

barcode7_mbdb.jpg	  0.1			True			0.1	  0.0

barcode8_mbdb.jpg	  0.1			True			0.1	  0.0

barcode9_mbdb.jpg	  0.1			False			0.1	  0.0

barcode10_mbdb.jpg  0.1			True			0.1	  0.0
