# PoeticMind - Interactive Chinese Poem Generator

## Overview

Chinese poetry, one of the most treasured elements of China's rich cultural heritage, has been an essential part of the nation's literary and artistic tradition for over two millennia. Renowned for its rhythmic precision, deep philosophical reflections, and artistic elegance, poetry has played a crucial role in education, governance, and personal expression. During the Tang and Song dynasties, poetry flourished as a hallmark of intellectual and artistic achievement, with forms like **五言绝句 (Five-Character Quatrains)** and **七言律诗 (Seven-Character Regulated Verses)** embodying the intricate interplay of form, tone, and meaning. These poetic styles continue to inspire contemporary writers and readers, preserving the timeless beauty of Chinese language and culture.

### **A Brief History of Chinese Poetry**
Chinese poetry dates back to the **Shijing (Book of Songs)**, a collection of over 300 poems compiled around the 6th century BCE. This anthology laid the foundation for the poetic tradition that evolved through the centuries, reflecting themes of nature, morality, and human emotion. During the Han dynasty, **fu poetry** emerged as a blend of prose and verse, emphasizing descriptive and narrative elements.

The Tang dynasty (618–907 CE) is often regarded as the **Golden Age of Chinese Poetry**. This era saw the rise of iconic poets like **Li Bai**, **Du Fu**, and **Wang Wei**, whose works captured the intricacies of human experience, the beauty of the natural world, and the political upheavals of their time. The Song dynasty (960–1279 CE) introduced **ci poetry**, a lyrical form set to music, which became a medium for personal expression and emotional depth.

In later centuries, Chinese poetry continued to thrive, adapting to changing cultural and social contexts while maintaining its classical roots. Today, Chinese poetry remains a vibrant art form, celebrated for its ability to bridge tradition and modernity.

### **Key Characteristics of Chinese Poetry**
1. **Structural Precision**: Traditional Chinese poetry follows strict rules of form, including fixed line lengths, tonal patterns, and rhyming schemes.
2. **Imagery and Symbolism**: Poets often use vivid imagery and metaphors to convey emotions and ideas. Nature is a recurring motif, serving as both a subject and a source of inspiration.
3. **Philosophical Depth**: Many poems reflect Confucian, Taoist, or Buddhist principles, offering insights into morality, harmony, and the human condition.
4. **Musicality**: The tonal nature of the Chinese language lends itself to a rhythmic and melodic quality, enhancing the auditory appeal of poetry.

<p align="center">
  <img src="imgs/wiki-poem.png" alt="Image of classical Chinese poetry">
</p>

