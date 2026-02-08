# Medicinal Leaf CBIR using Autoencoder

Autoencoder-based **Content-Based Image Retrieval (CBIR)** system for medicinal leaf images using **latent embeddings** and **cosine similarity**.  
This project trains a **Convolutional Autoencoder** to learn a compact representation of images and retrieves **Top-K similar leaf images** for a given query.

---

## Project Highlights
- ✅ Convolutional Autoencoder for **unsupervised representation learning**
- ✅ **256-D latent embeddings** extracted from the encoder
- ✅ Similarity search using **Cosine Similarity**
- ✅ Evaluation with reconstruction metrics: **MSE, PSNR, SSIM**
- ✅ Retrieval demo: Query image → Top-K similar images

---

## Dataset
- Folder-based medicinal leaf dataset (15 classes/folders)
- Total images: **6096**
- Image size used: **128×128×3** (normalized to [0,1])

> Note: Dataset images are not included in this repository.

---

## Model & Method
**Pipeline:**
1. Load and preprocess images (resize + normalize)
2. Train Convolutional Autoencoder using **MSE loss**
3. Extract embeddings from encoder (latent space)
4. Perform CBIR with cosine similarity
5. Display Top-K retrieved images

---

## Results (Validation)
- **MSE:** 0.00344  
- **PSNR:** 25.17  
- **SSIM:** 0.815  

(Include screenshots in `assets/screenshots/` for reconstructions and retrieval results.)

---

## How to Run (Colab)
1. Open the notebook: `Medicinal_Leaf_Dataset.ipynb`
2. Mount Google Drive and set `DATASET_PATH`
3. Run cells in order:
   - training + checkpoint saving
   - reconstructions + metrics
   - embeddings saving
   - retrieval demo (Top-K)

Outputs are saved to:
`/content/drive/MyDrive/leaf_cbir_outputs/`

---

## Repository Structure



---

## Future Work
- Build a local **Streamlit UI** for image upload and retrieval
- Improve retrieval using metric learning (contrastive / triplet loss)
- Add deployment (Docker / Hugging Face Spaces)

---

## Author
**Muhammad Ramzan** (MPhil AI, PUCIT – University of the Punjab Lahore)

