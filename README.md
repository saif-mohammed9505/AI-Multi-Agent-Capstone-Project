# 🤖 AI Multi-Agent Capstone

A modular AI Multi-Agent system that combines autonomous planning, specialized agents, Retrieval-Augmented Generation (RAG), neural networks, Hugging Face datasets, a fine-tuned LLM, Modal GPU deployment, and an interactive visualization interface.

## ✨ Features

- 🤖 Multi-Agent Architecture
- 🧠 Autonomous Planning
- 🔎 Retrieval-Augmented Generation (RAG)
- 🗃️ ChromaDB Vector Database
- 🤗 Hugging Face Dataset Integration
- 🎯 Fine-Tuned Llama 3.2 Model
- 🧬 PyTorch Neural Network
- 🎯 Ensemble Decision Making
- 🔬 Specialized AI Agents
- 💬 LLM-powered Agents
- ☁️ Modal Cloud GPU Deployment
- 🎨 Gradio-based Visualization
- 📊 Evaluation Components
- 🧹 Data Preprocessing
- 🔐 Environment-based Secret Management

## 🛠️ Tech Stack

- Python
- PyTorch
- Transformers
- Hugging Face Hub
- Hugging Face Datasets
- LangChain
- ChromaDB
- Sentence Transformers
- OpenAI Python SDK
- OpenRouter
- Ollama
- Modal
- Gradio
- Pydantic
- NumPy
- Pandas
- Scikit-learn
- python-dotenv

## 🤖 Models

### Base Model

- Meta Llama 3.2 3B: `meta-llama/Llama-3.2-3B`

### Fine-Tuned Model

A fine-tuned version of Llama 3.2 3B is used in the project and hosted on Hugging Face for remote inference.

### Other Models / Components

- OpenRouter models
- Ollama models
- Sentence Transformer embedding models
- Custom PyTorch neural network

## 🤗 Hugging Face Dataset

The project uses an adapted version of:

**`ed-donner/items_lite`**

Original dataset:

https://huggingface.co/datasets/ed-donner/items_lite

The dataset is maintained under the project's Hugging Face account and is used as part of the data preparation and fine-tuning workflow.

The original dataset source is credited above, and its original license and usage requirements should be followed.

### My Dataset

Hugging Face Dataset:

https://huggingface.co/datasets/MdSaif0718/scraped_amazon__data

## 🎯 Fine-Tuning

The fine-tuning workflow follows:

    Hugging Face Dataset
            ↓
    Data Preparation
            ↓
    Training Dataset
            ↓
    Llama 3.2 3B
            ↓
    Fine-Tuning
            ↓
    Fine-Tuned Model
            ↓
    Hugging Face Hub
            ↓
    Modal GPU Inference
            ↓
    AI Agent

The large model weights are hosted remotely rather than stored directly in the GitHub repository.

## ☁️ Modal Deployment

The project uses Modal to run the fine-tuned LLM on remote GPU infrastructure.

The Modal service handles:

- Remote GPU execution
- Loading the Hugging Face model
- Loading the fine-tuned model
- Running model inference
- Providing the model to the agent system

Sensitive Hugging Face credentials are managed through Modal Secrets instead of being hard-coded in the source code.

### Modal Workflow

    AI Agent
        ↓
    Modal Service
        ↓
    Remote GPU
        ↓
    Hugging Face Model
        ↓
    Fine-Tuned LLM
        ↓
    Inference Response
        ↓
    AI Agent

## 🔎 RAG Pipeline

The project includes a Retrieval-Augmented Generation pipeline for retrieving relevant information and providing it as context to an LLM.

    Documents
        ↓
    Preprocessing
        ↓
    Text Chunking
        ↓
    Embeddings
        ↓
    ChromaDB
        ↓
    Similarity Search
        ↓
    Relevant Context
        ↓
    LLM
        ↓
    Generated Response

### RAG Components

- LangChain
- Sentence Transformers
- Hugging Face Embeddings
- ChromaDB
- Text Splitters
- Vector Similarity Search
- Retrieval
- Re-ranking
- LLM Generation

## 🤖 Multi-Agent Architecture

The project contains multiple specialized agents:

- **Agent** — Base agent functionality
- **Planning Agent** — Task planning and coordination
- **Autonomous Planning Agent** — Autonomous multi-step workflows
- **Scanner Agent** — Scanning and information collection
- **Frontier Agent** — Retrieval and knowledge processing
- **Ensemble Agent** — Combines outputs from multiple agents/models
- **Neural Network Agent** — Neural-network inference
- **Specialist Agent** — Specialized model integration
- **Messaging Agent** — Notifications and messaging
- **Evaluator** — Evaluation utilities
- **Preprocessor** — Data preprocessing

## 🧠 Autonomous Planning

The autonomous planning component allows the system to decompose complex tasks and coordinate different agents.

    User Request
        ↓
    Task Planning
        ↓
    Task Decomposition
        ↓
    Agent Selection
        ↓
    Agent Execution
        ↓
    Result Collection
        ↓
    Decision Making
        ↓
    Final Response

## 🧬 Neural Network

The project also contains a PyTorch-based deep neural network component for inference.

The neural network includes:

- Fully connected layers
- Residual connections
- Normalization
- Dropout
- Non-linear activation functions
- Trained model weights

Large model weight files are excluded from Git where appropriate.

