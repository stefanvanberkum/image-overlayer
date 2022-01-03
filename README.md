# Image Overlayer
Image overlayer using image registration with user-specified control points. Can be used to compare different depictions of the same setting. It is especially useful for comparing different maps, such as those in the toolbox image.

[![View Image Overlayer on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://nl.mathworks.com/matlabcentral/fileexchange/104250-image-overlayer)

# How to install?
- Runs on MATLAB and can be found in the MATLAB Add-On Explorer (File Exchange).
- After adding the toolbox to MATLAB, the Image Overlayer app will appear among your apps.

# How to use?
- Launch the Image Overlayer app.
- Select a base (will not be transformed) and overlay (will be transformed) image, by pressing ````Select base```` or ````Select overlay````, respectively.
- To start a new transformation:
  - Press ````Start new```` (this will clear any previously placed control points).
  - Select control points in the pop-up window.
  - Closing the pop-up window will transform your overlay image to (approximately) align its control points with their corresponding base image control points.
- To edit your control points:
  - Press ````Edit existing````.
  - Edit your control points in the pop-up window.
  - Closing the pop-up window will re-transform your overlay image.
- To save your currently selected control points, press ````Save points```` (this will save your points to a .mat file). Note that this will only save your control points, so make sure to remember which images they correspond to!
- To load a previously saved .mat file with control points, press ````Load points````. Note that you need to reselect the images that correspond to these control points yourself.
- The displayed correlation is a 2-D correlation coefficient (corr2), between the base and transformed overlay control points, which gives an idea of how well the algorithm was able to align these points. Note that it will be quite high in most cases, and that an increase in control-point correlation need not imply a better fit in general (it's mostly there because the correlation gauge looks cool).
- Four different types of output can be previewed directly in the app:
  - Color: false color by independently applying brightness scaling to each image (default imshowpair).
  - Base: the (untransformed) base image.
  - Overlay: the (transformed) overlay image.
  - Both: the overlay layed on top of the base image, with blue and red crosses depicting the base and overlay control points, respectively.
- To save the result, press ````Save result```` (this will save all four aforementioned types).
- To change the transformation type, select a transformation from the transformation drop-down menu. Projective is sufficient in most cases, but more flexible transformations can be chosen as well. Note that the transformed overlay control points (red) cannot be obtained for  `polynomial' 

# Package requirements
- Requires the MathWorks Image Processing Toolbox.
- Created for MATLAB R2021b.
