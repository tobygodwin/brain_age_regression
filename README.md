# Age regression from brain MRI

This notebook was produced as part of a team of 3 and formed part of the submission fo the Machine Learning for Imaging course during my MSc in AI.
 The coursework provided data and high level guidance on strategies. However, the substantive methods were implemented independently.

Text in <em>italics</em> are taken from the coursework information.

<em>Predicting the age of patient from a brain MRI scan can have diagnostic value for a number of diseases that may cause structural changes and potential damage to the brain. A discrepancy between the predicted age and the real, chronological age of a patient might indicate the presence of disease. This requires an accurate predictor of brain age which may be learned from a set of healthy reference subjects, given their brain MRI data and their actual age.

The objective for the coursework is to implement different supervised learning approaches for age regression from brain MRI. We provided data from a total of 652 healthy subjects, that is split into different development sets and a held-out test set on which you will evaluate your final prediction accuracy.

Each approach will require a processing pipeline with different components that you will need to implement using methods that were discussed in the lectures and tutorials. There are three dedicated parts in the Jupyter notebook for each approach which contain some detailed instructions and some helper code. </em>

Three appraoches were taken (A,B,C), each approaching the task in different ways - from extracting domain specific features, to training a fully end-to-end model. The results of the three methods are compared. Please note data is not included for ethical reasons.

### A: Extract features using segmentation and apply regression

This technique trained a CNN-based model to segment a brain MRI into 3 tissues. The volumes of each tissue were then manually calculated using the images' metadata, to be used as features  in the regression. 

### B: Perform dimenionality reduction on MRI, and apply regression. 

This technique extracted abstract features from the MRI using PCA. Regression was performed on the low-dimensional features returned by PCA.

### C: Using CNN to predict age directly from MRI

A CNN architecture was trained to predict age directly from the MRI. Feature extraction and regression wis captured in the neural network architecture. The CNN learns highly representative, non-linear features of the MRI scan, from which age can be estimated. 
