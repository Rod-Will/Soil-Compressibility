# Soil Compressibility Prediction Using AI

This repository focuses on leveraging artificial intelligence to predict two critical parameters in geotechnical engineering: the **Compression Index** and the **Swelling Index**. Accurate prediction of these indices aids in understanding soil behavior under varying conditions, optimizing construction projects, and mitigating risks.

## Overview

This project integrates advanced AI/ML models to:

- Predict the **Compression Index (Cc)** and **Swelling Index (Cs)** based on soil properties.
- Enhance decision-making in civil engineering projects by providing reliable soil compressibility metrics.
- Improve efficiency by reducing the dependency on extensive laboratory tests.

The models are trained on high-quality datasets using features like soil type, moisture content, void ratio, and other geotechnical parameters.

## Features

- **Data Preprocessing**: Includes handling missing values, feature scaling, and encoding of categorical variables.
- **AI/ML Models**: Utilizes advanced machine learning algorithms for accurate predictions.
- **Model Persistence**: Saves the best-performing model using `joblib` for future use.
- **Interactive GUI (Optional)**: Visualize predictions with a user-friendly interface.

## Repository Structure

```plaintext
.
├── data/                   # Raw and processed datasets
├── notebooks/              # Jupyter notebooks for data exploration and model training
├── results/                # Trained models and performance metrics
├── src/                    # Source code for preprocessing, model training, and evaluation
├── tests/                  # Unit tests for codebase validation\
├── README.md               # Project documentation
```

## Installation

### Prerequisites

Ensure you have the following installed:

- Python 3.8+
- Required libraries (listed in `requirements.txt`)

### Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/soil-compressibility-ai.git
   ```

2. Navigate to the project directory:
   ```bash
   cd soil-compressibility-ai
   ```

3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Training the Model

1. Prepare your dataset and place it in the `data/` directory.
2. Run the training script:
   ```bash
   python src/train_model.py
   ```
3. The best model will be saved in the `results/models/` directory:
   ```plaintext
   results/models/{target_variable}_{name}_best.pkl
   ```

### Making Predictions

Use the saved model to make predictions:
```python
from joblib import load

model_path = "results/models/compression_index_best.pkl"
model = load(model_path)

# Example input features
input_features = {
    "moisture_content": 18,
    "void_ratio": 0.8,
    "soil_type": "Clay",
    "other_features": ...
}

# Make prediction
predicted_value = model.predict([list(input_features.values())])
print(f"Predicted Compression Index: {predicted_value[0]}")
```

## Contributing

We welcome contributions to this project! To get started:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Make your changes and commit:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

## License

This project is licensed under the Creative Commons Zero v1.0 License. See the [LICENSE](LICENSE) file for details.

## References

- Standard geotechnical engineering textbooks.
- Research papers on soil compressibility and AI/ML applications.
- Datasets from reliable sources in geotechnical engineering.

---

**Designed by Rod-Will**  
Empowering innovation in engineering through AI.
Contact via rhudwill@gmail.com

