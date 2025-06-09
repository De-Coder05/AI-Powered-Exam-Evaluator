# Exam Sheets Evaluator

## Overview

The Exam Sheets Evaluator is a Python-based system designed to automate the evaluation of student exam answers. It supports two types of questions:
- One-word answers (1 mark each)
- Short-answer questions (2 marks each)

The system uses natural language processing (NLP) techniques to assess student responses, providing both numeric scores and detailed feedback.

## Features

### Core Functionality
- **Automated Grading**: Evaluates student answers against correct answers using:
  - Cosine similarity for short answers
  - Levenshtein distance for one-word answers
  - Lemmatization for word normalization
- **Question Types**:
  - One-word questions (exact matching with spelling tolerance)
  - Short-answer questions (semantic similarity evaluation)

### User Modes
1. **Professor Mode**:
   - Load/create question banks
   - Set evaluation thresholds
   - View question banks
2. **Student Mode**:
   - Take randomized exams
   - View results with detailed feedback
   - Track performance over time
   - Practice with question bank

### Additional Features
- Performance analytics and progress tracking
- Weak area identification
- Practice mode with immediate feedback
- Exam history storage
- Visualization of performance trends

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/exam-sheets-evaluator.git
   cd exam-sheets-evaluator
   ```

2. Install required dependencies:
   ```bash
   pip install pandas numpy scikit-learn nltk matplotlib
   ```

3. Download NLTK data:
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('stopwords')
   nltk.download('wordnet')
   ```

## Usage

1. Run the system:
   ```bash
   python Exam_Sheets_Evaluator.ipynb
   ```

2. Choose between Professor or Student mode at startup.

### Professor Mode Options:
- Load question bank from CSV
- Create sample question bank
- Adjust evaluation thresholds
- View current question bank

### Student Mode Options:
- Take a new exam (randomized questions)
- View previous results
- Check performance analytics
- Practice with questions
- Review question bank

## File Structure

- `Exam_Sheets_Evaluator.ipynb`: Main Jupyter notebook containing the system
- `exam_results/`: Directory where student results are stored (created automatically)
- Sample question bank CSV files can be created through the professor interface

## Dependencies

- Python 3.9+
- pandas
- numpy
- scikit-learn
- nltk
- matplotlib

## Customization

Professors can:
- Adjust the evaluation threshold (`short_answer_threshold`)
- Modify the scoring scale for short answers
- Create custom question banks in CSV format with columns:
  - Question
  - Type ("one-word" or "short-answer")
  - Correct Answer

## License

This project is open-source and available under the MIT License.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

