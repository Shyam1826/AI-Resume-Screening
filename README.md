# AI Resume Screening & Candidate Ranking System

This project provides an AI-powered resume screening and ranking system that uses the job description and candidate resumes in PDF format to rank applicants based on their relevance to the job. The system leverages Natural Language Processing (NLP) techniques, specifically the TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer, and cosine similarity to assess the match between job descriptions and resumes.

## Features

- **Job Description Input**: Allows users to input a job description text.
- **Resume Upload**: Upload resumes in PDF format for screening.
- **Ranking System**: Ranks resumes based on the relevance to the job description using cosine similarity.

## Requirements

To run the application, you will need the following Python libraries:

- `streamlit` - For building the web interface.
- `PyPDF2` - For extracting text from PDF files.
- `pandas` - For handling data and displaying results.
- `sklearn` - For performing text vectorization and similarity calculation.

You can install the required dependencies by running the following command:

```bash
pip install streamlit PyPDF2 pandas scikit-learn
```
## How to Use
Clone the repository to your local machine:

```bash

git clone https://github.com/yourusername/ai-resume-screening.git
cd ai-resume-screening
```
Install the necessary dependencies:

```bash
pip install -r requirements.txt
```
Run the Streamlit app:

```bash
streamlit run app.py
```
Open the application in your browser, and follow the instructions:

- Enter the job description in the provided text box.
- Upload multiple resumes in PDF format using the file uploader.
- The system will rank the resumes based on their relevance to the job description.
- The results will be displayed in descending order of match.
  
## How It Works

The system processes the following steps:

- **Extract Text from PDF**: The PDF resumes are analyze using the `PyPDF2` library to extract raw text content.
- **Text Vectorization**: The job description and the resumes are combined into a single set of documents. The TF-IDF vectorizer from `sklearn` is used to convert the text data into numerical vectors based on the term frequency and inverse document frequency.
- **Cosine Similarity Calculation**: Cosine similarity is used to compare the job description vector with each resume vector. The results are presented as a similarity score.
- **Ranking**: The resumes are ranked based on their similarity score in descending order (higher scores indicate better matches).

## Example Output

| Resume            | Score   |
|-------------------|---------|
| shyam_resume.pdf      | 0.75    |
| kaushik_resume.pdf      | 0.68    |
| karthik_resume.pdf      | 0.60    |

- Higher score means a better match with the job description.
- Score lies between 0 to 1.