## 🎨 Visualization / Gradio UI

The project includes a Gradio-based interactive visualization interface for interacting with and demonstrating the AI system.

The interface provides a simple way to interact with the underlying agents, models, and AI workflow.

## 📊 Evaluation

The project contains evaluation components for analyzing different parts of the AI workflow.

Evaluation can be applied to:

- Retrieval quality
- Similarity matching
- Agent outputs
- Model predictions
- Decision consistency
- RAG performance

## 📂 Project Structure

    AI-Multi-Agent-Capstone/
    │
    ├── agents/
    │   ├── agent.py
    │   ├── autonomous_planning_agent.py
    │   ├── deals.py
    │   ├── deep_neural_network.py
    │   ├── ensemble_agent.py
    │   ├── evaluator.py
    │   ├── frontier_agent.py
    │   ├── items.py
    │   ├── messaging_agent.py
    │   ├── neural_network_agent.py
    │   ├── planning_agent.py
    │   ├── preprocessor.py
    │   ├── scanner_agent.py
    │   └── specialist_agent.py
    │
    ├── adding_rag.ipynb
    ├── agents.ipynb
    ├── gradio_ui.ipynb
    ├── pricer_service.py
    ├── requirements.txt
    ├── .gitignore
    └── README.md

## ⚙️ Installation

### 1. Clone the repository

    git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
    cd YOUR_REPOSITORY

### 2. Create a virtual environment

    python -m venv .venv

### 3. Activate the virtual environment

Windows:

    .venv\Scripts\activate

Linux / macOS:

    source .venv/bin/activate

### 4. Install dependencies

    pip install -r requirements.txt

## 🔑 API Configuration

Create a `.env` file in the project directory when API credentials are required.

Example:

    OPENROUTER_API_KEY=your_openrouter_api_key
    PUSHOVER_USER=your_pushover_user
    PUSHOVER_TOKEN=your_pushover_token

Never upload your actual `.env` file or API keys to GitHub.

Credentials should be provided through environment variables or Modal Secrets.

## 🦙 Ollama Setup

To use local Ollama models, install Ollama and pull the required model:

    ollama pull llama3.2

The local Ollama API is available through:

    http://localhost:11434/v1

## ☁️ Modal Setup

Install Modal:

    pip install modal

Authenticate:

    modal setup

Configure the required Hugging Face secret in Modal.

Deploy the model service:

    modal deploy pricer_service.py

## 🚀 Usage

### Run the notebooks

Start Jupyter:

    jupyter notebook

or:

    jupyter lab

The main notebooks include:

- `agents.ipynb` — Agent development and experimentation
- `adding_rag.ipynb` — RAG implementation
- `gradio_ui.ipynb` — Interactive visualization and UI

Run the notebooks according to the component you want to explore.

### Run the Modal service

After configuring Modal and the required secrets:

    modal deploy pricer_service.py

The deployed service provides remote inference for the fine-tuned model.

## 🔄 End-to-End Workflow

    User Request
        ↓
    Planning Agent
        ↓
    Specialized Agents
        ↓
    Data / RAG / Neural Network
        ↓
    Ensemble Decision
        ↓
    Fine-Tuned LLM
        ↓
    Modal GPU Inference
        ↓
    Visualization / Gradio
        ↓
    Final Output

## 🔒 Security

The repository is designed to keep sensitive information outside the source code.

Do not commit:

- API keys
- Hugging Face tokens
- Modal credentials
- `.env` files
- Passwords
- Large model weights
- Local databases
- Virtual environments
- Cache files

Use environment variables and cloud secret management for sensitive credentials.

## 📦 Large Model Files

Large files such as:

    *.pth
    *.pt
    *.bin
    *.safetensors
    *.ckpt
    *.h5
    *.keras

are excluded from Git where appropriate.

Required models can instead be loaded from Hugging Face or the configured remote model service.

## 🎯 Project Goal

The goal of this project is to demonstrate practical AI engineering by combining:

- Multi-agent systems
- Autonomous planning
- LLM integration
- RAG
- Vector databases
- Neural-network inference
- Fine-tuning
- Hugging Face model hosting
- Cloud GPU inference
- Modal deployment
- AI evaluation
- Interactive visualization

## 🔮 Future Improvements

- Add more specialized agents
- Improve agent orchestration
- Improve RAG retrieval and re-ranking
- Add additional evaluation benchmarks
- Improve visualization
- Add streaming responses
- Add automated testing
- Add CI/CD
- Improve production deployment
- Support additional fine-tuned models
- Add more advanced agent workflows

## 👨‍💻 Author

**Saif Mohammed**

AI / Machine Learning / LLM & Multi-Agent Systems

## 🙏 Acknowledgements

This project uses and builds upon technologies and resources from the AI/ML ecosystem, including:

- Hugging Face
- Meta Llama
- LangChain
- ChromaDB
- PyTorch
- Modal
- Gradio
- OpenRouter
- Ollama
- Sentence Transformers

Special acknowledgement is given to the original dataset:

**`ed-donner/items_lite`**

Please refer to the respective licenses and usage terms of the datasets, models, and libraries used in this project.

## ⭐ Project Summary

This project combines multi-agent systems, autonomous planning, RAG, neural networks, fine-tuned LLMs, Hugging Face, Modal cloud inference, and interactive visualization into a single AI engineering project.
