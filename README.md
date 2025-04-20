# Image Captioning with Flicker8k

This project implements an image captioning model using the Flicker8k dataset, TensorFlow/Keras, and a pre-trained InceptionV3 model for feature extraction.

## Project Structure

- `image_captioning_flicker8k.ipynb`: The main Jupyter Notebook containing the code for data loading, preprocessing, model building, training, and inference.
- `flicker8k/`: Directory containing the Flicker8k dataset (images and captions). **Note:** This directory is included in `.gitignore` and should be downloaded separately.
- `image_features_inceptionv3.pkl`: Saved image features extracted by InceptionV3.
- `tokenizer.pkl`: Saved Keras Tokenizer object.
- `max_length.pkl`: Saved maximum caption length.
- `final_caption_model.weights.h5`: Saved weights of the trained model.
- `.gitignore`: Specifies intentionally untracked files that Git should ignore.
- `README.md`: This file.

## Setup

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd another-image-captioning
    ```
2.  **Download the Flicker8k dataset:**
    - Download the dataset from a source like Kaggle or the original provider.
    - Extract the contents into the `flicker8k/` directory. Ensure you have `flicker8k/Images/` and `flicker8k/captions.txt`.
3.  **Create a virtual environment (optional but recommended):**
    ```bash
    python -m venv image_captioning_env
    source image_captioning_env/bin/activate # On Windows use `image_captioning_env\Scripts\activate`
    ```
4.  **Install dependencies:**
    ```bash
    pip install tensorflow numpy pandas Pillow tqdm scikit-learn matplotlib jupyterlab
    ```

## Usage

1.  **Start JupyterLab:**
    ```bash
    jupyter lab
    ```
2.  **Open and run the notebook:** Open `image_captioning_flicker8k.ipynb` and run the cells sequentially.
    - The notebook will:
        - Load and preprocess captions.
        - Load pre-extracted image features (`image_features_inceptionv3.pkl`) or extract them if the file doesn't exist.
        - Build the captioning model.
        - Load pre-trained weights (`final_caption_model.weights.h5`) or train the model if the file doesn't exist.
        - Generate captions for sample images.

## Notes

- The dataset (`flicker8k/`), virtual environment (`image_captioning_env/`), generated `.pkl`, `.keras`, and `.weights.h5` files are ignored by Git (see `.gitignore`).
- Ensure you have sufficient disk space for the dataset and extracted features.
- Training can take a significant amount of time depending on your hardware.
