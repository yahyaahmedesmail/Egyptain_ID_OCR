# 🇪🇬 Egyptian National ID OCR

### AI-Powered Egyptian ID Card Recognition & Information Extraction

An AI-powered computer vision project designed to automate the recognition and extraction of information from Egyptian National ID cards using deep learning and Optical Character Recognition (OCR).

The project explores how object detection and image processing can be combined to identify ID card regions and support automated information extraction, reducing the need for manual data entry.

**Developed by Yahya Ahmed Esmail**

[GitHub Repository](https://github.com/yahyaahmedesmail/Egyptain_ID_OCR)

---

##  Table of Contents

- [Project Overview](#-project-overview)
- [Objectives](#-objectives)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Technologies Used](#-technologies-used)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Potential Applications](#-potential-applications)
- [Limitations](#-limitations)
- [Future Improvements](#-future-improvements)
- [Privacy and Security](#-privacy-and-security)
- [Author](#-author)

---

##  Project Overview

Egyptian National ID cards contain important information that may need to be extracted for digital records, administrative workflows, and document processing systems.

Manually entering this information can be time-consuming and susceptible to human error.

This project investigates an automated approach using computer vision and deep learning to detect Egyptian ID cards and recognize relevant information from their images.

The repository includes a Jupyter Notebook for experimentation and three trained model files intended for the ID recognition pipeline.

##  Objectives

- Explore deep learning techniques for Egyptian ID card detection.
- Apply object detection to locate relevant regions in ID card images.
- Investigate automated text and number recognition.
- Reduce repetitive manual data-entry tasks.
- Build a foundation for more comprehensive identity-document processing systems.

##  Key Features

- **AI-Based Object Detection:** Uses trained model weights for ID-related detection tasks.
- **Document Recognition:** Focuses on Egyptian National ID card images.
- **Information Extraction:** Supports experimentation with identifying relevant regions and extracting information.
- **Deep Learning Workflow:** Combines trained models with a notebook-based development environment.
- **Extensible Architecture:** Provides a foundation for future improvements in OCR, validation, and application deployment.

> Note: The exact extraction capabilities and performance depend on the notebook implementation, model configuration, and evaluation data.

##  System Architecture

The intended high-level workflow is:

```text
       Egyptian ID Card Image
                 |
                 v
       Image Preprocessing
                 |
                 v
        ID Card Detection
                 |
                 v
      Region / Object Detection
                 |
                 v
       Relevant Region Cropping
                 |
                 v
        OCR / Text Recognition
                 |
                 v
     Structured Information Output
```

### Pipeline Explanation

1. **Image Input:** Provide an image containing an Egyptian National ID card.
2. **Preprocessing:** Prepare the image for detection and recognition.
3. **ID Card Detection:** Use the appropriate trained model to identify the card.
4. **Object Detection:** Detect relevant objects or regions using the available model weights.
5. **Region Extraction:** Isolate relevant areas for further processing.
6. **Text Recognition:** Apply the OCR approach implemented in the notebook.
7. **Information Output:** Organize recognized information for downstream use.

The diagram represents the intended processing workflow; individual stages should be verified against the current notebook implementation.

##  Technologies Used

| Technology               | Purpose                                     |
| ------------------------ | ------------------------------------------- |
| Python                   | Core programming language                   |
| Jupyter Notebook         | Development and experimentation             |
| Deep Learning            | Model-based recognition                     |
| Computer Vision          | Image analysis and object detection         |
| YOLO-based model weights | Trained detection models                    |
| OCR                      | Text recognition and information extraction |

The precise libraries and versions should be confirmed from the notebook's imports and execution environment.

##  Project Structure

```text
Egyptain_ID_OCR/
│
├── finalismaaa (2).ipynb   # Main development notebook
├── detect_id.pt            # Trained ID-related model
├── detect_id_card.pt       # Trained ID card model
└── detect_odjects.pt       # Additional detection model
```

### Model Files

| File                | Purpose                           |
| ------------------- | --------------------------------- |
| `detect_id_card.pt` | Intended for ID card detection    |
| `detect_id.pt`      | Intended for ID-related detection |
| `detect_odjects.pt` | Additional object detection model |

The precise class labels, architecture, and responsibilities of each model should be verified from the notebook and training configuration.

##  Installation

### Prerequisites

- Python 3.9 or a version compatible with the notebook dependencies.
- Git.
- Jupyter Notebook or JupyterLab.
- The Python packages required by the notebook.
- Sufficient memory and processing resources for the selected models.

### 1. Clone the Repository

```bash
git clone https://github.com/yahyaahmedesmail/Egyptain_ID_OCR.git
cd Egyptain_ID_OCR
```

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**Linux / macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

Install Jupyter Notebook:

```bash
pip install notebook
```

Install the additional libraries required by the notebook after reviewing its imports. For example, if used by the implementation:

```bash
pip install ultralytics opencv-python numpy matplotlib pillow
```

Install the appropriate OCR library separately if the notebook requires one.

> **Important:** These are example dependencies, not a verified dependency list. Use the notebook's actual imports and model requirements to establish a reproducible environment.

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `finalismaaa (2).ipynb` in your browser.

##  Usage

1. Clone the repository and configure the Python environment.
2. Launch Jupyter Notebook.
3. Open `finalismaaa (2).ipynb`.
4. Review the notebook cells and ensure the model file paths are correct.
5. Install any missing dependencies.
6. Provide an appropriate test image when prompted by the implemented workflow.
7. Execute the notebook cells in order.
8. Review the detection visualizations and outputs produced by the implementation.

**Input:** An image containing an Egyptian National ID card.

**Output:** The detection results and any recognized information supported by the notebook implementation.

The exact input format, output schema, and execution steps may vary depending on the notebook's current code.

##  Potential Applications

The techniques explored in this project may be useful as building blocks for:

- Digital document processing.
- Automated data entry.
- Administrative record digitization.
- Document-processing workflows.
- Identity-document information extraction.

These are potential applications, not claims of production readiness or official identity verification.

##  Limitations

- Recognition quality may vary with image resolution, lighting, blur, rotation, and occlusion.
- OCR performance depends on the recognition engine, image preprocessing, and the quality of the trained models.
- Detected information may require additional validation.
- The repository does not establish a verified benchmark for accuracy, inference speed, or generalization across different ID card conditions.
- Detection and text recognition alone do not establish whether an ID card is authentic.

##  Future Improvements

Potential improvements include:

- [ ] Implement a complete, reproducible end-to-end OCR pipeline.
- [ ] Improve image preprocessing and perspective correction.
- [ ] Add robust Arabic text recognition and post-processing.
- [ ] Validate extracted fields against expected formats.
- [ ] Evaluate model performance using precision, recall, and mAP where appropriate.
- [ ] Measure OCR quality using Character Error Rate (CER) and Word Error Rate (WER).
- [ ] Add automated testing and structured JSON output.
- [ ] Build a user-friendly interface with Streamlit or Gradio.
- [ ] Develop a REST API for integration with other applications.
- [ ] Document model training, dependencies, and reproducibility requirements.

##  Privacy and Security

Egyptian National ID cards contain sensitive personal information.

- Use only images you are authorized to process.
- Avoid committing real identity documents or extracted personal information to GitHub.
- Keep test datasets private and securely stored.
- Review logging and output handling to prevent accidental exposure of personal data.
- Apply appropriate access controls and data-retention policies before any real-world deployment.

This project should not be considered an official identity verification or fraud detection system without additional validation and security controls.

##  Author

**Yahya Ahmed Esmail**

Computer Science and Data Science graduate interested in machine learning, computer vision, and applied AI.

- GitHub: [@yahyaahmedesmail](https://github.com/yahyaahmedesmail)
- Project: [Egyptian National ID OCR](https://github.com/yahyaahmedesmail/Egyptain_ID_OCR)

---

##  License

No license has been specified in this README. Before distributing or reusing the project, add an appropriate license file after confirming the licensing terms for your code, datasets, and pretrained model weights.

---

⭐ If you find this project interesting, consider exploring the repository and following its development.
