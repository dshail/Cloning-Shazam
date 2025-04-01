# **Video Subtitle Search Engine (Cloning Shazam)** 🎬🔍

## **Overview**  
This project builds a **search engine for video subtitles** using **NLP** and **machine learning** to retrieve the most relevant subtitle segments based on **audio input**. It utilizes **semantic search** for better accuracy compared to traditional keyword-based search.

## **Objectives**  
- Develop a subtitle search engine that retrieves results based on audio queries.  
- Compare **keyword-based** and **semantic search** methods.  
- Use **cosine similarity** to rank subtitle relevance.  
- Leverage **AssemblyAI** for audio transcription and **ChromaDB** for storing embeddings.

---

## **Search Methods**  

| **Search Type**        | **Description**                                 | **Pros**                  | **Cons**                          |
|------------------------|-------------------------------------------------|---------------------------|-----------------------------------|
| **Keyword-Based**       | Matches exact keywords in queries and subtitles. | Simple & Fast             | Misses context & meaning.        |
| **Semantic Search**     | Uses embeddings (e.g., BERT) for meaning/context.| More accurate & context-aware | Requires embeddings & storage. |

---

## **Core Logic**  

### **1️⃣ Data Preprocessing**  
- Load and clean subtitle data.  
- Convert subtitles to vectors using:  
  - **TF-IDF/BoW** (Keyword Search)  
  - **BERT/SentenceTransformers** (Semantic Search)  
- Chunk subtitles for better embeddings.

### **2️⃣ Query Processing**  
- Transcribe audio input with **AssemblyAI**.  
- Convert the transcribed text to an embedding.  
- Calculate **cosine similarity** to find top-k relevant subtitle chunks.

---

## **Setup**  

### **1️⃣ Install Dependencies**  
Make sure you have **Python 3.8+** installed, then run:  
```bash
pip install streamlit assemblyai langchain_huggingface langchain_chroma sentence-transformers numpy scipy dotenv

## **🛠️ Setup Instructions**  

### **1️⃣ Install Dependencies**  
Ensure **Python 3.8+** is installed. Then, install the required libraries:  
```bash
pip install streamlit assemblyai langchain_huggingface langchain_chroma sentence-transformers numpy scipy dotenv
```
## **2️⃣ Set Up Environment Variables
### Create a .env file and add your AssemblyAI API key:

```
ASSEMBLYAI_API_KEY=your_api_key_here
```
## 3️⃣ Run the Streamlit App
### Launch the application with:
```
streamlit run app.py
```
📌 Future Improvements
Fine-tune embeddings for better accuracy.
Add YouTube video link support.
Implement real-time speech-to-subtitle matching.
