# Deep_Learning_Project
# Chest X-Ray Classification | DenseNet | 92%

![image](https://github.com/user-attachments/assets/1f38728f-25b9-4688-bbc6-fe7563d77638)              ![image](https://github.com/user-attachments/assets/895dfd64-4f13-4d11-b987-ea9ace2e426d)



This project aims to classify pediatric chest X-ray images into two categories: Normal and Pneumonia. The dataset consists of 5,863 images across train, test, and validation sets. Expert physicians from Guangzhou Women and Children’s Medical Center graded the images.

Dataset link :https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia/data
1. Data Loading
The project starts by loading the dataset from Kaggle using the Kaggle API. The dataset is then unzipped, and necessary libraries are imported.
2. Data Augmentation and Balancing
To address the data imbalance issue, augmentation techniques are applied to increase the number of normal X-ray images.
Three different datasets are created with unique augmentations and then concatenated. This balanced dataset is used for training.
3. Model Creation and Training
A DenseNet-161 model, pre-trained on ImageNet, is utilized for transfer learning.
The last fully connected layer is replaced with a new one for binary classification. The model is trained in two stages: first, only the classifier layer is trained, and then all parameters are fine-tuned.
Training is performed with cross-entropy loss, Adam optimizer, and a learning rate scheduler.
4. Test
The trained model is evaluated on the test set, displaying an imbalance similar to the training data. Performance metrics such as accuracy, precision, recall, and F1 score are calculated.
A confusion matrix visualizes the model's performance on the test set.
5. Model Evaluation and Visualization
Selected images from the test set are displayed with their actual and predicted labels. Additionally, the model's confidence in its predictions is visualized through probability distributions for each class.

# Conclusion
The DenseNet-based classifier achieves a high accuracy of 92% on the test set, demonstrating its effectiveness in distinguishing between normal and pneumonia chest X-ray images.
