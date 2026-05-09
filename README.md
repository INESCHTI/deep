# Neural Image Captioning with Visual Attention and Error Correction

This project is a reproduction and extension of the "Show, Attend and Tell" model for neural image captioning with visual attention.

## Overview

This project implements an attention-based encoder-decoder model for image captioning, incorporating an error correction framework. It aims to provide a comprehensive understanding of the core concepts from the original "Show, Attend and Tell" paper by Xu et al. (2015) [1] and the error analysis and correction strategies proposed by Liu and Brailsford (2023) [2].

## Project Structure

```
neural_image_captioning/
├── models/                  # Contains the Encoder, Decoder (LSTM with attention), and attention modules.
│   └── implementation.py    # Core model and correction framework logic.
├── data/                    # Placeholder for dataset classes, preprocessing utilities, and dataset folders (e.g., Flickr8k, Flickr30k).
├── training/                # Placeholder for training loop and loss functions.
├── evaluation/              # Placeholder for metrics (BLEU, METEOR) and visualization tools.
├── configs/                 # Placeholder for configuration settings.
├── scripts/                 # Placeholder for training, evaluation, and caption generation scripts.
├── notebooks/               # Jupyter notebooks for demonstration, reproduction, and analysis.
│   └── Neural_Image_Captioning_Recreation.ipynb
└── README.md                # Project README file.
```

## Installation

To set up the project and run the Jupyter Notebook, follow these steps:

### 1. Clone the repository

```bash
git clone <repository_url>
cd neural_image_captioning
```

*(Note: Replace `<repository_url>` with the actual URL if this project were hosted on a platform like GitHub.)*

### 2. Install dependencies

Ensure you have Python 3.8+ installed. The following Python libraries are required:

*   `torch`
*   `torchvision`
*   `transformers`
*   `spacy`
*   `matplotlib`
*   `Pillow`
*   `requests`

You can install them using pip:

```bash
pip install torch torchvision transformers spacy matplotlib Pillow requests
python -m spacy download en_core_web_sm
```

Alternatively, you can use a `conda` environment if preferred (environment files are not provided in this recreation but would typically be located in the `configs/` directory).

## Usage

### Jupyter Notebooks

Explore and reproduce results using the provided notebook:

1.  Launch Jupyter Notebook from the project root directory:
    ```bash
jupyter notebook
    ```
2.  Navigate to the `notebooks/` folder and open `Neural_Image_Captioning_Recreation.ipynb`.
3.  Run all cells in the notebook to see the implementations, demonstrations, and conceptual visualizations.

### Training (Conceptual)

*(Note: Full training scripts are not provided in this recreation but would typically be located in the `scripts/` directory.)*

```bash
# Example command for training (conceptual)
python scripts/train.py --config configs/default_config.yaml
```

### Evaluation (Conceptual)

*(Note: Full evaluation scripts are not provided in this recreation but would typically be located in the `scripts/` directory.)*

```bash
# Example command for evaluation (conceptual)
python scripts/evaluate.py --model_path models/trained_model.pth --dataset Flickr8k
```

### Generate Captions (Conceptual)

*(Note: Full caption generation scripts are not provided in this recreation but would typically be located in the `scripts/` directory.)*

```bash
# Example command for caption generation (conceptual)
python scripts/generate_caption.py --image_path data/test_images/sample.jpg --model_path models/trained_model.pth
```

## Data

Place the Flickr8k or Flickr30k datasets in the `data/flickr8k` or `data/flickr30k` folders, respectively. Update paths in the configuration files or the Jupyter Notebook as needed.

## Features

*   **Visual Attention Mechanism**: Implementation of the soft attention mechanism for image captioning, allowing the model to focus on relevant image regions.
*   **Error Correction Framework**: A post-processing algorithm to identify and correct semantic errors in generated captions using a language model for scoring.
*   **BLEU and METEOR Evaluation Metrics**: (Conceptual) Tools for quantitative evaluation of caption quality.
*   **Attention Map Visualization**: (Conceptual) Functionality to visualize the attention weights on images, providing interpretability.
*   **Manual and Automatic Error Analysis**: (Conceptual) Framework for analyzing common errors in generated captions.

## References

[1] Xu, K., Ba, J., Kiros, R., Cho, K., Courville, A., Salakhutdinov, R., Zemel, R. S., & Bengio, Y. (2015). Show, Attend and Tell: Neural Image Caption Generation with Visual Attention. *Proceedings of the 32nd International Conference on Machine Learning (ICML)*.

[2] Liu, H., & Brailsford, T. (2023). Reproducing “Show, Attend and Tell: Neural Image Caption Generation with Visual Attention”. *Journal of Physics: Conference Series, 2589*(1), 012012.
