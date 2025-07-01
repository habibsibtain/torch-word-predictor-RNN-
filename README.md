# Sherlock Holmes Text Generation with PyTorch

This project demonstrates how to train a Recurrent Neural Network (RNN) using PyTorch to generate text in the style of "Sherlock Holmes". The model is trained on the contents of `Sherlock Holmes.txt` and can predict the next word(s) given a seed phrase.

## Project Structure

- `model.ipynb` — Jupyter notebook with all code, cell by cell.
- `Sherlock Holmes.txt` — Training text file.
- `requirements.txt` — List of Python dependencies.

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd rnn
```

### 2. (Optional) Create and Activate a Virtual Environment

```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### 3. Install Dependencies

Install all required packages using:

```bash
pip install -r requirements.txt
```

**Key dependencies for this project:**
- torch
- numpy
- pandas
- jupyter

### 4. Add the Training Text

Ensure `Sherlock Holmes.txt` is present in the project directory. You can use any large text file for training, but the notebook expects this filename.

### 5. Run the Notebook

Start Jupyter Notebook:

```bash
jupyter notebook model.ipynb
```

Or, if you use VS Code, open the notebook interface and run the cells.

---

## Step-by-Step Usage

1. **Text Preprocessing:**  
   The notebook reads and tokenizes the text, cleans it, and builds a vocabulary.

2. **Sequence Creation:**  
   It creates sequences of words for training the RNN, mapping each word to an integer index.

3. **Dataset Preparation:**  
   The sequences are converted into PyTorch tensors and loaded into a DataLoader for batching.

4. **Model Definition:**  
   An RNN model is defined using PyTorch's `nn.Module`, with embedding, RNN, and linear layers.

5. **Training:**  
   The model is trained using cross-entropy loss and the Adam optimizer. Training progress is printed for each epoch.

6. **Text Generation:**  
   After training, you can generate new Sherlock Holmes-style text by providing a seed phrase to the prediction function.

---

## Example: Generate Text

After training, try generating text:

```python
seed = "To Sherlock Holmes she is a"
print(predict_next_word(model, seed, n_words=100))
```

---

## Requirements

- Python 3.7+
- torch
- numpy
- pandas
- jupyter

All dependencies are listed in `requirements.txt`.

---

## License

This project is for educational purposes.
