# Predicting Individual Quality Ratings of Compressed Images through Deep CNNs-based Artificial Observers (AI Observers)

This software constitutes the AI Observers models (trained Matlab NNs) presented in the paper 

[**Predicting Individual Quality Ratings of Compressed Images through Deep CNNs-based Artificial Observers**](https://doi.org/10.1016/j.image.2022.116917)

by Lohic Fotio Tiotsop, Antonio Servetti, Marcus Barkowsky, Peter Pocta, Tomas Mizdos, Glenn Van Wallendael, Enrico Masala,  
Signal Processing: Image Communications, vol. 112, Mar 2023, pp. 1-15,   
DOI: 10.1016/j.image.2022.116917 (ISSN: 0923-5965)  ([Link to author's version](https://media.polito.it/web/res/2023/01/Fotio_SPIC2023_author_version.pdf))

The software is provided free of charge, see [LICENSE.txt](./LICENSE.txt) file for further conditions.
*We kindly ask anyone using the software to cite the previous paper.*

**NOTE**: Due to its large size (1.5+ GB), the full set of data files (.mat files) must be downloaded from [https://media.polito.it/AIobservers](https://media.polito.it/AIobservers)

## How to run the code

The present instructions are provided with the software in order to explain how to run it. 

Please note that to run the provided software, it is recommended  to have installed MATLAB R2019b or later Versions.

The folder contains: 

- 20 .mat files containing the weights and the architecture of the trained Deep Neural Networks (DNNs) i.e., the JPEGResNet50 and the 19 AIOs. 

- the MATLAB script ```Simulate_AI_subjective_test.m``` that provides the software for simulating a subjective experiment with the AIOs. 

- the MATLAB script ```get_quality_JPEG_images.m``` that provides the software for computing the Visual quality of a JPEG compressed images using the JPEGResNet50.

- a folder called ```Test_folder``` containing few images on which the software can be tested.
  
To run ```Simulate_AI_subjective_test.m``` or ```get_quality_JPEG_images.m```, first prepare a folder containing the Images whose quality should be evaluated, then insert it in the folder that contains the 19 DNNs modeling the AIOs, the JPEGResNet50, ```Simulate_AI_subjective_test.m``` and ```get_quality_JPEG_images.m```. Open the script Simulate_AI_subjective_test.m or get_quality_JPEG_images.m depending on what you want to do, update the variable named ```imgfolder``` by inserting the name of the folder containing the images whose quality should be evaluated, then simply run the script.

In case of ```get_quality_JPEG_images.m```, a csv file named ```JPEGResNet50_MOS.csv``` reporting the estimation of the MOS of each image will be generated and saved in the folder that contains the scripts. 

In case of Simulate_AI_subjective_test.m, 21 csv files are generated and in the folder that contains the scripts: The file ```MOS_AI.csv``` that reports the MOS computed from the AIOs opinion scores; the file ```AI_opinin_scores.csv``` containing the AIOs opinion Scores; and 19 other files, one for each AIOs, reporting the probability of choosing each of the five possible opinion scores i.e., "Bad", "Poor", "Fair", "Good" and "Excellent" for every evaluated image.

Please send an email to lohic.fotiotiotsop@polito.it for any further questions. 

