
# Retinal Vessel Segmentation using MONAI 🧠💉

This project focuses on **retinal blood vessel segmentation** using the **DRIVE dataset** and the **MONAI framework**.  
It demonstrates how medical image preprocessing, augmentation, and dataset handling can be automated and visualized efficiently — an essential step toward building robust AI-based diagnostic systems.

---

## 🧩 Project Overview

Retinal vessel segmentation is a critical step in **automated diagnosis of diabetic retinopathy and other eye-related diseases**.  
This notebook performs the following:
- Downloads and prepares the **DRIVE dataset** directly from Kaggle.
- Preprocesses retinal images and segmentation masks.
- Applies **data augmentation** using MONAI transforms.
- Visualizes the dataset and verifies augmentation effectiveness.

---

## 🧠 Technologies Used

| Tool / Library | Purpose |
|-----------------|----------|
| **Python** | Primary programming language |
| **MONAI** | Medical imaging framework built on PyTorch |
| **Kaggle API** | Dataset download automation |
| **Matplotlib** | Visualization |
| **NumPy** | Numerical processing |
| **PIL (Pillow)** | Image handling |

---

## 📂 Dataset

**Dataset:** [DRIVE: Digital Retinal Images for Vessel Extraction](https://www.kaggle.com/datasets/andrewmvd/drive-digital-retinal-images-for-vessel-extraction)  
- The dataset contains high-resolution retinal images with manually annotated vessel masks.
- Structure after extraction:
```

drive_data/
└── DRIVE/
├── training/
│   ├── images/
│   ├── 1st_manual/
└── test/
├── images/
├── 1st_manual/

````

---

## ⚙️ Steps Involved

### 1. Install Required Libraries
```bash
!pip install monai kaggle matplotlib
````

### 2. Download the Dataset

Upload your Kaggle API key (`kaggle.json`) and execute:

```python
from google.colab import files
files.upload()
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
!kaggle datasets download -d andrewmvd/drive-digital-retinal-images-for-vessel-extraction
!unzip -q drive-digital-retinal-images-for-vessel-extraction.zip -d drive_data
```

### 3. Set Up Paths and Verify Data

The notebook verifies the image and mask counts and samples to ensure dataset integrity.

### 4. Apply MONAI Transforms

Augmentation includes:

* Image resizing to `(512, 512)`
* Random flipping
* Random rotation
* Zooming
* Gaussian noise addition
* Contrast adjustment

### 5. Visualize the Output

Sample images and masks are visualized to confirm preprocessing and augmentation steps.

---

## 💡 Key Features

* Fully automated **dataset download and preparation**.
* Reproducible and modular pipeline using **MONAI’s Compose transforms**.
* Supports **Google Colab GPU acceleration**.
* Easily extendable for **deep learning model training** (e.g., U-Net).

---

## 🚀 Future Scope

* Integrate U-Net / Attention U-Net for vessel segmentation.
* Evaluate performance using Dice Score and IoU metrics.
* Add model saving and inference scripts.

---

## 🧑‍💻 How to Run

1. Open the notebook in **Google Colab**.
2. Upload your **Kaggle API key (kaggle.json)**.
3. Run all cells sequentially.
4. Observe dataset preparation, transformation, and visual results.

---


## 🙌 Acknowledgments

* **Kaggle** for hosting the DRIVE dataset.
* **MONAI** for providing robust medical imaging tools.
* **Google Colab** for free GPU access.

---

### 👩‍💻 Author

**Shreya R. Chittaragi**
AI Intern | Data Science Enthusiast | Deep Learning Learner
🔗 [LinkedIn](https://www.linkedin.com/in/shreya-r-chittaragi-b1b28b353/) • [GitHub](https://github.com/ShreyaRChittaragi)

```

