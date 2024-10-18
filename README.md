
# GPT-2 Fine-Tuning for Creative-Writing with MLflow and Gradio Integration

This project demonstrates how to fine-tune the GPT-2 language model for creative text generation, track experiments using MLflow, and deploy the model via Gradio with public access using ngrok.

## Project Overview

This repository includes:
- Fine-tuning GPT-2 using a cleaned creative writing dataset.
- Experiment tracking with MLflow (SQLite as backend store).
- Web interface for text generation using Gradio.
- Model deployment with ngrok for public access.

## Key Features
- **GPT-2 Fine-Tuning**: Fine-tune GPT-2 on custom data with Hugging Face's `transformers` library.
- **Experiment Tracking with MLflow**: Log hyperparameters, metrics, and models, and visualize experiment results.
- **Gradio Web Interface**: Build a user-friendly interface to generate text from a given prompt using Gradio.
- **ngrok for Public Access**: Establish an ngrok tunnel to make your local web app accessible via the internet.

## Requirements

To run the project, you'll need the following dependencies:

- `transformers`
- `datasets`
- `torch`
- `mlflow`
- `pyngrok`
- `gradio`
- `wandb`

Install the dependencies via `pip`:

```bash
pip install transformers datasets torch mlflow pyngrok gradio wandb
```

## Project Structure

```bash
|-- README.md                   # Project description
|-- main.ipynb                  # Main script to fine-tune GPT-2 and set up Gradio UI
|-- mlflow.db                   # SQLite database for MLflow tracking
|-- ngrok_tunnel.py             # Script to set up ngrok tunnel
|-- results/                    # Directory to store model checkpoints
|-- cleaned_creative_writing_dataset.csv  # Dataset for fine-tuning
|-- requirements.txt            # List of required Python packages
|-- fine_tuned_gpt2/            # Directory to store the fine-tuned GPT-2 model
```

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/AbdallaNassar/Fine-Tuning-GPT-2-for-Creative-Writing.git
cd repo-name
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the main script to fine-tune the GPT-2 model and launch the Gradio web interface:

```bash
python main.ipynb
```

4. Access the Gradio interface:

- Once the script is running, an ngrok public URL will be provided. Use that URL to access the Gradio web interface and generate text.

## Usage

- Enter a text prompt in the Gradio web interface and generate creative stories.
- Track the training process using MLflow. Start the MLflow UI by running:

```bash
mlflow ui --backend-store-uri sqlite:///mlflow.db
```

Open [localhost:5000](http://127.0.0.1:5000) in your browser to access the UI.

## Logging with W&B

You can also log the experiment results and monitor training using Weights & Biases (W&B). To log into W&B, replace `your_api_key` in the code with your actual API key:

```bash
wandb.login(key='your_api_key')
```

## Fine-Tuning and Model Saving

The fine-tuned GPT-2 model is saved to the `fine_tuned_gpt2` directory. You can load this model and tokenizer for further use or text generation.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.



## Author

- [Abdalla Nassar](https://github.com/AbdallaNassar)
- [Mohamed Nafea](https://github.com/MoNafea01)
- [Osama Shalan](https://github.com/osama3442ws)
- [Abdulrahman Elsadiq](https://github.com/elsadiq7)
