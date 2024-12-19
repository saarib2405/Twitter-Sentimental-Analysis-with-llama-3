# Twitter Sentiment Analysis with Llama-3-8B

This project enables sentiment analysis and tone classification of tweets using the fine-tuned Meta Llama-3-8B-Instruct model. It uses Hugging Face's transformers library and Gradio for creating an interactive interface.

## Table of Contents
- [Installation](#installation)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Code Description](#code-description)
- [How to Run](#how-to-run)
- [Acknowledgments](#acknowledgments)

---

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/twitter-sentiment-analysis.git
    cd twitter-sentiment-analysis
    ```

2. Set up a virtual environment (optional but recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

## Dependencies

Here are the dependencies and their versions required for this project:

- **Python** >= 3.8
- **torch** >= 2.0.1
- **transformers** >= 4.33.3
- **gradio** >= 3.39
- **spaces** >= 0.2.3

The required dependencies are listed in the `requirements.txt` file:
```txt
torch>=2.0.1
transformers>=4.33.3
gradio>=3.39
spaces>=0.2.3
```

---

## Usage

This project uses a fine-tuned Llama-3-8B-Instruct model hosted on Hugging Face for text generation and analysis. You'll need to set up your Hugging Face API token to access the model.

### Steps:
1. Obtain a Hugging Face API token by logging into [Hugging Face](https://huggingface.co/).
2. Replace the `"Enter your own token"` placeholder in the code with your Hugging Face token.
3. Use the Gradio interface to interact with the model for sentiment analysis and tone classification.

---

## Code Description

The primary script is structured as follows:

1. **Imports:**
    - Required libraries like `torch`, `transformers`, `gradio`, and `spaces` are imported.

2. **Model Setup:**
    - The Llama-3-8B-Instruct model is loaded using Hugging Face's `transformers.pipeline` for text generation.

3. **Gradio Interface:**
    - The Gradio `ChatInterface` is used to create an interactive chat interface with a textbox for input and sliders for model parameters like `Max New Tokens` and `Temperature`.

4. **Chat Function:**
    - A function `chat_function` processes user input, generates predictions, and returns outputs using the fine-tuned model.

---

## How to Run

1. Launch the application using the following command:
    ```bash
    python app.py
    ```

2. Open the Gradio interface in your browser (a URL will be displayed in the terminal).
3. Input a tweet in the textbox and adjust the system prompt, max tokens, and temperature as needed.
4. Analyze the sentiment and tone of the input text.

---

## Example System Prompt

Use this system prompt for a detailed analysis:
```txt
Analyze the provided text and classify sentiment (positive, negative, neutral) and tone (formal, informal). Return a sentiment, tone, and a brief reason (max 100 characters) for the classifications.
```

---

## Acknowledgments

- **Meta** for providing the Llama-3-8B model.
- **Hugging Face** for their transformers library.
- **Gradio** for creating an easy-to-use interface.

Feel free to customize this repository as per your needs. Happy coding!
