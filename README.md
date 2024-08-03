# Attention

This project demonstrates how to visualize the attention mechanism of a pre-trained BERT model. The script allows users to input text with a mask token, retrieves top predictions for the mask token, and generates attention diagrams showing the attention weights across different layers and heads.

## Description

This project uses the BERT (Bidirectional Encoder Representations from Transformers) model to predict masked words within a text sequence. BERT is a transformer-based language model developed by Google, trained to predict a masked word based on its surrounding context. The project involves two main tasks:

1. **Masked Word Prediction**: Using the Hugging Face transformers library, the program predicts masked words in an input text. The user inputs text containing a `[MASK]` token, and the program outputs the top predictions for the masked word.

2. **Attention Visualization**: The program generates diagrams visualizing attention scores for each of BERT's 144 attention heads. These diagrams help users understand which words BERT focuses on when making predictions.

## Features

- **Masked Word Prediction**: Predicts the masked word in a text sequence using BERT.
- **Attention Diagrams**: Generates and saves visualizations of attention scores for each attention head across all layers.
- **Configurable Parameters**: Allows customization of the number of predictions, font settings, grid size, and output options.
- **Console Output**: Optionally prints predictions and attention values to the console.
- **Output Directory**: Saves generated diagrams to a specified output folder.

## Goal

The goal of this project is to provide insights into the inner workings of the BERT model by visualizing its attention mechanism. By analyzing the attention diagrams, users can gain a better understanding of what BERT pays attention to when processing language, which can be particularly useful for debugging and improving language models.

## Getting Started

1. **Installation**:
   - Clone the repository and navigate to the project directory.
   - Create a virtual environment and activate it.
   - Install the required packages using `pip install -r requirements.txt`.

2. **Running the Script**:
   - Execute the script using `python script.py`.
   - Input the text with the `[MASK]` token when prompted.
   - View the predictions and attention diagrams as per the configured output options.

## Example Usage

```bash
$ python script.py
Text: We turned down a narrow lane and passed through a small [MASK].
Top Predictions:
1. We turned down a narrow lane and passed through a small field.
2. We turned down a narrow lane and passed through a small clearing.
3. We turned down a narrow lane and passed through a small park.
```

## Configuration Parameters

- **MODEL**: Identifier for the pre-trained masked language model (e.g., `"bert-base-uncased"`).
- **K**: Number of top predictions to generate for the mask token.
- **FONT**: Default font for drawing text on images; can be adjusted as needed.
- **BASE_GRID_SIZE**: Base size of each grid cell in the attention diagram.
- **PIXELS_PER_WORD**: Pixels allocated per word for image dimensions.
- **PRINT_TO_CONSOLE**: If `True`, prints the predictions and attention values to the console.
- **SAVE_TO_OUTPUT_FOLDER**: If `True`, saves the generated diagrams to the output folder.

## License

This project is licensed under the MIT License.
```

For further details and updates, you can refer to the [CS50 AI course page](https://cs50.harvard.edu/ai/2024/projects/6/attention/).
