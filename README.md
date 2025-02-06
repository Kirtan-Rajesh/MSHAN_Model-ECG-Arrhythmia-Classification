# Multi-Scale Hybrid Attention Network (MSHAN) for ECG Arrhythmia Classification

MSHAN is a deep learning framework designed for ECG arrhythmia classification. By integrating multi-scale convolutional feature extraction, hierarchical attention mechanisms, and GRU-based temporal modeling, MSHAN achieves state-of-the-art performance with high accuracy, precision, recall, and F1 scores. The model further incorporates SHAP (SHapley Additive exPlanations) for enhanced interpretability, offering both global and local explanations for its predictions, which is crucial for clinical applications.



## Overview

In clinical settings, an accurate and interpretable ECG arrhythmia classification system can reduce processing costs, shorten patient wait times, and lower medical errors. MSHAN is built using TensorFlow/Keras and achieves 98% accuracy on the MIT-BIH Arrhythmia Database (Lead II). It outperforms traditional models such as 1D CNN, LSTM, BiLSTM, GRU, ResNet-1D, and MLP by combining:
- **Multi-scale Convolutional Feature Extraction:** Parallel convolutional blocks with various kernel sizes capture both local and global features.
- **Hierarchical Attention Mechanisms:** Temporal and channel attention refine the extracted features.
- **GRU-Based Temporal Modeling:** GRU layers capture sequential dependencies in the ECG signal.
- **Explainability via SHAP:** Integrated SHAP visualizations provide transparent, interpretable insights that help build clinical trust.

## Features

- **State-of-the-art Performance:** Achieves 98% accuracy in ECG arrhythmia classification.
- **Hybrid Architecture:** Combines multi-scale convolution, attention, and GRU layers.
- **Robust and Stable:** Uses residual connections and layer normalization to prevent vanishing/exploding gradients.
- **Explainable AI:** SHAP visualizations offer both global and local interpretability, making the model's decisions clear to clinicians.
- **Extensible:** Future work includes incorporating advanced residual architectures like ResNet or DenseNet.



This script produces SHAP summary, waterfall, and overlay plots to illustrate the model’s interpretability.

## Dataset

The model is trained and tested using the [MIT-BIH Arrhythmia Database](https://physionet.org/content/mitdb/1.0.0/). ECG signals are sampled at 360 Hz and segmented into individual heartbeats (360 samples per beat: 180 before and 180 after the R-peak).


## Results

The evaluation of MSHAN demonstrates that it outperforms traditional models in ECG arrhythmia classification. Key results include:
- **Accuracy:** 98%
- **Performance Metrics:** High precision, recall, and F1 scores across all arrhythmia classes.
- **Explainability:** SHAP visualizations provide insight into the contribution of individual ECG time points.

Below are the visualizations done in the research:

### Summary Plot
The summary plot highlights the most influential time points in the ECG signals.

### Bar Plot (Feature Importance)
The bar plot displays mean SHAP values for different time points, showing the effect of hierarchical attention.

### Waterfall Plot
The waterfall plot illustrates the cumulative contributions of individual time points to the model’s output.

### SHAP Overlays on ECG
Overlaid SHAP plots on ECG waveforms highlight critical regions such as the QRS complex and T-wave.
Additionally, the confusion matrix below confirms the robust classification performance.

## Conclusion and Future Work

MSHAN delivers state-of-the-art performance, achieving an accuracy of 98\% along with high precision, recall, and F1 scores. The model’s hybrid architecture combines the advantages of multi-scale feature extraction, hierarchical attention, and GRU-based temporal modeling, enabling it to surpass traditional approaches. By integrating SHAP, the model enhances transparency by offering both global and local explanations for its predictions. These visual insights help bridge the gap between advanced AI techniques and clinical practice, fostering trust among healthcare professionals.

In clinical settings, this strategy has the potential to reduce ECG signal processing costs and patient wait times while lowering medical errors. Future work will focus on further enhancing model accuracy and robustness by integrating advanced residual architectures such as ResNet or DenseNet.



Feel free to modify and expand this README to better fit your project details and preferences. Happy coding!
