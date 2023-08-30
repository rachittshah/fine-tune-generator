# fine-tune-generator
A fine-tuning library leveraging distilled GPT-4 outputs to fine-tune to GPT-3.5 for better accuracy.

Fine-tuning task-specific LLMs has the potential to defeat raw GPT-4 outputs(until we get FTed GPT-4 lol).

## Overview
Distillation from GPT-4 to GPT-3.5 can be particularly useful for specific tasks. This library provides a structured approach to achieve this goal. While the experiment is ongoing regarding the granularity of tasks and the quantity of data, this code is shared to benefit the community.

## Features

### What it does:
- Accepts a list of input prompts.
- Generates answers using GPT-4.
- Uploads the data to OpenAI.
- Fine-tunes a GPT-3.5 model based on the generated data.

### Configurable Parameters:
- **GPT-4 Parameters:** 
    - `temperature`: Adjusts randomness in model's output.
    - `max_tokens`: Maximum token limit for the output.
    - `system_prompt`: Provides a system message to guide the model.
- **Fine-tuning Parameters:** 
    - `n_epochs`: Number of epochs for fine-tuning.
    - `repetitions`: Number of times data is repeated for fine-tuning.

## Getting Started

1. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
2. Run the main script with your data file:
    ```bash
    python main.py your_file.txt
    ```

## Roadmap

- **Cost Estimation:** Determine the cost of distillation and identify the breakeven point between fine-tuned GPT-3.5 and GPT-4.
- **Data Augmentation:** Enhance seed data augmentation using GPT-4.
- **PyPi Package:** Create a PyPi package for easy installation.
- **Integrate with datasetGPT**: [https://github.com/radi-cho/datasetGPT](datasetGPT) is a lightweight GPT based dataset generator. Combining the two libraries will allow for a more streamlined process.
- **Add monitoring and logging**: Add monitoring and logging to the library to track the progress of the fine-tuning process.

## License
Please refer to the `LICENSE` file for licensing information.
