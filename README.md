# HireSight: AI-Powered Resume & Job Description Matcher 🚀

HireSight is a web application built with Streamlit that leverages Natural Language Processing (NLP) to analyze and score the similarity between a candidate's resume and a job description. This tool is designed to help recruiters, hiring managers, and job seekers quickly assess the alignment of a resume to a specific role, highlighting matching skills and identifying potential gaps.

## Key Features
- 📄 PDF Resume Parsing: Extracts text directly from uploaded PDF resumes.

- 📊 Match Score Calculation: Utilizes TF-IDF vectorization and Cosine Similarity to generate a quantitative match score between the two documents.

- ⚙️ Categorized Skill Extraction: Identifies and categorizes technical, soft, and domain-specific skills from the text based on a comprehensive internal library.

- ✅ Gap Analysis: Clearly displays which required skills are present in the resume and which are missing.

- 🌐 Interactive UI: A clean and user-friendly web interface built with Streamlit for easy interaction.

## How It Works
The application follows a simple yet effective NLP pipeline:

1. Input: The user uploads a resume (PDF) and pastes a job description into the text areas.

2. Text Extraction & Preprocessing: Text is extracted from the PDF. Both the resume and job description texts are then cleaned by converting them to lowercase, removing stopwords/punctuation, and performing lemmatization using spaCy.

3. Similarity Analysis: The cleaned texts are converted into numerical vectors using TfidfVectorizer. The cosine similarity between these vectors is then calculated to produce the final match score.

4. Skill Analysis: A custom function searches the preprocessed text for keywords from a categorized skill database, identifying skills present in both the resume and the job description.

5. Output: The results, including the match score, matching skills, and missing skills, are presented to the user in an easy-to-read dashboard format.

## Technologies Used
- Language: Python

- Web Framework: Streamlit

- NLP/ML Libraries: spaCy, Scikit-learn

- PDF Processing: PyMuPDF

## How to Run Locally
- Clone the repository:
Bash
git clone https://github.com/your-username/hiresight.git
cd hiresight

- Install dependencies:
Bash
pip install -r requirements.txt

- Download the spaCy model:
Bash
python -m spacy download en_core_web_sm

- Run the Streamlit app:
Bash
streamlit run app.py
