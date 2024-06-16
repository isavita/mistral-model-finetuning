# Mistral Model Fine-tuning

This project demonstrates how to fine-tune a Mistral model using the Advent of Code dataset.

## Project Structure

```
.
├── data/
│   ├── chunk_eval.jsonl
│   ├── chunk_train.jsonl
│   └── python_418.jsonl
└── notebooks/
    └── data_preparation.ipynb
```

- The `data/` directory contains the training and evaluation data in JSONL format.
  - `chunk_eval.jsonl`: Evaluation data
  - `chunk_train.jsonl`: Training data
  - `python_418.jsonl`: Full dataset for Python solutions

- The `notebooks/` directory contains Jupyter notebooks for data preparation and model fine-tuning.
  - `data_preparation.ipynb`: Notebook for data loading, preprocessing, and template generation

## Getting Started

1. Clone the repository:
   ```
   git clone https://github.com/your-username/mistral-model-finetuning.git
   ```

2. Install the required dependencies:
   ```
   pip install datasets pandas mistralai
   ```

3. Open the `data_preparation.ipynb` notebook in Jupyter:
   ```
   jupyter notebook notebooks/data_preparation.ipynb
   ```

4. Follow the instructions in the notebook to prepare the data and fine-tune the Mistral model.

## License

This project is licensed under the [MIT License](LICENSE).
