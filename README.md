**RAG Experiment: The Fine Line Between Femvertising And Femwashing**

**Overview**

This project explores how a Retrieval-Augmented Generation (RAG) system handles conceptually complex marketing ideas; specifically, the fine line between femvertising and femwashing.

Rather than testing performance on simple factual queries, this experiment focuses on a more challenging question: **Can a RAG-enabled LLM meaningfully interpret and apply nuanced, contested academic concepts in a marketing context?**

**Experimentation**

- Built a RAG pipeline in Google Colab via sentence-transformers/all-mpnet-base-v2 and Google Gemini
- Created a custom academic corpus by integrating five recent academic literature on femvertising and femwashing
- Implemented text preprocessing, chunking and semantic embedding, and similarity-based retrieval
- Ran a mini experiment to test retrieval accuracy, model comprehension (of the corpus), and performance in a creative marketing task (ad copy generation + critique)

**Key Insight**

**1. Retrieval is highly sensitive to wording:**
 Small phrasing changes significantly affected retrieval accuracy and outputs, suggesting RAG systems primarily rely on lexical signals and pattern alignment rather than deep-level conceptual understanding.

**2. "Semantic dead zone" in embedding space:**
 Some queries failed to retrieve content despite clear matches in the corpus, likely due to how embeddings cluster meaning, not actual absence of information.

**3. Knowing ≠ Applying:**
 The model could correctly retrieve theoretical concepts from the corpus and explain them in isolation, but struggled to apply those concepts in a creative/interpretive generation task. Even with RAG, the model reverted to generic “empowerment” messaging that the academic literature explicitly critiques.

**Why this matters**

This experiment highlights a practical limitation of using LLMs in marketing, creative fields, or other relevant spheres. 

Even when grounded in relevant knowledge, models may still produce outputs that contradict or do not fully align with that knowledge, especially in creative or value-laden contexts.

RAG can improve factual grounding, yet does not replace critical judgment; particularly in normatively sensitive areas like brand authenticity, DEI, or feminist/cultural messaging

**Repository Contents**

RAG_Experiment_Data_in_Practice_Project.ipynb --> full pipeline and experiment (implemented in Google Colab Notebook)

**Notes**

- This project was completed as part of a Master's programme at King's College London exploring digital tools, data, and collaborative methods.
- The original academic corpus is not included in the repository contents. 

















