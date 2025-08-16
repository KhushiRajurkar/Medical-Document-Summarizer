# Medical Document Summarizer

This project is designed to automatically extract and summarize key information from clinical trial documents (e.g., PDF files of research articles) using state-of-the-art NLP models. The pipeline leverages the BigBird-Pegasus model for long-form summarization and includes content filtering, text cleaning, and post-processing to produce concise bullet-point and paragraph summaries.

## Features

*Note*: User has to upload medical document into the file directory before running the model.

- **PDF Extraction:** Reads and filters PDF files to capture only pages with core content (e.g., Abstract, Methods, Results, Conclusions). 
- **Text Cleaning:** Removes noisy metadata, citations, and excess whitespace.
- **Core Section Extraction:** Attempts to identify and extract important sections using regex; falls back to header removal when sections are not detected.
- **Chunking & Summarization:** Splits the text into manageable chunks and uses the BigBird-Pegasus summarization model for each chunk.
- **Post-Processing:** Formats the final summary into bullet points and neatly wraps it into a paragraph.
- **Modular and Extensible:** Each step is modular, making it easy to adjust, extend, or integrate with other systems.

## Requirements

- Python 3.7+
- [spaCy](https://spacy.io/) with the `en_core_web_sm` model
- [NLTK](https://www.nltk.org/) (with the `punkt` tokenizer)
- [Transformers](https://huggingface.co/transformers/)
- [PyMuPDF](https://pymupdf.readthedocs.io/en/latest/)
- [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/Medical_Doc_Summarization.git
   cd Medical_Doc_Summarization
    ```
## Live Demo
https://huggingface.co/spaces/Kaiyeee/Medical_Document_Summarizer
