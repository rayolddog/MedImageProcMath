# MedImageProcMath
Medical image processing with Mathematica
repository is for Mathematica code segmenting an axial CT body image into body pixels, and non body pixels. The segmentation is useful for calculation of Size Specific Dose Estimate (SSDE).  The segmentation of body axial CT images can be accomplished with well established techniques.  This allows a fast calculation of SSDE.  The SSDE is one of the best available parameters to optimize the tradeoff between the risk of radiation exposure, and the usefullness of the medical image for diagnosis.  If actual calculation of a patient's radiation exposure is required, more computationally complex techniques of x-ray photon transport simulation are required.  This program is useful only as an educational tool.  Currently, a large number of medical facilities are unaware of the usefullness of SSDE.
This repository contains both ".nb" format and ".pdf" format documents.  ".nb" are files that can be executed with Mathematica.

There are now three programs listed that demonstrate basic morphologic image processing for application to Computed Tomography exams.  The programs are provided in MATLAB, Mathematica, and Python computer languages. Please see the other repositories.  The programs read the DICOM format file to obtain the metainformation and image data.  The image is segmented to separate the area of interest from the background. Based on pixel dimensions included in the metainformation, the equivalent disk diameter is calculated.  The equivalent water disk diameter is then calculated using the pixel attenuation values contained within the body pixels.

The programs were used to calculate the equivalent disk diameter of a CT phantom.  The CT phantom has a known diameter.  Therefore the results can be compared to a known true value.  In this case, the Mathematica parameters used for a morphologic algorithm were based on measurements from the phantom.  Both the MATLAB program, and the Python program rely on the Otsu method of determining thresholds for morphologic segmentation.

The programs are intended as examples Medical Physicists can use to program a tool for calculating SSDE from CTDIvol.  The SSDE tool can demonstrate how the calculation of Size Specific Dose Estimate is a better measure of radiation exposure for optimizing the tradeoff between radiation exposure and image quality.  The majority of CT facilities use older measures of CT radiation exposure.  By demonstrating the calculation of SSDE (which can be automated), CT facilities may be convinced to adopt the better method of optimizing radiation exposure. The SSDE provides a better parameter for predicting image noise and radiation exposure. 

If users plan to use these programs, some modifications will be necessary. The programs would have to be modified to reflect the folder where axial CT images are found (often provided on an optical disk).  Programs may also have to be modified to reflect different values in the metainformation included in the DICOM image header. The metainformation in the DICOM headers of different CT manufactures vary.  The DICOM header metainformation should include information about the dimensions of individual pixels.  The Mathematica program does contain the formula for calculating SSDE from CTDIvol (SSDE conversion factor) based on the equivalent disk diameter.  This should provide enough information for users to modify the program for their own use.
