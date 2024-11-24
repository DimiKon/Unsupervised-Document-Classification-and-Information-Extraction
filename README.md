
# Document Classification and Information Extraction

## Overview
This project explores various approaches to **unsupervised document classification** and **information extraction** from unstructured data using PDF files from the ICDAR 2024 dataset. The main tasks include:

1. **Information Extraction:** Extracting titles and authors from the provided PDF files.
2. **Document Classification:** Classifying each paper into predefined categories and/or analyzing the content to identify better-suited categories.

The solution utilizes **Sentence Transformers models**, **BertTopic**, **K-Means clustering**, and **Lbl2Vec** for the experiments, and the results are saved in a structured JSON format. Model fitting and text encodings were run on a **GPU environment** provided by Google Colab to enhance performance during training and classification.

## Project Structure

- `MLE_Assignment.ipynb`: Jupyter notebook containing the full solution and experiments.
- `output.json`: The final JSON output file with extracted titles, authors, and classifications.

## Requirements

To run the project, the following tools and libraries are required:

- **Python 3.8+**
- **Jupyter Notebook** or **Google Colab**
- Libraries including:
  - SentenceTransformer
  - Torch
  - Pandas
  - Scikit-learn
  - BertTopic
  - Lbl2Vec



## Instructions to Run the Code

1. Open the `MLE_Assignment.ipynb` Jupyter notebook in **Google Colab**.
2. **Enable GPU:** Some parts of the code require GPU for faster processing. To enable the GPU runtime, navigate to `Runtime -> Change runtime type -> GPU` in Colab.
3. **Upload files:** Upload the `ICDAR 2024 paper list.csv` and the `ICDAR2024_proceedings_pdfs` folder to your Google Drive.
4. **Run the notebook:** Execute all the cells in the notebook. This will:
   - Install and import all libraries and packages
   - Parse the PDF files.
   - Perform title and author extraction using text from the PDFs.
   - Evaluate the performance of the extraction.
   - **Implement experiments regarding classification**.
   - Classify each document into one of the predefined categories using **Lbl2TransformerVec**.
   
5. The final results will be saved in `output.json`, with the following structure:

```json
{
  "tables": [
    {"originalFileName": "paper_A.pdf", "title": "recognized title", "authors": ["author_A", "author_B"]},
    ...
  ],
  "classification": [...],
  "keyInformationExtraction": [...],
  "opticalCharacterRecognition": [...],
  "datasets": [...],
  "layoutUnderstanding": [...],
  "others": [...]
}
```

## Output

The `output.json` file contains the extracted information for each document, categorized into tables such as **classification**, **key information extraction**, **optical character recognition**, and others based on the experiments performed.

