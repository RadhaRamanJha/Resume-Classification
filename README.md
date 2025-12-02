# Resume Classification

# Business Objective  
The goal of this project is to reduce manual human effort in the recruitment process by automatically classifying resumes into predefined categories using Natural Language Processing (NLP) and Machine Learning techniques.

# Project Overview  

* **Data Collection**  
    * All resumes (PDF/DOC) were converted to `.docx` using `pdf2docx` and `doc2docx` libraries.  
    * The text from the `.docx` files was extracted using `textract` library, to bring the data in `pandas` compatible form.  
    * Resumes were categorized based on labels **Internship** , **ReactJS**, **PeopleSoft**, **SQL** and **Workday**.
    * All data was combined into a single DataFrame and labeled using `LabelEncoder`.  
    * Saved as `resume_data.csv` for further processing.

* **Data Cleaning**  
    * Removed whitespace, converted text to lowercase, and performed tokenization to break a stream of text in smaller managable units called **tokens**.  
    * Applied stemming and lemmatization for word conversion in it's root form.  
    * Removed stop words (e.g., “is”, “are”, “we”). 
    * Cleaned data stored separately as `clean_resumes.csv`.

* **Exploratory Data Analysis (EDA)**  
    * **TF-IDF**(Term frequency - Inverse document frequency) analysis was conducted to identify the importance of words in the document.  
    * Word frequency plots and n-gram (bi/tri-gram i.e. words formed taking two and three words at a time respectively) visualizations created for each category.  
    * **Word clouds** charts was generated to highlight key terms by category.
 
* **Feature Engineering**
   * Performed Part-of-Speech tagging. 
* **Model Building**  
Dataset was split: 75% training and 25% testing  
Applied classifiers:  
  * K-Nearest Neighbors (KNN)  
  * Decision Tree  
  * Random Forest  
  * Support Vector Machine (SVM)
  * Naive Bayes

  A strong classifier model was developed by **Bootstrap Aggregation** as well as **Adaptive Boosting**
    The ensemble learning methods used 
    * Bagging Classifier  
    * AdaBoost    

* **Model Evaluation**  
  Metrics considered for determining the accuracy for the test data (data which was not shown to model during it's training):
    *   Precision
    *   Recall
    *   F1-Score  
Bar charts and tables were used to compare model performance.

* **Deployment**
    The best-performing model was deployed using **Streamlit** for an interactive resume classification interface.


* **Files Included**
  * `Clean_resumes.csv`, `resume_data.csv` – Preprocessed datasets
  * `EDA.ipynb` – EDA notebook
  * `Model_Building_Final.ipynb` – Final model training
  * `classification_model.ipynb` – Alternate model trial
  * `VECTOR.pkl`, `ModelDTC.pkl` – Saved vectorizer & model
  * `Resume_app1.py` – Streamlit app for deployment
  * `Project - Resume Classification.pptx` – Presentation
  * `README.md` – Project documentation
* Author  
**Radha Raman Jha**
(https://www.linkedin.com/in/radha-raman-jha-a565a2102)  
**GitHub Repository**(https://github.com/RadhaRamanJha/Resume-Classificaion
