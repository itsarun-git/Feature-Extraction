# Wildlife Species Clustering Using CIFAR-10 Dataset

## Overview
This project focuses on clustering wildlife species from the CIFAR-10 dataset using feature extraction and dimensionality reduction techniques. It leverages **ResNet50** for feature extraction and employs both **T-SNE** and **UMAP** for dimensionality reduction. The goal is to group similar images into clusters without prior labels, showcasing how machine learning can identify patterns in wildlife species identification.

## Data Source
- **Dataset**: CIFAR-10  
  The CIFAR-10 dataset consists of 60,000 32x32 color images across 10 different classes:  
  - Frog, Truck, Deer, Automobile, Bird, Horse, Ship, Cat, Dog, and Airplane.
  - Dataset source: [CIFAR-10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)

## Project Workflow
1. **Feature Extraction**:
   - A **ResNet50** model was used for feature extraction. This model is pre-trained on ImageNet and fine-tuned for feature extraction of 32x32 pixel images.
   
2. **Dimensionality Reduction**:
   - **T-SNE**: Applied to visualize the high-dimensional feature space in 2D and 3D. T-SNE is effective for understanding complex relationships but is computationally expensive.
   - **UMAP**: UMAP was utilized as a faster alternative to T-SNE, focusing on preserving both local and global structures of the dataset. It performed well in organizing similar clusters while being significantly faster.
   
3. **Clustering**:
   - Using the extracted features, unsupervised clustering was performed. The objective was to group similar images without knowing their labels, showcasing the power of machine learning in classification tasks.

## Results and Findings
- **T-SNE** was able to create meaningful clusters but was computationally slower. (10,000 images took around 10 minutes).
- **UMAP**, on the other hand, completed the same task faster (about 1 minute for 10,000 images), making it more scalable for larger datasets.
- Both methods, though effective, can be improved by increasing the sample size, using higher-resolution images, and fine-tuning hyperparameters such as perplexity, learning rate, and `n_neighbours`.

## Recommendations
- **Model Improvements**:
  - Use more advanced models like **ResNet101** or **EfficientNet** for improved feature extraction.
  - Hyperparameter tuning for both T-SNE (perplexity, learning rate) and UMAP (`n_neighbours`, `min_dist`).
- **Data Quality**:
  - Larger datasets and higher-resolution images would improve the accuracy of clustering, enabling better identification of subtle features.

## Applications
- This project demonstrates the potential of clustering in wildlife species identification, with broader applications in fields such as:
  - **Healthcare**: Clustering medical images (MRI, X-ray) for disease detection.
  - **Business and Marketing**: Customer segmentation for targeted marketing.
  - **Finance**: Grouping stocks or assets based on market behavior.

## Next Steps
- Fine-tune the feature extraction and clustering models.
- Explore this methodology in larger datasets or other domains like medical imaging or financial analysis.

## Citation
- **Author**: Arun Shamsher Chand  
- **Institution**: Utica University


This README file gives an overview of your project, methods, findings, and potential applications based on the presentation slides you provided.
