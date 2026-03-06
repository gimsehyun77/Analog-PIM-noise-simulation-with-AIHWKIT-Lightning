Analog-PIM-noise-simulation-with-AIHWKIT-Lightning

This repository explores the impact of analog non-idealities in Processing-In-Memory (PIM) systems on language model performance. The project includes fine-tuning of DistilGPT-2, analog noise injection using AIHWKIT Lightning, and graph-based visualization of performance degradation under analog noise conditions.

All experiments are conducted on a personal GPU server environment, allowing controlled and reproducible evaluation of analog PIM noise effects on transformer-based language models.

Repository Structure

The codebase is organized into three main stages:

1. Fine-tuning

This stage fine-tunes the DistilGPT-2 language model on the training dataset to obtain a task-adapted digital baseline model.
The resulting model serves as the reference point for later noise-injection experiments.

Main tasks:

Load and preprocess dataset

Fine-tune DistilGPT-2

Save the trained model for evaluation

2. Testing (Noise Injection Experiments)

This stage evaluates the model under analog noise conditions.

Noise is injected into specific transformer layers or components (e.g., attention, MLP, LayerNorm) to simulate analog hardware non-idealities. The model performance is then measured using Perplexity (PPL).

Main tasks:

Inject analog-like noise into selected model weights

Perform layer-wise and component-wise noise experiments

Measure performance degradation (PPL)

Store experiment results

3. Visualization

This stage analyzes and visualizes the experimental results.

The stored results are processed to generate plots and heatmaps that illustrate how model performance changes under different noise levels and across different layers.

Main tasks:

Convert experiment results into structured data

Generate layer-wise performance plots

Create heatmaps showing noise sensitivity across layers and operations

Experiment Pipeline
Fine-tuning
      ↓
Digital Baseline Model
      ↓
Noise Injection Experiments
      ↓
Performance Measurement (Perplexity)
      ↓
Visualization & Analysis
Key Technologies

PyTorch

HuggingFace Transformers

AIHWKIT Lightning

NumPy / Pandas

Matplotlib
