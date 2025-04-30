# 🧊 Cold Email Generator

An AI-powered tool that helps software service companies generate **personalized cold emails** based on job postings from potential clients. This tool scrapes job descriptions, extracts key information, matches skills with past project portfolios, and crafts compelling emails to pitch software services.

---

## Tech Stack

- **LLM**: [LLaMA 3.1 (llama3-70b-8192)](https://console.groq.com/docs) via **Groq** for ultra-fast inference  
- **Framework**: [LangChain](https://www.langchain.com/) – Web scraping & orchestration  
- **Vector DB**: [ChromaDB](https://www.trychroma.com/) – Stores vectorized skill–portfolio data  
- **Frontend**: [Streamlit](https://streamlit.io/) – For a lightweight interactive UI

---

## Workflow

1. **Input**: User provides a job post URL (e.g., from Nike Careers)
2. **Scraping**: LangChain extracts text from the web page
3. **LLM Extraction**: LLaMA parses the page and outputs structured JSON containing:
   - Role  
   - Experience  
   - Skills  
   - Description  
4. **Vector Search**: ChromaDB is queried with extracted skills to find relevant past project links
5. **Cold Email Generation**: LLaMA 3.1 uses JSON + portfolio links to generate a personalized email
6. **Output**: Streamlit displays the email with options to copy or download


