# retinal-alzheimers-detection

This project explores the potential of using retinal images to aid in the early detection of Alzheimer’s Disease, using deep learning and transfer learning techniques.

We use:
- **Kaggle OCT dataset** for pretraining a convolutional neural network (CNN)
- **STARE dataset** for fine-tuning and evaluation
- A variety of preprocessing, class collapsing, and evaluation techniques

Workflow overview:
1. **Data Preprocessing**:
   - Resized all images to (256, 256)
   - Normalized pixel values
   - Converted grayscale to RGB when needed
   - Collapsed 51 STARE classes into fewer Alzheimer-related categories

2. **Modeling**:
   - Pretrained on Kaggle OCT dataset using EfficientNetB0
   - Fine-tuned on STARE dataset
   - Used transfer learning and class weighting to improve generalization

3. **Evaluation**:
   - Accuracy and loss plots
   - Confusion matrix and classification report
   - ROC curves

Data:
- **Kaggle OCT dataset for pre-training:** https://www.kaggle.com/datasets/paultimothymooney/kermany2018 
- **STARE dataset for fine-tuning:** https://cecas.clemson.edu/~ahoover/stare/ 

Due to GitHub’s 100MB upload limit, the data is not included here.

To use the data:

1. Download the datasets from the links above

2. Unzip and place them in a directory like data/

3. Update paths in the notebook or script accordingly

Results:
Our model showed limited predictive accuracy on STARE due to label complexity and small sample size, but the workflow demonstrates a proof of concept. We hope future work combining this with EEG data will improve performance.

Note: The commented-out code blocks at the end can be ignored. Only the first two models that appear (pre-trained and refined models) are relevant. 

Made by:
The PRISM team
