# Multiple PDF Query Chatbot &nbsp;🤖

A powerful PDF-based chatbot application built using **Python**, **Streamlit**, **LangChain**, and the **OpenAI API**. This project leverages **Retrieval-Augmented Generation (RAG)** to answer user questions based on the content of uploaded PDF documents. Ideal for anyone looking to interact with PDF documents seamlessly, providing quick, accurate answers.

---

## Key Features

- **Upload Multiple PDFs**: Supports uploading and processing multiple PDF documents simultaneously.
- **Context Retrieval**: Utilizes FAISS (Facebook AI Similarity Search) to store text embeddings for rapid information retrieval.
- **Conversational Memory**: Remembers previous questions within a session, enabling seamless follow-up questions without losing context.
- **Contextual Responses**: For questions unrelated to the PDFs, the chatbot returns no answer, keeping responses scoped to the uploaded documents.

---

## Libraries and Tools Used

- **[Streamlit](https://streamlit.io/)**: For building the web application interface.
- **[LangChain](https://github.com/hwchase17/langchain)**: To process PDF text, convert it to embeddings, and retrieve relevant text snippets.
- **[FAISS](https://github.com/facebookresearch/faiss)**: Vector database for efficient similarity search and retrieval of relevant text embeddings.
- **[OpenAI API](https://platform.openai.com/docs/introduction)**: For generating responses based on the retrieved text data.

---

## Demo

### Step 1: Upload PDFs
1. Click on the **Browse files** button to select one or more PDF files.
2. Click **Process** to initiate the document ingestion.

### Step 2: Convert to Embeddings
1. The application processes each PDF file, converting its text into embeddings.
2. These embeddings are then stored in FAISS, a high-speed vector database.

### Step 3: Ask Your Questions
1. Once processing is complete, you can ask questions related to the PDF content.
2. The chatbot provides accurate answers based on the retrieved data.

### Step 4: Conversational Memory
1. The chatbot retains the memory of previous questions, allowing for a conversational flow.
2. You can review answers and return to previous questions, similar to a typical chatbot experience.

### Step 5: Contextual Responses
1. For questions outside the scope of the PDFs, the chatbot will return no answer.
2. This ensures focus on document-specific information.

---

## How to Run Locally

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install Requirements**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the App**:
   ```bash
   streamlit run app.py
   ```
   > Replace `app.py` with the name of your main Streamlit app file if it differs.

4. **Access the Chatbot**:
   - Once the server is running, open your browser and go to [http://localhost:8501](http://localhost:8501) (or the address shown in your terminal).

---

## Configuration

1. **OpenAI API Key**  
   Make sure you have an OpenAI API key. You can set it as an environment variable:
   ```bash
   export OPENAI_API_KEY="your_openai_api_key"
   ```
   Or, in your code, assign it directly if you prefer (not recommended for production).

2. **Other Environment Variables**  
   You may have additional environment variables for your local or production setup, such as paths for PDFs or custom model parameters.
