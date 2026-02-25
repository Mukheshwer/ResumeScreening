# Resume Screening System

This project is a resume screening pipeline built to automate candidate shortlisting and reduce manual review effort. It processes resumes in PDF and DOCX format, extracts useful information, and ranks candidates based on skill and experience relevance.

---

## Background

During my internship, recruiters were manually reviewing a large number of resumes. The process was slow and inconsistent because resumes are unstructured and hiring requirements are often loosely defined. Simple keyword search resulted in too many irrelevant matches.

The goal of this project was to build a system that could:
- Extract structured signals from resumes  
- Perform contextual skill matching  
- Provide transparent and interpretable scoring  

---

## How the System Works

The pipeline follows these steps:

1. **Resume Ingestion** – Accepts resumes in PDF and DOCX formats  
2. **Text Extraction** – Converts documents into raw text  
3. **Preprocessing** – Cleans and normalizes text (lowercasing, noise removal, tokenization)  
4. **Named Entity Recognition** – Uses Stanford NER to extract entities such as organizations and locations  
5. **Section Parsing** – Identifies sections like Skills, Experience, and Education  
6. **Scoring Engine** – Applies rule-based scoring with contextual validation and section weighting  
7. **Ranking Output** – Produces a ranked list of candidates  

---

## NLP Techniques Used

- Text normalization  
- Tokenization  
- Section-aware parsing  
- Stanford Named Entity Recognition (Organization, Location, Person)  
- Context-based skill validation  
- Rule-based scoring  

Stanford NER helps convert unstructured resume text into structured entities, improving validation of real work experience instead of relying only on keyword presence.

---

## Tech Stack

- Python  
- Stanford CoreNLP (NER)  
- PDF/DOCX parsing libraries  
- pandas  

---

## Design Decisions

- Chose rule-based scoring for interpretability  
- Weighted skills differently depending on resume section  
- Reduced false positives using contextual validation  
- Focused on reliability and transparency over model complexity  

---

## Limitations

- NER models are not trained specifically on resume datasets  
- Scoring logic is rule-based and not learned from recruiter feedback  
- No UI implemented (command-line based execution)  

---

## Future Improvements

- Integrate semantic similarity using embeddings  
- Fine-tune NER on resume-specific data  
- Add recruiter feedback loop  
- Build a dashboard for visualization and filtering  

---

## Setup Instructions

Clone the repository:
