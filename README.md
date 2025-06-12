# Text Generation model using Fine-tuned GPT-2 Model

This repository contains a fine-tuned GPT-2 model trained on a custom dataset. The process involves loading a pre-trained GPT-2 model, preparing a custom dataset, tokenizing and processing the data for language modeling, fine-tuning the model, and finally using the fine-tuned model to generate text.

## Setup

To run the code and use the fine-tuned model, you need to install the necessary libraries. You can do this using pip:
Note: You might need to install `torch` separately if it's not already present in your environment.

## Fine-tuning Process

The fine-tuning process follows these steps:

1.  **Load GPT-2 Model & Tokenizer:** The pre-trained GPT-2 model and its tokenizer are loaded from the Hugging Face `transformers` library. A padding token is added to the tokenizer.
2.  **Load and Prepare Custom Dataset:** A custom dataset (in this case, a list of strings) is defined and converted into a Hugging Face `datasets` compatible format.
3.  **Tokenize Custom Dataset:** The custom dataset is tokenized using the loaded tokenizer.
4.  **Prepare Data for Language Modeling:** The tokenized dataset is processed for causal language modeling by concatenating and chunking the texts.
5.  **Fine-tune the GPT-2 Model:** The model is fine-tuned using the `Trainer` class from the `transformers` library with defined training arguments.
6.  **Save the Fine-tuned Model:** The fine-tuned model and tokenizer are saved to a local directory.

The code for these steps is provided in the Jupyter Notebook/Python script.

## Generating Text

After fine-tuning and saving the model, you can load the fine-tuned model and tokenizer to generate text based on a given prompt. The code includes a function `generate_text` that demonstrates how to do this, showcasing both greedy search and beam search generation strategies.

## Files

*   `your_notebook_name.ipynb` (or your Python script): Contains the code for the entire process, from setup to text generation.
*   `./gpt2_finetuned_custom_data/`: This directory will be created after running the fine-tuning process and will contain the saved fine-tuned model and tokenizer files.

## Usage

1.  Clone this repository.
2.  Open and run the Jupyter Notebook (`your_notebook_name.ipynb`) or execute the Python script.
3.  Follow the steps in the notebook/script to load the model, prepare data, fine-tune, save, and generate text.
4.  Modify the `custom_texts` variable in the notebook to use your own data for fine-tuning.
5.  Experiment with different prompts and generation parameters in the `generate_text` function.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
