# Chest X-Ray Medical Diagnosis with Deep Learning

A state-of-the-art project harnessing deep learning for accurate chest X-ray analysis. Designed for healthcare professionals, researchers, and data scientists, this solution leverages advanced Convolutional Neural Networks (CNNs) and innovative data handling techniques to offer robust diagnostic support.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technical Details](#technical-details)
- [File Structure](#file-structure)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Data Acquisition](#data-acquisition)
- [Model Performance & Evaluation](#model-performance--evaluation)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgements](#acknowledgements)

---

## Overview

This project implements an automated chest X-ray diagnosis system using deep learning. It processes high-resolution X-ray images, applies rigorous preprocessing and augmentation techniques, and uses a tailored CNN architecture to classify various chest pathologies. The system outputs detailed metrics, ROC curves, and other visualizations to help assess model performance and diagnostic accuracy.

Key SEO Keywords: Chest X-Ray Diagnosis, Deep Learning, Medical Imaging, CNN, AI Healthcare, ROC Curve, Medical Diagnosis System

---

## Features

- **Advanced CNN Architecture:** Custom-designed network for fine-grained feature extraction.
- **Robust Data Handling:** Implements image normalization and augmentation to accommodate variations in medical images.
- **Comprehensive Evaluation:** Generates ROC curves, computes AUC, and provides advanced statistical performance metrics.
- **Scalable & Modular:** Easily integrable in clinical workflows and extendable for future research.
- **Interactive Notebook:** Explore and visualize experiments using the provided Jupyter Notebook.

---

## Technical Details

- **Data Preprocessing:**  
  Detailed pipelines for image resizing, normalization, augmentation, and segmentation ensure robust input data for training and inference.

- **Model Architecture:**  
  The CNN is constructed with multiple convolutional, pooling, and fully connected layers. Key functions include loss computation and performance evaluation, as seen in methods like `get_roc_curve()` in `util.py`.

- **Performance Metrics:**  
  Utilizes metrics such as accuracy, precision, recall, F1-score, and AUC (Area Under ROC Curve). ROC curves are produced using `matplotlib` and `sklearn.metrics` to visually assess classifier performance.

- **Interactive Experiments:**  
  The `X-Ray.ipynb` notebook provides step-by-step demonstrations, experimental setups, and diagnostic warnings generated by TensorFlow and Keras, ensuring reproducibility and transparency.

---

## File Structure

- **readme.md:**  
  Detailed documentation and project overview.

- **util.py:**  
  Contains utility functions including `get_roc_curve(labels, predicted_vals, generator)` which:
  - Computes ROC and AUC for each class.
  - Dynamically generates and displays ROC plots.
  - Handles exceptions for classes with insufficient data.

- **batch_download_zips.py:**  
  Automates the download of the extensive NIH chest X-ray dataset (~40GB).

- **X-Ray.ipynb:**  
  An interactive Jupyter Notebook for model training, evaluation, and visualization.
  - Includes detailed output logs and warnings for deprecated functions.

---

## Installation & Setup

1. **Clone the Repository:**
   ```
   git clone https://github.com/yourusername/Chest-X-Ray-Medical-Diagnosis-with-Deep-Learning.git
   cd Chest-X-Ray-Medical-Diagnosis-with-Deep-Learning
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Environment Configuration:**
   - Create a `.env` file in the root directory.
   - Define environment variables like API keys and dataset paths as needed.

4. **Run the Application:**
   ```bash
   python main.py
   ```

---

## Usage
  
- **Jupyter Notebook:**  
  Open `X-Ray.ipynb` in Jupyter or Colab for interactive exploration, visualization, and custom experiments.

- **Visualization Tools:**  
  Utilize the ROC curve plots and confusion matrix outputs to interpret model reliability in clinical settings.

---

## Data Acquisition

The project utilizes a large dataset of chest X-ray images provided by the NIH:
- **Manual Download:**  
  Access the dataset [here](https://nihcc.app.box.com/v/ChestXray-NIHCC), unzip the contents into `images-small/nih`.
  
- **Automated Download:**  
  Execute `batch_download_zips.py` to download all zip files automatically.  
  *Note:* Ensure at least 40GB of free disk space (downloads default to `C:\Users\(Username)`).

---

## Model Performance & Evaluation

After rigorous training, the system demonstrates:
- **High Diagnostic Accuracy:**  
  Comprehensive evaluations via metrics such as AUC, precision, recall, and F1-score.

- **Visual Assessments:**  
  The ROC curves and confusion matrices illustrate the model's strength in differentiating pathologies and handling imbalanced data.

- **Diagnostic Reports:**  
  Integrated output from both the Jupyter Notebook and standalone scripts provides clear, patient-specific diagnostic insights.

---

## Contributing

We encourage contributions to enhance performance, usability, and research discoveries:
- Fork the repository and create a new branch for your feature or fix.
- Follow our code guidelines and update documentation as necessary.
- Submit a pull request detailing your changes with references to associated issues.
- See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed instructions.

---

## License

Licensed under the MIT License. See the [LICENSE](./LICENSE) file for full license details.

---

## Contact

For any questions, issues, or collaboration inquiries, please contact:
- Maintainer: [maintainer@example.com](mailto:naitik@wayne.edu)

---

## Acknowledgements

- Special thanks to the NIH for the chest X-ray dataset.
- Appreciation to the open-source community for providing robust libraries and frameworks such as TensorFlow, Keras, and scikit-learn.
- Collaboration and insights from clinical experts have been invaluable.
