# Galaxy Morphology Classification with CNN

This project focuses on classifying galaxy morphologies using Convolutional Neural Networks (CNNs) and transfer learning. By leveraging multiple pre-trained models and ensemble methods, we aim to improve the accuracy of classifying galaxies from image datasets like Galaxy DECaLS and SDSS.

## 📁 Project Structure

- `Galaxy_Morphology_Classification.ipynb`: Main Jupyter notebook containing code for data loading, preprocessing, model training, evaluation, and predictions.
- `Galaxy Morphology Classification with CNN.pdf`: Detailed project report including methodology, challenges, and results.

## 📊 Datasets

We used two publicly available galaxy image datasets derived from the Galaxy Zoo project:

- **Galaxy DECaLS**: [DECaLS Dataset](https://astronn.readthedocs.io/en/latest/galaxy10.html)
- **Galaxy SDSS**: [SDSS Dataset](https://astronn.readthedocs.io/en/latest/galaxy10sdss.html)

## 🧪 Methodology

### 🔧 Preprocessing

- Images resized to `128x128x3` to optimize training speed and memory usage.
- Normalized image pixel values.
- Labels converted to categorical format.
- Addressed class imbalance using class weighting.

### 🧠 Models Used

Initial experiments were conducted with:

- EfficientNetB0, EfficientNetB3, EfficientNetB4
- ResNet50
- InceptionV3
- MobileNetV2

The top-performing models (EfficientNet variants) were chosen for further training and ensemble learning.

### 🏗️ Ensemble Architecture

An ensemble classifier was built using the best three models (EfficientNetB0, B3, B4), which significantly improved overall performance.

## 📈 Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

## 🧪 Results

### Individual Model Performance on DECaLS:

| Model            | Accuracy | Loss    |
|------------------|----------|---------|
| EfficientNetB0   | 77.28%   | 0.7621  |
| EfficientNetB3   | 78.41%   | 0.7728  |
| EfficientNetB4   | 81.22%   | 0.8122  |
| ResNet50         | 73.80%   | 0.7380  |

### Ensemble Performance on DECaLS:

- **Accuracy**: 83.2%
- **Precision**: 82.97%
- **Recall**: 83.2%
- **F1-Score**: 82.81%

### Ensemble Performance on SDSS:

- **Accuracy**: 55.28%
- **Precision**: 71.86%
- **Recall**: 55.28%
- **F1-Score**: 53.20%

##  Challenges Faced

- **Hardware limitations**: Limited RAM and GPU time on Google Colab and Kaggle.
- **Class imbalance**: Mitigated using class weights.
- **Generalization**: Mapped class labels across datasets to enable transfer learning.

## 🏁 Conclusion

Our ensemble model achieved a high test accuracy of **83.2%**, outperforming baseline models and showcasing the potential of CNNs with transfer learning in galaxy morphology classification.

## 📚 References

- [Galaxy10 Tutorial on astroNN GitHub](https://github.com/henrysky/astroNN/blob/master/demo_tutorial/galaxy10/Galaxy10_Tutorial.ipynb)
- [Galaxy10 Dataset Documentation](https://astronn.readthedocs.io/en/v1.0.0/galaxy10.html)
- [Galaxy10 SDSS Dataset](https://astronn.readthedocs.io/en/latest/galaxy10sdss.html)

## ✍️ Authors

- **Mohamed Hassan** - [Email](mailto:s-mohamed.eldin@zewailcity.edu.eg)
- **Yusuf Tamer** - [Email](mailto:s-yusuf.sahab@zewailcity.edu.eg)

Project for **DSAI 308 - Deep Learning**, Zewail City of Science and Technology.
