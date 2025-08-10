---

## 🚀 Practical Application: PDF Image Classification

To demonstrate the real-world utility of the trained classifier, I developed a complete pipeline that takes a **PDF file** as input, automatically extracts all relevant images, and uses the model to identify which of them are medical.

<img width="540" height="642" alt="image" src="https://github.com/user-attachments/assets/1ed770ac-17d9-478c-9b5a-f2526a8d42ff" />



*This screenshot shows the script successfully processing a medical case study in PDF format. It correctly identifies the chest X-ray as a medical image with 95.2% confidence, while ignoring other non-relevant images.*

### Key Features of the Application Script:

* **PDF Image Extraction:** The script uses the `PyMuPDF` library to parse PDF documents and extract embedded images. It includes intelligent filtering to ignore small images (e.g., icons, logos) that are unlikely to be of interest.
* **Deployment-Ready Inference:** The script is intentionally configured to run inference on the **CPU**. This ensures it is highly portable and can be run on any standard machine, even those without a dedicated GPU.
* **Consistent Preprocessing:** The image preprocessing steps (resizing, color correction, normalization) are identical to those used during training, ensuring maximum model accuracy.
* **Clear Output:** The script provides a clean summary and visually displays each image classified as "medical," along with the model's confidence score.

