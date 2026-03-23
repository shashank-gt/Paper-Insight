# PaperInsight

PaperInsight is an AI-based tool that helps you quickly understand research papers without reading everything in detail.

It converts complex research papers into a simple and structured dashboard that shows:

- Core problem  
- Methods and models used  
- Best performance results  
- Limitations and risks  
- When to use or avoid the research  


## Why I Built This

Reading research papers takes a lot of time and effort. Most of the time, we just want to know:

- What is the main contribution?  
- What is the best result?  
- Is the research reliable?  
- Can I use this in my project?  

PaperInsight solves this by automatically extracting useful insights using LLMs and semantic search.

---

## Architecture Overview

PaperInsight follows a modular pipeline:

1. File Loader  
   Supports PDF, DOCX, TXT, and ZIP files  

2. Text Normalization  
   Cleans and prepares raw text  

3. Section Chunking  
   Splits text into sections like Abstract, Methods, Results, etc.  

4. LLM Agents  
   - Section Understanding Agent  
   - Contribution Extraction Agent  
   - Limitation Analysis Agent  
   - Explanation Agent  

5. Performance Metric Cleaner  
   Keeps only the best metrics (Accuracy, AUC, F1)  

6. Vector Store + Retrieval  
   Enables semantic search and Q&A  

7. Web Dashboard (Flask)  
   Interactive UI to view insights  


## Key Features

- Structured summary of research papers  
- Extracts only the best performance metrics  
- Removes duplicate or unnecessary results  
- Performance visualization (Accuracy / AUC / F1)  
- Risk and limitation analysis  
- Beginner-friendly explanations  
- Q&A support using embeddings  


## Tech Stack

- Python  
- Flask  
- Sentence Transformers  
- FAISS (Vector Search)  
- OpenAI / LLM integration  
- Chart.js  


## Project Structure

agents/    → LLM reasoning modules  
core/      → chunking, embeddings, vector store  
loaders/   → PDF / DOCX / TXT parsers  
web/       → Flask app and templates  


## How to Run Locally

1. Clone the repository:

git clone https://github.com/shashank-gt/Paper-Insight.git  
cd Paper-Insight  

2. Create a virtual environment:

python -m venv venv  
venv\Scripts\activate  

3. Install dependencies:

pip install -r requirements.txt  

4. Run the app:

python -m web.app  

5. Open in browser:

http://127.0.0.1:5000  

---

## Author

Built by Shashank H K  
Engineering Student
