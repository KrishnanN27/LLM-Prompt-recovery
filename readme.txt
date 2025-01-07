readme.txt

Name and CSM ID:
- Name: Sowndarya Krishnan Navaneetha Kannan
- CSM ID: 10907259

Programming Language:
- Python

How the Code is Structured:
- The project is structured as follows:
  1. **`Prompt_gen.ipynb`**:
     - This Jupyter notebook contains all the steps for testing, fine-tuning, and generating prompts using GPT-2.
  
  2. **Initial Testing with GPT-2**:
     - In the first part of the notebook, GPT-2 was tested on the task of generating rewrite prompts from `original_text` and `rewritten_text` without any fine-tuning.
     - The model’s performance was poor, as it failed to generalize the task and generate meaningful prompts.

  3. **Fine-Tuning GPT-2**:
     - After initial testing, GPT-2 was fine-tuned using a dataset containing pairs of `original_text`, `rewritten_text`, and `rewrite_prompt`.
     - The notebook preprocesses the data, fine-tunes the model using the `transformers` library's `Trainer` class, and saves the fine-tuned model.
     - Despite fine-tuning, the model still showed limited improvements, and the performance did not meet expectations.

  4. **Prompt Generation**:
     - In the final part of the notebook, the fine-tuned model is used to generate prompts based on original and rewritten text.
     - The generated prompts are **printed to the console**, not saved to a file.
     - The results showed that, while fine-tuned, the model still struggled to generate accurate prompts, showing signs of overfitting and insufficient generalization.

How to Run the Code:
1. **Prerequisites**:
   - Python 3.x (preferably Python 3.8+)
   - Install required libraries:
     ```bash
     pip install pandas datasets transformers torch
     ```

2. **Set Up Virtual Environment** (optional but recommended):
   - Create a virtual environment:
     ```bash
     python -m venv venv
     ```
   - Activate the virtual environment:
     - On Windows:
       ```bash
       venv\Scripts\activate
       ```
     - On macOS/Linux:
       ```bash
       source venv/bin/activate
       ```

3. **Running the Notebook**:
   - Open the **`Prompt_gen.ipynb`** notebook in Jupyter:
     ```bash
     jupyter notebook Prompt_gen.ipynb
     ```
   - Run the notebook step by step to:
     - Test GPT-2's initial performance on the task.
     - Fine-tune GPT-2 on the dataset.
     - Generate prompts using the fine-tuned model (results will be printed to the console).

4. **Model and Tokenizer**:
   - The fine-tuned model and tokenizer will be saved in the `v2-gpt2-finetuned-rewrite` directory.

Specific Compilation Instructions:
- No compilation is required as the project is implemented in Python.
- Ensure that the Python environment is properly set up and all dependencies are installed via `pip`.
