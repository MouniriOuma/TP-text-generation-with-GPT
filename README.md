# Text Generation with Transformers

This repository contains a Python script for generating text using pre-trained models from the `transformers` library. It utilizes the `pipeline` module for easy text generation and demonstrates how to customize generation parameters.

## Overview

The script defines a function called `generate_story` which encapsulates the text generation process. This function takes several parameters that allow for customization of the generated text, including:

*   **Initial Phrase:** The starting point for the generated text (set to "My idea from the start was ...").
*   **Model Name:** The pre-trained GPT model to use (e.g., gpt2, gpt2-medium, etc.).
*   **Maximum Length:** The maximum number of tokens in the generated text.
*   **Seed:** An optional seed for ensuring reproducible results.
*   **Temperature:** Controls the randomness or creativity of the generated text.
*   **Top-p:** Controls the diversity of the generated text.
*   **Repetition Penalty:** Controls how likely the model is to repeat words or phrases.

The script then demonstrates how to call the `generate_story` function with different combinations of these parameters to explore various text generation results, which are then outputted to the console.


## How It Works

The script uses the Hugging Face `transformers` library, which provides pre-trained models and easy-to-use pipelines for various NLP tasks, including text generation.

Here's a breakdown of the process:

1.  **Setup:** The script imports the necessary libraries and handles potential SSL certificate issues when downloading libraries.
2.  **`generate_story` function:** This function is configured to use the text-generation pipeline and can be called with different parameters to customize text generation.
3.  **Main execution:** The main body of the code demonstrates how to use `generate_story` by calling it multiple times with various parameters, showcasing the control provided by this function and its ability to demonstrate different text generation capabilities. These different calls include:
    *   Default text generation with the starting phrase.
    *   Text generation with the starting phrase, a specific seed, temperature, top-p and max length.
    *   Text generation with the starting phrase with three calls each using different random seeds, and a max length.
    *   Text generation using the starting phrase but with a different model, `gpt2-medium`.
