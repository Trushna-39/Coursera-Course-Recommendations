# Course Recommendation System

This project demonstrates a **Content-Based Filtering** approach to recommend courses based on their descriptions, skills, and other features. The system is implemented using **Python** and leverages **cosine similarity** to calculate the similarity between courses.

---

## Project Overview

The goal of this project is to build a recommendation system that suggests courses based on their content. By combining keywords from course names, descriptions, and skills, we create a feature-rich dataset to generate personalized course recommendations.

---

## Dataset

The dataset contains the following columns:
- **Course Name**: Title of the course.
- **Course Description**: Detailed information about the course.
- **Skills**: Keywords associated with the course.
- **Difficulty Level**: Difficulty level of the course (e.g., Beginner, Intermediate, Advanced).
- **Other Columns**: Additional information used for preprocessing and analysis.

---

## Preprocessing

To prepare the dataset for recommendations:
1. **Combined Features**:
   - Merged `Course Name`, `Course Description`, and `Skills` into a single column.
   - This column serves as the input for content-based filtering.

2. **Text Cleaning**:
   - Converted all text to lowercase.
   - Removed:
     - Stopwords (e.g., "and", "or", "the").
     - Special characters and punctuation.
     - Numeric keywords (e.g., "101").
   - Performed tokenization and stemming to standardize the text.

3. **Encoding**:
   - One-hot encoding was applied to categorical variables like `Difficulty Level`.

4. **Vectorization**:
   - Used **TF-IDF (Term Frequency-Inverse Document Frequency)** to transform the combined features into numerical vectors for similarity calculations.

---

## Exploratory Data Analysis (EDA)

- Analyzed the distribution of keywords and their frequencies.
- Visualized the most common skills using word clouds and bar charts.
- Examined the sparsity of the dataset to understand its structure.

---

## Recommendation Engine

- **Similarity Metric**: 
  - Computed **cosine similarity** between course vectors to measure how similar courses are.

- **Recommendation Function**:
  - Input: A course name or description.
  - Output: A ranked list of similar courses.
  - If the input course is not in the dataset, the system calculates similarity using the keywords from the input and the combined features of all courses.

---

## Results

- Recommended courses are displayed along with their original names for better understanding.
- The system efficiently finds similar courses based on content, improving discoverability for learners.

---
