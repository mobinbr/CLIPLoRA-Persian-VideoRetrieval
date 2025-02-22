# video-retrieval-CLIP

This project improves Persian video search by fine-tuning the CLIP model with LoRA, making text-to-video search smooth and effective. Using multimodal learning, it connects Persian text queries with instructional video content for better retrieval.

## Key Features

### 1. **YouCook2 Dataset Processing**

- Loads and structures the YouCook2 dataset for processing.
- Extracts video segments and their associated textual descriptions.
- Translates English descriptions into Persian using **GoogleTranslator**.
- Applies basic text preprocessing, including Persian stopword removal.

### 2. **Cross-Lingual Embedding Similarity**

- Uses **Sentence Transformers** to generate sentence embeddings for English and Persian translations.
- Computes cosine similarity scores to assess translation quality.
- Provides statistical analysis of translation fidelity.

### 3. **Video Processing & Frame Extraction**

- Downloads YouTube videos using **yt-dlp**.
- Extracts frames from relevant video segments with **OpenCV**.
- Organizes frames into structured directories for downstream processing.

### 4. **Multimodal Model Fine-Tuning (LoRA)**

- Implements **CLIP**-based Vision-Text embedding model.
- Applies **LoRA** (Low-Rank Adaptation) for efficient fine-tuning.
- Uses Persian CLIP models for domain-specific adaptation.
- Optimizes using **AdamW** and **cosine similarity loss** for better text-image alignment.

### 5. **Efficient Image-Text Retrieval**

- Stores fine-tuned embeddings for retrieval tasks.
- Enables **query-based video retrieval** using Persian text input.
- Retrieves the most relevant video segments based on text queries.

## Key Points

- **Cross-Modal Understanding** – Aligns video frames with corresponding Persian textual descriptions.
- **Users Can Add New Videos** – The system allows users to upload new videos and perform retrieval using the fine-tuned model.
- **Scalability** – Handles large-scale video datasets with batch processing and checkpointing.
- **High-Quality Translations** – Incorporates multilingual sentence embeddings to validate translations.
- **Robust Frame Extraction** – Uses adaptive frame sampling to optimize storage and computational efficiency.
- **Fine-Tuning CLIP Using LoRA** – Optimizes CLIP-based models with LoRA for efficient and accurate image-text retrieval.