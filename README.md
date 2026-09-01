# NLP-Based Analysis of Student Answers

A Python-based project for analyzing student answers using basic Natural Language Processing (NLP) techniques.

This project analyzes incorrect answers, spelling errors, word segmentation errors, and visualizes the analysis results.

## Objectives

- Identify student answers that do not match the answer key.
- Detect potential spelling errors using Levenshtein Distance.
- Classify spelling errors into different categories.
- Analyze word segmentation errors.
- Visualize the analysis results.

## Methodology

The analysis process consists of:

1. Data Loading
2. Text Normalization
3. Answer Comparison
4. Incorrect Answer Identification
5. Levenshtein Distance Analysis
6. Spelling Error Classification
7. Word Segmentation Analysis
8. Data Visualization

### Text Normalization

Student answers are converted to lowercase to make the comparison between student answers and answer keys more consistent.

### Answer Comparison

Each student answer is compared with the predefined answer key to determine whether the answer matches the expected answer.

### Levenshtein Distance

Levenshtein Distance is used to measure the difference between incorrect student answers and the corresponding correct answers.

A threshold of 2 is used to select answers for further spelling error analysis.

### Spelling Error Classification

The spelling errors are classified into three categories:

- Deletion (Penghilangan Huruf)
- Insertion (Penambahan Huruf)
- Substitution (Penggantian Huruf)

### Word Segmentation Analysis

The project also identifies errors related to word segmentation in student answers.

### Data Visualization

Matplotlib is used to visualize the number of errors identified during the analysis.

## Results

The analysis produced the following results:

| Analysis | Result |
|---|---:|
| Answers that do not match the answer key | 33 |
| Potential spelling errors | 15 |
| Word segmentation errors | 11 |

### Spelling Error Classification

| Error Type | Count |
|---|---:|
| Substitution | 7 |
| Deletion | 6 |
| Insertion | 2 |

## Example

Some spelling error examples identified in the analysis:

| Student Answer | Correct Answer | Levenshtein Distance |
|---|---|---:|
| peki | pukis | 2 |
| angkung | angklung | 1 |
| angklong | angklung | 1 |
| ketas | kertas | 1 |
| doter | dokter | 1 |
| bokter | dokter | 1 |
| narkoda | nahkoda | 1 |

## Technologies

- Python
- Google Colab
- Pandas
- Matplotlib
- python-Levenshtein

## How to Run

1. Open the notebook using Google Colab.
2. Prepare the required student answer dataset in Excel format.
3. Upload the dataset to your own Google Drive.
4. Make sure the dataset path in the notebook matches the location of the Excel file.
5. Run the notebook cells sequentially.

The notebook uses the following path to access the dataset:

```python
df = pd.read_excel('/content/drive/MyDrive/metopen_kelompok_2/jawaban_siswa.xlsx')
