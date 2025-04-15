# DeepSeek Models with Ollama

A comprehensive toolkit for running and interacting with DeepSeek models using Ollama in Google Colab.

## Overview

This script provides a complete environment for working with DeepSeek models in Google Colab using Ollama. It features a wide range of utilities from basic model interaction to advanced benchmarking and comparison tools.

## Features

### Core Features
- **Automatic Ollama Setup**: One-click installation and configuration of Ollama
- **Model Management**: Easy downloading and selection of DeepSeek models
- **Interactive Chat**: Full-featured chat interface with DeepSeek models

### Advanced Features
- **Model Benchmarking**: Compare performance across different models and settings
- **Multi-Model Comparison**: Side-by-side response comparison
- **Batch Processing**: Process multiple prompts efficiently
- **Chat History Management**: Save and load conversation history
- **Resource Monitoring**: Track CPU, RAM, and GPU usage during model operation
- **Web UI**: Optional Gradio interface for easier interaction
- **File Input Processing**: Use document content as context for the model

## Quick Start

1. Open the script in Google Colab
2. Run the script to install Ollama and setup the environment
3. Pull a DeepSeek model of your choice
4. Start interacting with the model through the interactive chat

## Detailed Usage

### Interactive Chat

The interactive chat interface provides a conversational experience with the model. Special commands are available during chat:

- `/save`: Save the current chat history
- `/file`: Upload and use a file as context
- `/reset`: Reset the conversation
- `/system <prompt>`: Change the system prompt
- `/help`: Show available commands

Example:
```
You: Tell me about large language models

deepseek-llm:7b: Large language models (LLMs) are advanced AI systems...

You: /system You are an expert in quantum physics

System prompt updated: "You are an expert in quantum physics"

You: Explain entanglement

deepseek-llm:7b: Quantum entanglement is a phenomenon in quantum physics...
```

### Model Benchmarking

The benchmarking tool allows you to compare performance across different models:

1. Select models to benchmark
2. Enter prompts or load from a file
3. Configure parameters (system prompt, max tokens, temperature)
4. Run the benchmark
5. View and save comparative results

### Multi-Model Comparison

Compare responses from different models for the same prompt:

1. Select up to 4 models to compare
2. Enter a prompt for comparison
3. Configure parameters
4. View side-by-side response comparison with timing statistics

### Batch Processing

Process multiple prompts efficiently:

1. Select a model
2. Load prompts manually, from CSV, or from a text file
3. Configure model parameters
4. Process all prompts with a single command
5. Export results to CSV

### Chat History Management

- Save chat history to JSON files
- Load and continue previous conversations
- Organize conversations by model and timestamp

### Resource Monitoring

Track and visualize system resource usage:

- Real-time CPU usage monitoring
- RAM usage tracking
- GPU utilization (if available)
- Visualization of resource usage

### Web UI

Launch a user-friendly web interface using Gradio:

1. Configure system prompt and model settings
2. Chat through a clean web interface
3. Share the interface with others

## Advanced Settings

Configure model behavior with advanced settings:

- System prompt customization
- Maximum token length adjustment
- Temperature and top_p sampling parameters
- Resource monitoring options

## Installation

This script is designed for Google Colab and handles all necessary installation automatically.

Required dependencies:
- Python 3.6+
- requests
- psutil
- matplotlib
- pandas
- tqdm

Optional dependencies:
- gradio (for Web UI)
- torch (for GPU monitoring)

## Directory Structure

The script creates the following directory structure:

```
./
├── chat_history/      # Saved chat histories
├── benchmarks/        # Benchmark and comparison results
├── model_configs/     # Model configuration files
└── input_files/       # Uploaded input files
```

## Examples

### Basic Chat Example
```python
# Start interactive chat with default settings
interactive_chat(model_name="deepseek-llm:7b")
```

### API Usage Example
```python
# Query the model directly
response = query_deepseek(
    prompt="Explain quantum computing in simple terms.",
    model="deepseek-llm:7b",
    stream=False,
    system_prompt="Explain concepts simply.",
    max_tokens=1024,
    temperature=0.7
)
print(response)
```

## Limitations

- This script is designed specifically for Google Colab environment
- Performance depends on the Colab instance resources
- Some features require optional dependencies

## License

This script is provided for educational and research purposes.

## Acknowledgments

- DeepSeek AI for their powerful language models
- Ollama for providing easy model deployment
- Google Colab for the free computing environment

---
