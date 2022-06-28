+++
# Experience widget.
widget = "experience"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 40  # Order that this section will appear.

title = "Project"
subtitle = ""

# Date format for experience
#   Refer to https://sourcethemes.com/academic/docs/customization/#date-format
date_format = "Jan 2006"

# Experiences.
#   Add/remove as many `[[experience]]` blocks below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin/end multi-line descriptions with 3 quotes `"""`.

[[experience]]
  title = "Postgraduate individual project: The Segmentation of Fetal Cardiovascular Magnetic Resonance Imaging (August 2020)"
  company = "King's College London"
  company_url = "https://www.kcl.ac.uk/"
  location = "London, UK"
  date_start = "2020-06"
  date_end = "2020-09"
  description = """
  The result :
  
  In this report, we proposed two methods for the fetal cardiovascular motion-corrected MRI image segmentation of the fetal heart and vessels. They are 
  * A 3D U-Net with applied to images non-rigidly co-aligned with an anatomical template 
  * A modified Gaussian Mixture Model (GMM) which uses an atlas of fetal cardiac anatomy as prior information.
  
  The reorientation and registration required for pre-processing are the main bottlenecks for both algorithms. According to the P value of T-test in experiment B, we can’t decide which one is better. But both of them showed better results than previous experiments, segmented more vessel volume of fetal heart.

  Experimental process :
  
  In this experiment, we tested whether new U-Net and HighRes-net can successfully segment vessels of fetal heart, and studied the effects of different model structures, optimizers, augmentations, loss functions, low and high resolution on the results.
There are two kinds labels, one is the whole heart label (heart and vessels), the second one is only the vessels labels. The vessels labels are used when we want our model to only focus on vessels.

  1. Trained U-Net and HighRes-net on the whole cardiac segmentation. U-net achieved Dice score 0.897, and HighRes-net is 0.885. But unfortunately, most vessels are not segmented.
  2. We hypothesized, that failure of deep networks to segment small cardiac structures is due to the high anatomical variability and relatively small training set. We have therefore included a pre-processing registration step, to non-rigidly align the images to the reference template.  
  3. Trained U-Net with image registration. The average dice score is 0.925. Compared with the above experimental results, it has only increased by about 2%, but U-Net with image registration has successfully segmented small cardiac vessels. 
  4. According to the T-test result of U-Net and U-Net with registration, P value < 0.01, which means that there is a significant difference in the performance for these two experiments. Image registration did reduce the anatomical variability of vessels, and improved the segmentation results
  5. Applied modified GMM with probabilistic atlas to 10 samples in the validation set, and the average dice score of GMM is 0.935.
  
  Conclusion:
we applied multiple segmentation models to do fetal cardiovascular magnetic resonance imaging segmentation, explored the reasons why models such as U-Net and HighRes-net are not effective in segmenting small vessels in images. We found that data pre-processing steps such as reorientation and image registration improved the image quality. They made the models‘ dice scores higher and more vessels appeared in the output. In conclusion, reorientation and image registration can further improve the results of fetal cardiac segmentation and enable small organs to be segmented.


"""
[[experience]]
  title = "Graduation project: A classifier for autism prediction based on the combination of phenotypic information and the features of brain networks"
  company = "Northeastern University"
  company_url = ""
  location = "Shenyang City"
  date_start = "2019-04-01"
  date_end = "2019-06-10"
  description = """
  The result :
  
  * I have developed a classifier that distinguishes between autistic and normal people by combining multiple feature vectors. On the basis of 9 important edges between brain areas, the vector such as 2 spectral domain features, 14 node efficiency and 9 node degree are merged as the input of the support vector machine, and the output is the classification result, achieving a 70% correct rate. 
  
  * Based on the experiment, I summarized the differences between the brain regions of autistic patients and normal people:   1. The brain areas which node efficiency and node degree are slightly higher than normal people:57, 63, 77(AAL atlas)    2. The brain areas which node efficiency and node degree are slightly lower than normal people:25, 28, 86, 90(AAL atlas)


  Experimental process :
  
  1. Download 871 data from ABIDE website and calculate the correlation coefficient matrix
  
  2. Use a combination of L1-scca + SLR(learn from Japanese paper) and phenotype information for correlation coefficient matrix dimensionality reduction(feature dimension reduction), choose the important edges.
  
  3. Extract the spectral domain features of each correlation coefficient matrix, and select features that have a classification effect
  
  4. Select appropriate node features with classification effect
  
  5. SVM
  
  
  Award:
  
  1. Outstanding Graduation project of School of Biomedical Engineering 
  
  2. Outstanding Graduation project of Northeastern University
  """
[[experience]]
  title = "GCN network"
  company = "Northeastern University"
  company_url = ""
  location = "Shenyang City"
  date_start = "2018-04-01"
  date_end = "2019-03-01"
  description = """
One reason for the low classification accuracy is the great heterogeneity between different collection sites, in order to solve this problem, We set up a study group, read some papers, and found that one solution is to use GCN and phenotype information. So we studied a gcn model and used phenotype information to improve the classification accuracy.
  
  
  The result :
  
The paper ' Disease prediction using graph convolutional networks: Application to Autism Spectrum Disorder and Alzheimer’s disease ' gave us a lot of inspiration. In this paper, it builds a gcn model, and the chebyshev polynomial is used to process each preprocessed matrix. Then it uses phenotypic information to reduce the distance between each individuals. However, the number of features in this paper is 2000, all of them are selected by ridge regression，I think it might be better to use more specific features. So in my graduation project, I used different method to select only 31 important samples' features.
  
  
  """
  
  
  
  
  
  [[experience]]
  title = "Application of Supervised Deep Learning in Medical Data Analysis"
  company = "Northeastern University"
  company_url = ""
  location = "Shenyang City"
  date_start = "2017-06-01"
  date_end = "2017-08-10"
  description = """
It was my first time to know about deep learning. And in order to complete the project better, I set up a study group to participate in this project. But unfortunately, everyone except me(in my group) went to enjoy the summer holiday gradually, so I had to do the whole project by myself. Because I had a internship at the same time, the project I finished didn't contain much.
  
  
  The result:
  
  I built a cnn and autoencoder model and use them to learn the features of images of pulmonary nodules. They didn't work well, this may be caused by my poor knowledge about pulmonary nodule. And the structure and parameters of the model I chose may be another reason.
  
  """

+++

