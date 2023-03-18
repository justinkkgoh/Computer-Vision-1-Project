# ELEN644_Project: New Deep Multi-Modal Network for Book Genre Classification Based on Cover Images using Transformers

## Folder and file Organization 
We have organized our folders based on the approaches we were applying for genre classification image-based, text-based and multimodal. Instructions to run the code for each approach is contained with each folder's README file. Access to view the folders can be obtained in section 6 of the accompanying report or requested by sending an email to justinkkgoh@gmail.com.  




## Problem Statement: 
Most real-world interactions are usually multi-modal or multi-sensory, but historically, machine learning models are usually single-modal. Previous work in multi-modal book genre classification by book cover have shown promising results. However, with a 56.1\% top-1 accuracy for 30 classes, even the state-of-the-art models of yesteryear have plenty of room for improvement. Previous work in this area have employed limited methods and have not explored solutions using newer deep learning models. Limited work has also been done in determining the effects of applying pre-processing techniques for genre classification. For these reasons, this paper can serve as an additional data point to the community with respect to the larger question of deep learning architectures beyond CNNs for classification and the role of transformers in machine learning in general.

## Introduction
The common saying goes “Don’t judge a book by its cover”. However, when it comes to genre classification, convolutional neural networks (CNN) have made significant progress in the last several years doing just that \cite{judge}. This is not particularly surprising; CNNs have been deployed for various image-related tasks, including classification, tracking, detection, facial recognition, and many others.

Most real-world interactions are usually multi-modal or multi-sensory, but historically, machine learning models are usually single-modal. Previous work by Kundu et al. \cite{deep_multi} takes a multi-modal approach to book genre classification, which is where we drew inspiration for our project. The approach taken by Kundu et al. was to use ResNet-50 and a Universal Sentence Encoder for image and text feature extraction respectively. Results from that paper demonstrated that the multi-modal models outperformed image based and text based models alone, and the approach achieved a top-1 accuracy of 56.1\% across 30 classes. In recent years, large language models (LLM) have become better at tasks such as prediction, text classification, translation, and named entity recognition to name a few. In this paper, we present a similar multi-modal approach to Kundu et al., except we use newer state-of-the-art image and language models for our image and text modalities.

For our image-based modality, we implement a Vision Transformer (ViT) proposed by Dosvitsky et al.  and Shifted Window (SWIN) Transformer proposed by Liu et al.  For our text-based modality, we implement a Bidirectional Encoder Representation from Transformers (BERT) and a Robustly Optimized BERT Pretraining Approach (RoBERTa) language model. Lastly, we experiment with some image pre-processing techniques to determine if there is any impact on our models performance, particularly mean normalization, standardization, and Principal-Component-Analysis (PCA). This is based on work by Pal et al.

Since our investigation revolves around assessing the potential superiority of ViT, SWIN, BERT, RoBERTa, and image-preprocessing over ResNet-50 and Universal Sentence Encoder, we'll be using the baseline of Kundu et al. of 56.1\% top-1 accuracy on the BookCover30 dataset for training and validation. This dataset provided by Iwana et al.  consists of of 57,000 labeled book cover images split equally across 30 classes.





