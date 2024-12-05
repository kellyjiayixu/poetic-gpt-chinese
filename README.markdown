# PoeticMind - Interactive Chinese Poem Generator

## Overview

Chinese poetry, one of the most treasured elements of China's rich cultural heritage, has been an essential part of the nation's literary and artistic tradition for over two millennia. Renowned for its rhythmic precision, deep philosophical reflections, and artistic elegance, poetry has played a crucial role in education, governance, and personal expression. During the Tang and Song dynasties, poetry flourished as a hallmark of intellectual and artistic achievement, with forms like **五言绝句 (Five-Character Quatrains)** and **七言律诗 (Seven-Character Regulated Verses)** embodying the intricate interplay of form, tone, and meaning. These poetic styles continue to inspire contemporary writers and readers, preserving the timeless beauty of Chinese language and culture.

**PoeticMind** is a project designed to fine-tune a GPT-based language model for generating structured Chinese poems interactively. The primary aim is to explore how large language models can assist in preserving and expanding the creative possibilities of Chinese poetry, blending ancient artistry with modern AI innovation.

---

## Problem Statement

Generating Chinese poetry requires capturing the rhythm, structure, and essence of the language while remaining contextually relevant. Traditionally, this process relies on human creativity and linguistic expertise, which can be both time-intensive and resource-heavy. Our project addresses this by leveraging a fine-tuned transformer model that allows for real-time generation of poems based on user input, with customizable structure and creative parameters.

---

## Approach

- A **pre-trained GPT-2 model** (`uer/gpt2-chinese-cluecorpussmall`) was fine-tuned on a dataset of Chinese poems and text.
- The fine-tuned model generates structured text based on user inputs such as seed text, rows, columns, and temperature.
- A **Gradio interface** was developed for interactive use within a Google Colab notebook, allowing users to experiment with the model's outputs in real time.

---

## Results

The project successfully demonstrates how a transformer model can generate creative and contextually meaningful Chinese poems interactively, with flexible structure and adjustable parameters.

---

## Presentation Materials

An **interactive Gradio demo** is embedded within the provided Google Colab notebook. Users can:
1. Provide seed text for poem generation.
2. Customize parameters such as rows, columns, temperature, and token length.
3. View the generated Chinese poems in a structured format.

### To Access the Demo
1. Open the Google Colab notebook in the repository.
2. Install required dependencies:
   ```bash
   !pip install gradio
    ```
## Demo
Run the cells, and use the Gradio interface directly within the notebook.  
The demo eliminates the need for external apps, making it easy to explore and interact with the model.

---

## Model Card / Dataset Card

### Model

**Base Model**:  
`uer/gpt2-chinese-cluecorpussmall`

**Fine-Tuning**:  
Fine-tuned using PyTorch on a curated Chinese poetry dataset, emphasizing structural and contextual nuances.

---

## Dataset

### Source
The dataset includes a curated collection of publicly available Chinese poetry, encompassing both classical and contemporary works.

### Dataset Characteristics

1. **五言绝句 (Five-Character Quatrains)**:
   - This style consists of **four lines**, each containing **five characters**.  
   - Known for its concise yet vivid imagery, 五言绝句 often reflects themes of nature, emotions, and philosophical musings.  
   - It is one of the oldest and most popular forms of Chinese poetry, exemplified by the works of Tang Dynasty poets like Wang Wei and Li Bai.  

2. **七言律诗 (Seven-Character Regulated Verses)**:
   - This form includes **eight lines**, each with **seven characters**.  
   - It follows strict tonal patterns and rhyming schemes, which are designed to create a rhythmic and harmonious flow.  
   - 七言律诗 is often used for expressing grander themes, including historical events, political commentary, or personal reflections, as seen in the works of poets like Du Fu and Bai Juyi.

3. **Preprocessing**:
   - The poems were pre-processed to ensure structural and semantic integrity:
     - Normalization of punctuation (e.g., standardizing commas, periods).
     - Removal of irrelevant or incomplete lines while preserving the poetic format.

4. **Diversity**:
   - The dataset includes a balanced mix of **classical styles** (Tang and Song dynasties) and **modern interpretations** to ensure a broader coverage of language nuances and contexts.

### Permissions
The dataset usage complies with **open-source licenses**, ensuring it can be used for research and educational purposes.

---

### Why Focus on 五言绝句 and 七言律诗?

The focus on these styles reflects the richness and structured elegance of traditional Chinese poetry. By training the model on these forms, the project aims to:
- Generate poems that respect the syntactical and tonal constraints of Chinese poetic traditions.
- Capture the essence of classical literary aesthetics, making the generated texts culturally authentic and meaningful.

---

## Uses

- **Poetry Generation**:
  - For artistic and educational purposes.
- **Text-Based Creative Applications**:
  - Themed poetry.
  - Personalized compositions.

---

## Critical Analysis

### Impact

The project demonstrates the potential of fine-tuned language models to:
1. Support **creative tasks** in niche linguistic domains, like Chinese poetry.
2. Preserve and adapt **cultural traditions** for a modern audience.
3. Reduce the barrier to entry for experimenting with **creative text generation**.

### Suggestions

- **Reveals**: Fine-tuned language models effectively capture nuances and structures unique to specific datasets.
- **Next Steps**:
  1. Incorporate additional fine-tuning for different poetic styles (e.g., **Tang or Song poetry**).
  2. Extend the model's capability to generate **multi-lingual poems**.
  3. Explore **reinforcement learning** to enhance coherence and creativity.

---

## Resource Links

### Papers with Code
- [GPT-2 Overview](https://paperswithcode.com/method/gpt-2)
- [Low-Rank Adaptation (LoRA)](https://arxiv.org/abs/2106.09685)

### Relevant Models
- [`uer/gpt2-chinese-cluecorpussmall`](https://huggingface.co/uer/gpt2-chinese-cluecorpussmall)

### Blogs
- [Fine-Tuning GPT-2 for Text Generation](https://huggingface.co/blog/fine-tune-gpt2)

### Datasets
- [CLUECorpusSmall](https://github.com/CLUEbenchmark/CLUECorpus2020)

---

## Code Demonstration

The repository includes a **Jupyter Notebook** that demonstrates:
1. **Loading the fine-tuned model.**
2. **Generating structured Chinese poems interactively.**
3. **Saving and reloading the model** for future use.

### Step-by-Step Guidance
1. **Dataset Preprocessing**: Instructions for cleaning and structuring the dataset.
2. **Fine-Tuning**: Code for training the model.
3. **Interactive Text Generation**: Using the **Gradio** interface to generate Chinese poems directly in the notebook.

---

## Repository Structure

- **`README.md`**: This file, providing an overview and guide for the project.
- **`learn.ipynb`**: Jupyter notebook containing the code for training and demonstrating the interactive Gradio interface for generating Chinese poems.
- **`chinese_poems.txt`**: A text file containing a dataset of Chinese poems used for training and fine-tuning the model.
- **`more_datas/`**: Directory containing additional datasets for experimentation or model training.
- **`.git/`**: Git configuration and metadata for version control.
- **`videos/`**: Includes a recorded walkthrough of the project.

---

## Video Recording

A video recording is available in the `videos/` directory. The recording:
1. Provides a **two-minute overview** of the project.
2. Demonstrates the **Gradio interface** embedded in the Colab notebook.
3. Highlights key results and insights.

---
