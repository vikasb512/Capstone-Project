The Project is split into three notebooks:

1. EDA Notebook
2. Convert DCIM to Jpg
3. Capstone Project CNN Modeling

The CNN modeling notebook utulizes the first two notebooks for the modeling process. 

## Project Goals:
To use the given sets of chest x-rays and train a neural network to help identify whether the model can predict pneumonia in a particular patient. This project is part of the much larger Covid-19 Detection Kaggle Competition, but the scope of this project is the binary classification of the presence of pneumonia in a patient.  

## Data
The Data used in the project is from the Kaggle competition. The Original image Dataset is around 110GB in size, and hence the approach in this project has been to convert the images into a format that is much smaller in size and hence accessible. Initial EDA was done on Kaggle. 

Link to the Kaggle Competition: https://www.kaggle.com/c/siim-covid19-detection
Link to Original Repo in Kaggle: https://www.kaggle.com/vikasb512/capstone-project-eda-notebook

Dataset information

The train dataset comprises 6,334 chest scans in DICOM format, which were de-identified to protect patient privacy. All images were labeled by a panel of experienced radiologists for the presence of opacities as well as overall appearance.

Note that all images are stored in paths with the form study/series/image. The study ID here relates directly to the study-level predictions, and the image ID is the ID used for image-level predictions.

The hidden test dataset is of roughly the same scale as the training dataset.

Files

train_study_level.csv - the train study-level metadata, with one row for each study, including correct labels.
train_image_level.csv - the train image-level metadata, with one row for each image, including both correct labels and any bounding boxes in a dictionary format. Some images in both test and train have multiple bounding boxes.
sample_submission.csv - a sample submission file containing all image- and study-level IDs.
Columns

train_study_level.csv

id - unique study identifier
Negative for Pneumonia - 1 if the study is negative for pneumonia, 0 otherwise
Typical Appearance - 1 if the study has this appearance, 0 otherwise
Indeterminate Appearance  - 1 if the study has this appearance, 0 otherwise
Atypical Appearance  - 1 if the study has this appearance, 0 otherwise
train_image_level.csv

id - unique image identifier
boxes - bounding boxes in easily-readable dictionary format
label - the correct prediction label for the provided bounding boxes


## Next Steps:
The project will be built upon, to include multi-class classification and also perform localization on the chest x-rays.
