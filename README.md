# Gender Representation Bias in Gendered Languages

Repository accompanying the anonymous submission of a paper titled "Leveraging Large Language Models to Measure Gender Representation Bias in Gendered Language Corpora" to the ACL 2025 GeBNLP Workshop.

## Repository Structure

- `code`: Code for dataset analysis, continual pretraining, inference, and validation
  - `bias-quantification`: Gender representation bias quantification in a given dataset
  - `continual-pretraining`: Continual pretraining and model inference to evaluate how gender representation bias in training data propagates to the model inference
  - `validation`: Validation of the gender representation bias quantification method on an annotated dataset
- `data`: Samples of corpora, annotated datasets, prompts, few-shot examples, word skiplist, and stories for continual pretraining
  - `continual-pretraining`: Biased and balanced stories datasets generated for continual pretraining experiments
  - `corpora-en-es`: Samples of aligned parallel corpora in English and Spanish used in the experiments in the paper
  - `corpora-va`: Samples of Valencian corpora used in the experiments in the paper
  - `dataset-analysis`: Prompts, few-shot examples, and skiplist for bias evaluation
  - `validation`: Annotated (ground truth) data for gender representation bias quantification method validation

## Getting Started

### Prerequisites

- Python 3.12
- CUDA 12.1 to use GPU

### Installation

1. Clone or download the repository.

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### Gender representation bias quantification in a given dataset

In `code/bias-quantification`, use:
- `dataset-analysis-openai.ipynb` to analyze datasets in gendered languages using OpenAI API
- `dataset-analysis-groq.ipynb` to analyze datasets in gendered languages using Groq API
- `dataset-analysis-gp.ipynb` to analyze datasets in English using the Gender Polarity method

### Sample subset extraction from a corpus

To extract a sample subset from a (potentially multilingual aligned) text corpus, use `dataset-extraction.ipynb` in `code/bias-quantification`.

### Continual pretraining and inference

In `code/continual-pretraining`, use:
- `continual-pretraining.ipynb` to continually pretrain a HuggingFace model on a given raw text dataset
- `inference.ipynb` to run inference with a base or continually pretrained model

### Validation

To validate the gender representation bias quantification method on an annotated dataset, use in `code/validation`:
-  `validation-gt-openai.ipynb` to perform the validation using OpenAI API
-  `validation-gt-groq.ipynb` to perform the validation using Groq API

## License

This project is licensed under the MIT License. See the [LICENSE.txt](LICENSE.txt) file for details.