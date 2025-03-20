# AI-Resume-Screening
Overview
This Streamlit application uses Natural Language Processing (NLP) techniques to rank resumes based on a given job description. The app extracts text from PDF resumes and compares them with the job description using cosine similarity to determine which resumes are the best match for the job.

Features
Extracts text from uploaded PDF resume files.
Allows users to input a job description.
Ranks resumes based on their relevance to the job description using TF-IDF (Term Frequency-Inverse Document Frequency) and cosine similarity.
Displays a ranked list of resumes with a matching score based on their relevance to the job description.
Requirements:
Before running this app, ensure you have the following libraries installed:
1)streamlit
2)PyPDF2
3)pandas
4)scikit-learn
You can install the required libraries using pip:
      pip install streamlit PyPDF2 pandas scikit-learn

How to Run:
1)Clone this repository or download the code files.
2)Open a terminal and navigate to the directory containing the app.py file.
3)Run the following command to start the Streamlit app:
      streamlit run app.py
4)The app will open in your web browser.

How to Use the App:
Enter Job Description: In the "Job Description" section, input the job description for which you want to evaluate resumes.

Upload Resumes: In the "Upload Resumes" section, click on the "Upload PDF files" button to upload multiple PDF files of resumes you wish to rank.

View Results: After uploading the resumes and entering the job description, the app will process the resumes and rank them based on their relevance to the job description. The results will be displayed in a table with the resume filenames and their corresponding match scores. The higher the score, the better the match.

How It Works:
The app uses the following steps:
Text Extraction: It extracts text from each uploaded PDF resume using the PyPDF2 library.
Text Vectorization: The job description and resumes are converted into numerical vectors using TfidfVectorizer from the scikit-learn library. This transformation helps represent the text data in a format suitable for comparison.
Cosine Similarity Calculation: The app calculates the cosine similarity between the job description vector and each resume vector. This gives a score indicating how closely each resume matches the job description.
Ranking: The resumes are ranked based on their cosine similarity scores, with the most relevant resumes appearing at the top.
