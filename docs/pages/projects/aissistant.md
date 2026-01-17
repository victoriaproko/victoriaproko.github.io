---
layout: project-page
title: "Alssistant"
short_description: "AI-Powered Language Study Assistant Tool."
role: "Lead Developer"
tools: "Python, Streamlit, Hugging Face, PyPDF2"
timeline: "2024"
image: /assets/aissistant.png
permalink: /projects/alssistant/
---

<!-- **[GitHub Repository](https://github.com/your-username/alssistant)** -->

## Overview
Alssistant was developed to bridge the gap between passive reading and active learning. For students and researchers handling high volumes of technical literature, the bottleneck is often the manual labor required to summarize content and create study materials. 

This tool automates that pipeline, extracting core concepts from complex documents and instantly generating study-ready assets.

---

## Technical Implementation

### The NLP Engine
The core of the application utilizes **Hugging Face** transformers to perform abstractive summarization. Unlike simple keyword extraction, the model understands context to provide a coherent overview of the source material.

### PDF Processing Pipeline
* **Extraction:** Using **PyPDF2**, the system parses text from documents up to 50+ pages.
* **Optimization:** Optimized the processing pipeline to achieve high speed, delivering summaries at a rate of less than 10 seconds per page.
* **Interface:** Built a responsive web interface using **Streamlit**, allowing for seamless document uploads and real-time summary generation via Streamlit Cloud.

---

## Key Features

1.  **Automated Flashcard Generation:** The system auto-generates 5-10 high-quality flashcards per document, focusing on key terminology and definitions.
2.  **Effortless Summarization:** Transforms dense academic text into digestible bullet points without losing critical nuance.
3.  **Anki Integration (Upcoming):** Currently developing functionality to export generated flashcards directly to Anki format (.apkg), aiming to reduce manual note-taking time by 60-70%.

---

## Impact & Strategy
The primary product goal was to minimize "busy work" in the learning process. By automating the transition from a PDF to a flashcard deck, users can spend more time on actual retention and less on administrative organization. 

Future iterations will focus on expanding support for multi-lingual documents and improving the accuracy of flashcard questions through fine-tuned LLM prompting.
