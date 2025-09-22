# Transfer Learning for Scene Classification

This project applies **transfer learning** to classify natural scene images into six categories:  
🏙️ Buildings | 🌲 Forest | ❄️ Glacier | ⛰️ Mountain | 🌊 Sea | 🚦 Street  

We leverage **pre‑trained deep neural networks** (ResNet50, ResNet100, EfficientNetB0, VGG16) 
as feature extractors and train custom fully connected layers on top.  

---

## Features
- **Data Preprocessing**
  - Zero‑padding / resizing images for consistency  
  - One‑hot encoding of class labels  
  - Train/validation/test split (20% of training used for validation)  

- **Transfer Learning Models**
  - ResNet50  
  - ResNet100  
  - EfficientNetB0  
  - VGG16  
  (All pretrained on ImageNet; final FC layers retrained while freezing earlier layers)  

- **Regularization & Optimization**
  - Image augmentation: crop, zoom, rotate, flip, contrast, translation  
  - Batch normalization + dropout (20%)  
  - ReLU activation + softmax output  
  - Adam optimizer with categorical cross‑entropy loss  
  - Early stopping based on validation error  

- **Evaluation Metrics**
  - Precision, Recall, F1‑Score, AUC  
  - ROC curves per class  
  - Confusion matrices  
  - Training & validation error curves 