<p align="center">
  *Image source: [Wikipedia - Chinese Poetry](https://en.wikipedia.org/wiki/Chinese_poetry)*
</p>


### **Forms of Classical Chinese Poetry**
- **五言绝句 (Five-Character Quatrains)**: A compact form with four lines of five characters each, known for its brevity and vivid imagery.
- **七言律诗 (Seven-Character Regulated Verses)**: A more elaborate structure with eight lines of seven characters each, emphasizing tonal balance and rhyming precision.
- **词 (Ci Poetry)**: A lyrical style often set to music, allowing for more flexible line lengths and emotional expression.
- **赋 (Fu Poetry)**: A descriptive and narrative form combining prose and verse, popular during the Han dynasty.

## PoeticMind project

Chinese poetry is more than an art form—it is a profound window into the heart and soul of Chinese culture. For centuries, it has served as a tool for education, a medium for political commentary, and a means of personal expression. The elegance and depth of classical Chinese poetry continue to inspire poets, scholars, and readers worldwide, bridging the past with the present.

The PoeticMind project seeks to preserve this treasured tradition while making it more accessible and engaging for contemporary audiences. By leveraging a fine-tuned transformer model, the project captures the rhythm, structure, and essence of classical Chinese poetry while allowing for real-time generation based on user input. This innovation reduces the reliance on time-intensive human creativity and linguistic expertise, enabling users to explore and create meaningful poetry interactively. Through customizable structures and creative parameters, PoeticMind ensures the legacy of Chinese poetry is preserved and adapted for future generations, fostering a deeper appreciation of its timeless cultural influence.

---

## Approach

- A **pre-trained GPT-2 model** (`uer/gpt2-chinese-cluecorpussmall`) was fine-tuned on a dataset of Chinese poems and text.
- The fine-tuned model generates structured text based on user inputs such as seed text, rows, columns, and temperature.
- A **Gradio interface** was developed for interactive use within a Google Colab notebook, allowing users to experiment with the model's outputs in real time.

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

This section demonstrates the PoeticMind model in action, showcasing its ability to generate structured Chinese poetry. The seed text, along with user-defined parameters such as rows and columns, serves as the foundation for creating meaningful and aesthetically pleasing poems.

### **Demo 1: Generating a Poem with Seed Text "秋日"**
- **Seed Text**: 秋日 (Autumn Day)  
- **Rows**: 4  
- **Columns**: 5  

#### **Output Poem**:
0 [CLS] 秋日中有三，花上枝头月。 此处流光相，犹似天际落。

1 [CLS] 秋日满野寒，高楼垂柳飞。 寒更冷时暖，霜露冷冷日。

2 [CLS] 秋日未复远，山川未止阴。 月如水落花，风露山烟雪。

![alt text](imgs/autumn-demo.png)

#### **Explanation**:
1. **Stanza 1**:
   - The moonlight shimmers on blossoms, creating a harmonious connection between the earthly and celestial realms. The phrase "犹似天际落" likens the radiance to starlight descending from the sky, evoking a peaceful autumn night.

2. **Stanza 2**:
   - A chilly autumn breeze sweeps across fields and high towers. The swaying of willows contrasts motion and stillness, while the interplay of frost and sunlight introduces warmth amidst the cold, symbolizing resilience.

3. **Stanza 3**:
   - As autumn lingers, the natural beauty of mountains and rivers remains undisturbed. The moon resembles water flowing over blossoms, and the wind carries the dewy scent of mountain mist mixed with snow, blending melancholy and awe.

--- 

### **Demo 2: Generating a Poem with Seed Text "春风"**
- **Seed Text**: 春风 (Spring Breeze)  
- **Rows**: 4  
- **Columns**: 5  

#### **Output Poem**:

0 [CLS] 春风十月雨，风吹寒意雨。 新雨一季云，高露已长霜。

1 [CLS] 春风在竹径，月光如海浪。 谁言烟寒月，雨满江头月。

2 [CLS] 春风吹花上，绿花清雨下。 又有三千春，青龙更应长。


![Image of Spring Breeze Poem](imgs/spring-breeze.png)

#### **Explanation**:
1. **Stanza 1**:
   - The spring breeze mingles with rain, bringing a chilly atmosphere that contrasts with the season’s usual warmth. The imagery of “新雨一季云，高露已长霜” suggests the persistence of winter’s traces, setting the stage for renewal.

2. **Stanza 2**:
   - Walking along a bamboo path, the moonlight reflects on waves that resemble the vast ocean. The poet ponders the transient beauty of nature, likening the smoky chill to the poetic essence of the moonlit rain.

3. **Stanza 3**:
   - Spring’s vibrance unfolds as flowers bloom and green hues thrive under gentle rainfall. The mention of "三千春" (three thousand springs) and "青龙" (green dragon) symbolizes longevity and nature’s continuous cycle of growth and renewal.

This demo highlights the model's ability to capture the rejuvenating spirit of spring, blending imagery of nature and the passage of seasons into a harmonious poetic structure.

---

### **Demo 3: Generating a Poem with Seed Text "雨夜"**
- **Seed Text**: 雨夜 (Rainy Night)  
- **Rows**: 4  
- **Columns**: 7  

#### **Output Poem**:

0 [CLS] 雨夜夜深屋底寒，天黑后半夜来不。一日空云不知天，几度风雨不知南。

1 [CLS] 雨夜临江流水平，明月落日天空阔。山河明月江底沉，城里星星星星月。

2 [CLS] 雨夜里看天涯无，明月明月阴照云。白雪在眼群落黄，雪絮依旧在枝头。


![Image of Rainy Night Poem](imgs/rainy-night.png)

#### **Explanation**:
1. **Stanza 1**:
   - The first stanza sets a somber and mysterious mood, describing the coldness of the night as rain falls incessantly. The imagery of "一日空云不知天" (empty clouds obscure the sky) and "几度风雨不知南" (wind and rain blur the direction south) evokes disorientation and contemplation.

2. **Stanza 2**:
   - Transitioning to a riverside scene, the moonlight reflects on the water’s surface. The expansive imagery of “天空阔” (the vast sky) and “山河明月江底沉” (mountains, rivers, and the moon sinking into the riverbed) captures the grandeur of nature and the passage of time.

3. **Stanza 3**:
   - The final stanza brings a sense of quiet reflection. The moonlight peers through the clouds, and snowflakes gently settle on tree branches. The juxtaposition of “雪絮依旧在枝头” (snow remains on the branches) highlights the continuity of nature even amid change.

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

```bash
project-name/
│
├── README.markdown        # Overview and guide for the project
├── presentation.mp4       # Recorded walkthrough of the project
│
├── code/
│   ├── more_datas/
│   │   ├── .DS_Store
│   │   ├── chinese_poems.txt   # Primary dataset of Chinese poems
│   │   ├── learn.ipynb         # Jupyter notebook for training and demo
│   │   ├── save.model.zip.001  # Split model file part 1
│   │   ├── save.model.zip.002  # Split model file part 2
│   │   ├── save.model.zip.003  # Split model file part 3
│   │   └── save.model.zip.004  # Split model file part 4
│
├── imgs/
│   ├── .DS_Store
│   ├── autumn-demo.png    # Example output for "autumn" theme
│   ├── rainy-night.png    # Example output for "rainy night" theme
│   ├── spring-breeze.png  # Example output for "spring breeze" theme
│   └── wiki-poem.png      # "wiki poem"
│
├── .DS_Store              # MacOS system file

```
---
