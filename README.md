# 🧠 BrainScan AI

**BrainScan AI** is a deep learning-powered system for detecting, localizing, and classifying brain tumors using MRI scans.  
This project is designed from scratch by a solo developer committed to pushing technical, academic, and creative boundaries over the next two years — with the ultimate goal of publishing, and making an impact in medical AI.

---

## 🚀 Ambition

This project aims to go far beyond a basic tumor classifier:

✅ Accurate **tumor detection** (yes/no)  
✅ **Localization** via bounding boxes or segmentation  
✅ **Classification** of tumor type (glioma, meningioma, pituitary, etc.)  
✅ Integration of **explainable AI** (Grad-CAM, Saliency Maps)  
✅ Deployment as a full-stack **web app** (Spring Boot backend + React frontend)  
✅ Scientific **publication** and open-source contribution  
✅ **Nepal-tailored medical dataset exploration** (Phase II)

---

## 🔬 Motivation

Doctors often struggle to pinpoint tumor location or type from MRIs — especially in resource-limited settings. In one real case (personal), the tumor’s vascular connection remained unclear. This project draws from that reality to:

- Build practical, interpretable AI tools  
- Develop software that mimics real-world diagnostic challenges  
- Learn deeply while building something that matters

---

## 📁 Project Structure

brainscan-ai/
├── data/           # MRI datasets (will be added later)
├── notebooks/      # Colab/Jupyter notebooks for model training and testing
├── models/         # Saved model weights and checkpoints
├── utils/          # Utility scripts (e.g., data loaders, visualizations)
├── references/     # Research papers, dataset links, project notes
├── README.md       # Project overview and documentation
└── LICENSE         # Open-source license (MIT)

---

## 🧠 Stack + Tools

| Area                | Tech/Tool Used                       |
|---------------------|--------------------------------------|
| Core ML             | TensorFlow, Keras, OpenCV            |
| Image Processing    | NumPy, PIL, Skimage, CV2             |
| Modeling            | CNN, Transfer Learning, UNet, Grad-CAM |
| Dev & Versioning    | GitHub, Google Colab, Jupyter        |
| Web App (later)     | React (frontend), Spring Boot (backend) |
| Deployment          | Hugging Face Spaces / Streamlit / Docker |
| Research            | arXiv, PubMed, Kaggle, MICCAI papers |

---

## 📊 Metrics We Care About

- Accuracy, Precision, Recall, F1-score  
- AUC-ROC Curve  
- Grad-CAM interpretability  
- Localization IoU (Intersection over Union)

---

## 🔍 Research Goals

- Train using transfer learning (EfficientNet, VGG16, ResNet50)  
- Investigate UNet-based segmentation for tumor shapes  
- Compare performance across MRI modalities (T1, T2, FLAIR)  
- Generate visual explainability using Grad-CAM  
- Write and submit technical paper to arXiv / BMC Med Imaging / MICCAI

---

## 🖼️ Data Preprocessing

The Figshare brain tumor dataset was provided in `.mat` (MATLAB v7.3+) format.

I:
- Extracted 512×512 MRI slices
- Normalized them to 0–255 grayscale
- Converted to `.jpg` format
- Extracted tumor labels and bounding box coordinates
- Saved metadata to `data/metadata.csv`

This preprocessing pipeline is available in the notebook:  
`notebooks/00_convert_mat_to_jpg.ipynb`

Metadata CSVs are located in `/data/`:
- `metadata.csv`
- `no_tumor_metadata.csv`
- Converted JPGs are referenced but not stored in this repo due to size constraints.



## ✍️ Documentation & Reporting

- All notebooks are well-commented and reproducible  
- Weekly updates in `notebooks/dev-log/`  
- Model experiments tracked with parameters and results  
- Final write-up in `references/project-paper.pdf` (in progress)

---
🧩 How BrainScan AI Stands Out

Most brain tumor projects you’ll find online focus on basic classification using small preprocessed datasets. BrainScan AI is built to go far beyond that — both in technical ambition and real-world relevance.

    Larger and more diverse dataset
    Instead of ~250 images, BrainScan AI uses over 4,800+ MRI slices, combining tumor and healthy scans from multiple raw sources.

    Multiclass tumor classification
    Unlike binary models (tumor vs no tumor), we classify glioma, meningioma, pituitary, and healthy brains separately.

    Raw data preprocessing
    We start from .mat and .nii MRI formats, build conversion pipelines, and generate structured image slices with full metadata tracking.

    Tumor localization support
    The dataset includes bounding box coordinates, laying the groundwork for detection and segmentation — not just classification.

    Planned deep learning stack
    We're not stopping at a simple CNN — the project will explore transfer learning, UNet segmentation, and explainable AI tools like Grad-CAM.

    Real-world inspired
    This isn’t a generic academic task. It’s rooted in an actual clinical case where tumor location couldn’t be precisely identified, driving the need for better diagnostic tools.

    End-to-end deployment
    Future versions will be served through a full-stack web app (Spring Boot backend + React frontend) — making the tool accessible beyond notebooks.

    Well-documented and personal
    Every notebook is clearly commented and structured for learning. This project also serves as a personal research journey, meant to be shared, improved, and published.

    BrainScan AI isn’t just another image classifier — it’s a long-term technical, academic, and personal mission.

## 🧑‍💻 Author

**Aarogya Gyawali** – F1 student | Developer | Aspiring bioinformatics researcher  
🗺️ Based in the Bay Area | 🇳🇵 Nepalese  
🎯 Focused on combining tech with social impact and research  

---

## ⚖️ License

This project is licensed under the [MIT License](./LICENSE)

> Anyone can use this for good. Just don’t forget to cite the original repo and don’t sue me if your robot doctor misdiagnoses someone.

---

## ⭐ Star this repo if you want to follow along with a journey that’s personal, technical, and extremely overkill.


