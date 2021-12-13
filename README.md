
A brain tumor is considered as one of the aggressive diseases, among children and adults. Brain tumors account for 85 to 90 percent of all primary Central Nervous System(CNS) tumors. Every year, around 11,700 people are diagnosed with a brain tumor. The 5-year survival rate for people with a cancerous brain or CNS tumor is approximately 34% for men and 36% for women.
Proper treatment, planning, and accurate diagnostics should be implemented to improve the life expectancy of the patients. The best technique to detect brain tumors is Magnetic Resonance Imaging (MRI). A huge amount of image data is generated through the scans. These images are examined by the radiologist. A manual examination can be error-prone due to the level of complexities involved in brain tumors and their properties.
Application of automated classification techniques using Machine Learning(ML) and Artificial Intelligence(AI) has consistently shown higher accuracy than manual classification. Hence, proposing a system performing detection and classification by using Deep Learning Algorithms using ConvolutionNeural Network (CNN), and TransferLearning (TL) would be helpful to doctors all around the world.

According to the Croatian Institute of Public Health, from 2001 to 2015, 7,041 cases (52% of men) were diagnosed, while 5,797 people (also 52% of men) died of malignant brain tumors in the same period. Between 430 and 510 cases of malignant brain tumors are diagnosed annually in Croatia.


BRAIN TUMOR CLASSIFICATION 

This is my brain tumor classification project, which analyzes individual slices of MRI scans and predicts whether it is a tumor or not. It predicts among 4 classes: 3 classes of tumor (glioma, meningioma and pituitary tumor), and not a tumor class.
Dataset was downloaded from kaggle (https://www.kaggle.com/sartajbhuvaji/brain-tumor-classification-mri). It contains images of brain MRI with axial, coronal and sagittal slices which are located in corresponding class directory. I used only 5 images of each class as a testing data and the rest for training(75%) and validation(25%). Images were cropped before loaded into the model and also data augmentation was performed because of the small dataset. I used transfer learning with EfficientNetB0 as model with pre-trained weights from imagenet. Model accuracy was very good but it can be better with larger dataset and some more hyperparameter tuning.


BRAIN TUMOR SEGMENTATION

Another part of the project is tumor detection. It is actually a semantic segmentation of brain MRI images so my model will predict possible tumor pixels on the black background. Dataset was downloaded from kaggle (https://www.kaggle.com/mohamedchakerouari/brain-tumor-dataset). It contains brain tumor images and corresponding ground truth binary masks. Images were preprocessed and loaded into convolutional neural network designed for segmentation tasks called U-net. Because of the class imbalance problem (tumor is relatively small in contrast to large black background in the ground truth images), Jaccard similarity index (IOU) was used as a metric in model training.
