# LangChain PDF Chat App  
This project allows you to interact with multiple PDF documents using Large Language Models (LLMs) such as OpenAI's GPT and Hugging Face models. It uses LangChain, FAISS, and Streamlit to build a simple chat interface that answers questions based on the contents of uploaded PDFs.  
## Clone the repository  
```bash  
git clone https://github.com/yourusername/langchain-pdf-chat.git  
cd langchain-pdf-chat  
```  
## Create and activate a virtual environment (optional)  
```bash  
python -m venv venv  
source venv/bin/activate  # On Windows: venv\Scripts\activate  
```  
## Install dependencies  
```bash  
pip install -r requirements.txt  
```  
## Create a `.env` file in the root directory and add your API keys  
```env  
OPENAI_API_KEY=your_openai_api_key  
HUGGINGFACEHUB_API_TOKEN=your_huggingface_api_key  
```  
Get your keys from: https://platform.openai.com/account/api-keys and https://huggingface.co/settings/tokens  
## Run the Streamlit app  
```bash  
streamlit run app.py  
```  
Then open the provided URL in your browser (usually http://localhost:8501).  
## How it works  
1. Upload PDF files via the web interface.  
2. The files are read and split into text chunks.  
3. Embeddings are generated using Hugging Face Embeddings.  
4. Chunks are stored in a FAISS vector store.  
5. When a user asks a question, relevant chunks are retrieved using similarity search.  
6. A response is generated using an LLM (OpenAI or Hugging Face) with the context.  
## Project structure  
```  
langchain-pdf-chat/  
├── app.py                 # Main Streamlit app  
├── pdf_reader.py         # Extracts and chunks PDF text  
├── vector_store.py       # FAISS vector store logic  
├── chat_engine.py        # Handles chat interaction with LLM  
├── requirements.txt  
└── .env  
```  
## Technologies used  
- Python 3.10+  
- LangChain  
- FAISS  
- Hugging Face Transformers  
- Streamlit  
- PyPDF2  
## Example use cases  
- Summarizing research papers  
- Legal or policy document Q&A  
- Interactive textbooks  
- AI assistants for documentation  
## Credits  
- Tutorial by Sam Witteveen: https://www.youtube.com/watch?v=dXxQ0LR-3Hg  
- LangChain and Hugging Face contributors  


