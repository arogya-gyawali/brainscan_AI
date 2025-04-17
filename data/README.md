# 📁 Data Folder – BrainScan AI

This folder contains all metadata and sample visual outputs used for tumor classification and segmentation. These are processed from the original Figshare `.mat` and IXI `.nii` datasets.

---

## 🧠 Metadata Files

### 🔹 `tumor_metadata.csv`
- Metadata for 3064 tumor MRI scans (from `.mat` files).
- Columns:
  - `file`: PNG filename
  - `label`: Tumor class (1 = meningioma, 2 = glioma, 3 = pituitary)
  - `has_mask`: Boolean flag for mask presence
  - `tumorBorder`: Border coordinates (used for overlay)
  - `label_name`: Readable tumor type

### 🔹 `no_tumor_metadata(1).csv`
- Metadata for 1743 healthy scans from the IXI `.nii` dataset.
- Columns:
  - `file`: PNG slice name
  - `label`: Always 0 (no tumor)
  - `source`: Set to `"IXI"`
  - `slice_index`: Z-slice number from 3D volume

### 🔹 `final_merged_metadata.csv`
- Combined tumor + no-tumor metadata.
- Contains 4817 rows with unified structure for modeling.

---

## 🧬 Data Sources

- **Tumor Scans**: [Figshare Brain Tumor Dataset](https://figshare.com/articles/dataset/brain_tumor_dataset/1512427?file=51340418)
- **Healthy Scans**: [IXI T1 Dataset](https://brain-development.org/ixi-dataset/?utm_source=chatgpt.com)

---

## 🖼️ Sample Image Previews

The following folders include small samples of converted and visualized data:

| Folder               | Description                                |
|----------------------|--------------------------------------------|
| `sample_mri/`        | Original grayscale PNGs (tumor scans)      |
| `sample_mask_overlay/` | Tumor masks overlaid in red                |
| `sample_border_overlay/` | Tumor borders drawn in red (from `.mat`) |
| `sample_binary_masks/` | Binary segmentation masks (tumor = white) |
| `healthy_samples/`   | Converted healthy slices from `.nii` files |

---

## 📌 How to Reproduce

All images and metadata were generated using the notebooks in: /notebooks/data_prep/


You can rerun the full pipeline using your own Google Drive or local `.mat` / `.nii` sources.

---

## 🧾 Usage Tips

Use this data to:
- Train tumor classification or segmentation models
- Visualize tumor region boundaries or masks
- Evaluate CNNs or autoencoders using well-aligned ground truth

---


