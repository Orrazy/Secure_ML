# Privacy-Preserving Biometric Identification Using Homomorphic Encryption

## 1. Project Overview

This project demonstrates an academic exploration into privacy-preserving biometric identification using Fully Homomorphic Encryption (FHE). The system focuses on computing similarity scores between facial embeddings in an encrypted space, ensuring user privacy. Through extensive experiments, including nearest-neighbor attack simulations, the project validates the robustness of FHE in preventing identity leakage.

## 2. Key Features

- Extraction of facial embeddings using the GhostFaceNet model and DeepFace.
- Encryption of embeddings using the CKKS homomorphic encryption scheme.
- Nearest-neighbor attack simulation on cleartext and encrypted data.
- Evaluation of attack success rates and suppression of high-confidence matches using encryption.

## 3. Installation and Setup

**_NOTE:_**  
If running locally, set up the environment as follows:  

```bash
# Create and activate the conda environment
conda create -y --name Project_in_secure_ml python=3.9 
conda activate Project_in_secure_ml

# Install necessary Jupyter kernel
conda install ipykernel
python -m ipykernel install --user --name Project_in_secure_ml --display-name "Python 3.9 (Project_in_secure_ml)"
```

Once the environment is ready, you can connect to the project using Jupyter Notebook or Visual Studio Code.

## 4. Running the Experiments

The entire workflow, including data preparation, embedding extraction, encryption, and attack simulation, is documented step-by-step in the Jupyter Notebook. Simply follow the instructions within the notebook to reproduce the results.

## 5. Project Structure

The project directory is structured as follows:

``` dir
/project-root
    ├── prepare_data.py            # Script to extract and store embeddings
    ├── main.ipynb                 # Jupyter notebook with full experimental details
    └── Final report/              # Final report in PDF and LaTeX
        └── /elements/             # Visualizations and report-related images
```

## 6. Results Summary

### Nearest-Neighbor Attack Success Rates

- Cleartext Data: 0%
- Encrypted Data: 0%

### Overall Performance Metrics

| Metric                           | Value   |
| -------------------------------- | ------- |
| Embedding generation (sec)       | 621.85  |
| Cleartext similarity computation | 16.03   |
| Encrypted similarity computation | 8622.54 |
| Encryption time (sec)            | 7.67    |
| Average top-10 match percentage  | 96.68%  |
| Size of encrypted scores (MB)    | 10.80   |

The results demonstrate the feasibility of using FHE for privacy-preserving biometric systems, though optimizations are needed to reduce computational overhead.

### Visualization

![distribution of similarity scores across the cleartext and encrypted scenarios](<Final report/elements/nearest_neighbor_attack_with_high_scores.png>)
The following plot shows the distribution of similarity scores across the cleartext and encrypted scenarios, emphasizing the suppression of high-confidence scores in the encrypted version.

## 7. References and Acknowledgments

This project would not have been possible without the following resources:

- GhostFaceNet: The lightweight model used for facial embeddings.
- DeepFace: Framework for embedding extraction.
- MS1M-ArcFace Dataset: The dataset used for robust performance evaluation.
- Special thanks to Adi Akiva for support and guidance throughout the project.

## 8. License

This project is intended for academic use and may not be distributed without permission.