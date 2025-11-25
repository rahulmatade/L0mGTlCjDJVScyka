# MonReader

## Project Structure

- Installation of required dependencies
- Importing necessary libraries
- Dataset preprocessing with ImageDataGenerator
- Building a CNN model
- Compiling and training the CNN
- Building a Vision transformer model
- Using transfer learning to further fine tune the ViT model on my dataset
- Evaluating performance on the test set

## Data Preprocessing

- Image Loading & Splitting
- Uses ImageDataGenerator.flow_from_directory()
- Automatically constructs:
- Training set
- Validation set
- Test set

### Handles:
- Reading images from directory structure
- Rescaling pixel values
- Converting labels into binary format
- Resizing images to model’s expected input shape
- Normalization
- Pixel values rescaled to a 0–1 range
- Ensures consistent input distribution for CNN training

## Results

### CNN
- CNN performed well on the dataset, achieving the following results on the test set:
- Test Accuracy: 0.9179

- Confusion Matrix:
[[242  48]
 [  1 306]]

- Classification Report:
              precision    recall  f1-score   support

     notflip       1.00      0.83      0.91       290  
        flip       0.86      1.00      0.93       307  

    accuracy                           0.92       597  
   macro avg       0.93      0.92      0.92       597  
weighted avg       0.93      0.92      0.92       597  

### ViT
- ViT performed extremely well on the dataset, achieving the following results on test set:
- Test Accuracy: 0.9966

- Confusion Matrix:
[[288  2]
 [  0 307]]

- Classification Report:
              precision    recall  f1-score   support  

     notflip       1.00      0.99      1.00       290  
        flip       0.99      1.00      1.00       307  

    accuracy                           1.00       597  
   macro avg       1.00      1.00      1.00       597  
weighted avg       1.00      1.00      1.00       597  
