# Fake News Detector

This project is a **Fake News Detector** that uses natural language processing and machine learning techniques to identify fake news articles. It employs the **TfidfVectorizer** and **Logistic Regression** algorithms to classify news articles as either real or fake based on their content.

## Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.x
- Jupyter Notebook (optional, but recommended for interactive execution)

Ensure the required libraries are installed:

```bash
pip install numpy pandas nltk scikit-learn
```

## Usage

1. Clone the repository or download the project files.
2. Download the NLTK stopwords dataset:

```python
import nltk
nltk.download('stopwords')
```

3. Run the **fake_news_detector.ipynb** notebook in Jupyter or execute the code in a Python environment.

## Project Description

### Data Preparation

1. The project utilizes a dataset stored in the **train.csv** file containing information about news articles.
2. Missing values in the dataset are filled with empty strings.
3. The 'author' and 'title' columns are merged to create a new 'content' column containing both the author and title information.
4. Text preprocessing is applied to the content by converting it to lowercase, removing non-alphabetic characters, tokenizing, removing stopwords, and stemming words.

### Feature Extraction

1. The textual data is converted into numerical feature vectors using the **TfidfVectorizer** from the scikit-learn library.

### Model Training

1. The dataset is split into training and testing sets using a test size of 20%.
2. A **Logistic Regression** model is trained on the training data.

### Model Evaluation

1. The accuracy scores of the model are computed for both the training and testing datasets.

## Results

After running the project, you should see the accuracy scores for the training and testing data:

- Accuracy Score for Training Data: 0.9865985576923076
- Accuracy Score for Test Data: 0.9790865384615385

These scores indicate the performance of the Fake News Detector model on the respective datasets.

## Contributing

If you find any issues with the project or have ideas to improve it, feel free to contribute. You can create pull requests or raise issues in the repository.

## License

This project is licensed under the [MIT License](LICENSE).

---

Please note that the project dataset (**train.csv**) is not included in this README. Make sure to provide the dataset in the same directory as the notebook or update the file path accordingly in the code. Additionally, the HTML representation of the notebook may not render correctly on GitHub, so it's recommended to run the notebook in a Jupyter environment for the best experience.
