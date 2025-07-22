# PDF Content Analysis and Question Generation 

This project is a step-by-step pipeline to extract text from PDF files and generate comprehension questions using NLP models.

## Features

- Extracts text and images from PDF documents
- Processes and cleans extracted content
- Uses transformer models to generate question-answer pairs
- Visual outputs and easy debugging
- Modular code for better readability and extension

## Installation

Install all required libraries using:

```
pip install pdfplumber pymupdf pillow transformers pytesseract
```

Ensure `Tesseract-OCR` is installed and added to your system path.

## How It Works

1. **PDF Text Extraction**  
   Uses `pdfplumber` and `PyMuPDF (fitz)` to extract and preprocess text/images from PDFs.

2. **OCR for Image-based PDFs**  
   Uses `Pillow` and `pytesseract` for OCR in image-based documents.

3. **Text Preprocessing**  
   Cleans and prepares text using regular expressions and string manipulation.

4. **Question Generation**  
   Uses HuggingFace `transformers` (e.g., T5) to generate questions from extracted passages.

5. **Output**  
   Saves question-answer pairs into structured files or prints them step-wise.

## Example 

```
pdf_content = extract_pdf_content("sample.pdf")
questions = generate_questions_from_pdf_content(pdf_content)
```

## Directory Structure

- `output/` – Stores generated question-answer pairs
- `images/` – Optional: stores extracted PDF images

## Requirements

- Python 3.7+
- `pdfplumber`, `PyMuPDF`, `pillow`, `transformers`, `pytesseract`
- Tesseract OCR Engine (external dependency)

## Model

Uses a pre-trained `t5-small` or similar transformer model for question generation.


