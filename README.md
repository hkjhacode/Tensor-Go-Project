# TensorGO Project

<p align="center">
<img src="TensorGo_Perfect.png" alt="Tensor-GO" width="500" height="124">
</p>

Welcome to the **TensorGO Project**! This project leverages the power of large language models (LLMs) to analyze and visualize datasets, providing insights and answers to user queries. Using the Llama-2 model, this tool is designed to assist with data analysis in a concise and helpful manner.

## Project Overview

This project demonstrates how to:

- **Install and configure Llama models** for data analysis.
- **Load and process datasets** using Python.
- **Generate detailed insights** and visualizations based on user queries.
- **Automate the interaction** between a CSV dataset and an AI Assistant.

## Features

- **Easy Setup**: Quickly get started by installing the necessary dependencies.
- **Data Analysis**: Load your CSV files and get immediate analysis and summaries.
- **Visualization**: Generate graphs and plots on the fly based on your queries.
- **Interactive Prompts**: Engage with the AI Assistant to get specific answers or visualizations based on your data.

## Installation

1. Clone this repository to your local machine:
    ```sh
    git clone https://github.com/yourusername/tensorgo.git
    cd tensorgo
    ```

2. Install the required Python packages:
    ```sh
    pip install -r requirements.txt
    ```

3. Download the Llama-2 model:
    ```python
    from huggingface_hub import hf_hub_download
    model_name_or_path = "TheBloke/Llama-2-13B-chat-GGML"
    model_basename = "llama-2-13b-chat.ggmlv3.q5_1.bin"
    model_path = hf_hub_download(repo_id=model_name_or_path, filename=model_basename)
    ```

## Usage

1. **Load the dataset**:
    ```python
    import pandas as pd
    csv = pd.read_csv("path/to/your/dataset.csv")
    ```

2. **Generate analysis**:
    ```python
    generate_prompt("What is the average flipper length of penguins?")
    ```

3. **Visualize data**:
    ```python
    generate_answer("Show a plot of flipper length vs body mass")
    ```

## Example

```python
# Importing necessary libraries
import pandas as pd
from llama_cpp import Llama

# Load the model
lcpp_llm = Llama(model_path=model_path)

# Load a sample dataset
csv = pd.read_csv("penguins.csv")

# Generate a prompt and get an answer
question = "What is the average body mass of penguins?"
answer = generate_answer(question, csv)
print(answer)
```

![Example Visualization](plot.png)

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue.

## Acknowledgments

- Special thanks to the Hugging Face community for providing the Llama models.
- Inspired by real-world data analysis challenges and the potential of AI in automating insights.

--- 




