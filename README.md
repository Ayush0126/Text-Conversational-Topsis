# TOPSIS for Conversational AI Model Evaluation

## Overview
This project implements the **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** method to rank conversational AI models based on multiple performance metrics. The script normalizes data, applies weighting, computes TOPSIS scores, and generates visualizations for analysis.

## Features
- **Normalization**: Uses Min-Max Scaling to normalize model scores.
- **Weighted Decision Matrix**: Applies user-defined weights to criteria.
- **TOPSIS Calculation**: Computes distances to ideal best and worst solutions.
- **Ranking**: Assigns a rank to each AI model based on TOPSIS scores.
- **Visualization**: Generates bar plots for easy comparison.
- **Data Export**: Saves results to a CSV file.

## Installation
Ensure you have Python installed along with the following dependencies:
```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

## Usage
1. **Prepare Data:** Update the `data_conversational` DataFrame with model evaluation metrics.
2. **Adjust Weights:** Modify `weights_conversational` to change criteria importance.
3. **Run Script:** Execute the Python script to compute and visualize rankings.
4. **Check Output:** The results are saved in `results_conversational.csv` and displayed as plots.

## Example Criteria
The evaluation metrics used for ranking models:
- **BLEU Score**: Measures translation quality (higher is better).
- **Response Coherence**: Assesses logical flow (higher is better).
- **Diversity**: Measures response variability (higher is better).
- **Latency**: Measures response time (lower is better).

## Expected Output
- **CSV File (`results_conversational.csv`)**: Contains TOPSIS scores and ranks.
- **Graphical Visualization**: A bar plot showing model rankings.
- **Normalized Data Table**: Displays transformed and weighted values.

## Troubleshooting
- **Shape Mismatch Error?** Ensure that the weight array matches the number of selected criteria.
- **Incorrect Ranking?** Double-check that lower-is-better criteria (e.g., latency) are handled correctly.

## License
This project is open-source and available under the MIT License.
