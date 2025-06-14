# Question Answering System using Retrieval-Augmented Generation (RAG)

A Retrieval-Augmented Generation (RAG) Question Answering System that semantically retrieves relevant documents from a custom knowledge base and generates context-aware answers to user queries. Built with Python, Sentence Transformers, FAISS, and Gradio, it enables interactive Q&A and supports dynamic document addition for domain adaptability.

---

## Features

- Semantic retrieval from a custom, user-expandable knowledge base
- Context-aware answer generation using extractive techniques
- Interactive Gradio web UI for easy question answering
- Dynamic document addition for domain adaptability
- Ready-to-use in Google Colab with minimal setup

---

## Getting Started

### Environment

- Python 3.8+ (tested on Google Colab)

### Installation

Install dependencies directly in your Colab notebook:
```python
!pip install faiss-cpu sentence-transformers gradio
```

No complex setup required—all dependencies are managed within the notebook.

---

## Usage

### Notebook

1. Open the provided notebook (`Easy_RAG_System_Colab.ipynb` or `QA_RAG.ipynb`) in Google Colab.
2. Add documents to the knowledge base:
    ```python
    rag.add_documents(["Your custom document text here"])
    ```
3. Ask a question:
    ```python
    answer, docs = rag.answer_question("What is explainable AI?")
    print(answer)
    ```

### Web Interface

- Launch the Gradio UI from the notebook:
    ```python
    demo.launch(share=True)
    ```
- **Input:** User question (e.g., "What is a neural network?")
- **Output:** Generated answer and a list of retrieved documents

---

## Model and Tech Stack

- **Sentence Transformers** (`all-MiniLM-L6-v2`) for semantic embeddings
- **FAISS** for vector similarity search
- **Gradio** for the interactive web interface
- **No fine-tuning or external LLMs used**; answers are extracted from retrieved content
- Optionally extensible with frameworks like **LangChain** or **Haystack** for advanced use cases

---

## Dataset

- **Type:** Custom, curated knowledge base (10–39 documents) focused on AI, deep learning, and related topics
- **User Expansion:** Users can add their own documents via the interface
- **No public dataset used**; all data is user-provided or sample educational content

---

## Contribution

Currently, public contributions are not enabled for the notebooks.

- If open-sourcing in the future, please consider adding a `CONTRIBUTING.md` and a code of conduct.

---

## License

*No license specified.*  
If open-sourcing, we recommend an [MIT License](https://opensource.org/licenses/MIT) or [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

## Contact

*Contact information not specified.*  
If you would like to add contact details, please specify your email or preferred method of contact.

---

## FAQ

**Q:** Can I run this outside Google Colab?  
**A:** Yes, but you’ll need to ensure the same Python environment and dependencies.

**Q:** Does it work with large document collections?  
**A:** The current setup is optimized for small to moderate (10–39) documents. For scalability, see the roadmap.

**Q:** Are answers always accurate or generated?  
**A:** Answers are extractive, generated only from the retrieved content, and not hallucinated.

---

## Known Issues

- Answers are strictly extractive; generative LLM integration is not included.
- Limited scalability for large knowledge bases in the current notebook implementation.
- No authentication or access control on the Gradio interface by default.

---

## Roadmap

- Integrate LLM-based generative answering for better flexibility and reasoning
- Improve scalability for larger document repositories
- Add support for advanced retrieval frameworks (LangChain, Haystack)
- Enable production deployment options and API endpoints

---

*For suggestions, feature requests, or to express interest in contributing, please open an issue or contact the maintainer directly once contact info is available.*
