# Mistral Model Fine-tuning

This project demonstrates how to fine-tune the `mistral-small` model using my [Advent of Code dataset](https://huggingface.co/datasets/isavita/advent-of-code), which contains over 7,500 solutions in 37 programming languages, from which we use a subset of 400+ Python examples.

The fine-tuning process is designed to adapt the model to solve these challenges autonomously, creating files with the solutions. By mimicking the approach of [OpenDevin](https://github.com/OpenDevin/OpenDevin), an open platform for AI software developers as generalist agents, the fine-tuned `mistral-small` model can potentially be used more effectively within the OpenDevin platform, enhancing its ability to solve programming challenges.

## Training Example

Each training example consists of a series of messages exchanged between the user and the assistant. The messages guide the assistant through the process of solving an Advent of Code challenge using Python. Here's a brief overview of the messages:

1. The user presents the Advent of Code challenge to the assistant and asks for a solution in Python.
2. The assistant responds by creating a new Python file named `solution.py`.
3. The user observes the creation of the new file.
4. The assistant writes the Python solution code to the `solution.py` file.

This exchange of messages allows the model to learn how to autonomously solve Advent of Code challenges by creating and writing to Python files.

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
