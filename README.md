# QML_Tomography_QCG

## Project Documentation

### Overview
This repository contains the implementation of Quantum Machine Learning (QML) techniques for quantum tomography using QCG (Quantum Computing in Python). The objective is to develop methods that effectively reconstruct quantum states from measurement data.

### Methodology
- **Data Collection**: Gather raw measurement data from quantum experiments.
- **State Reconstruction**: Utilize various algorithms like Maximum Likelihood Estimation and Bayesian inference to reconstruct quantum states.
- **Evaluation Metrics**: Measure the performance of the reconstruction methods using fidelity and trace distance.

### Implementation Details
- **Dependencies**: 
  - Qiskit
  - NumPy
  - Pandas
  - Matplotlib

- **Key Modules**:
  - `data_collection.py`: Module for fetching and processing measurement data.
  - `state_reconstruction.py`: Contains functions for the reconstruction algorithms.
  - `evaluation.py`: Implements evaluation metrics to assess the reconstructed states.

### Results
- **Fidelity Evaluation**: The average fidelity across various tests was found to be greater than 0.9, indicating a high accuracy in state reconstruction. 
- **Trace Distance**: The calculated trace distances varied, with the best-performing methods showing values significantly below the upper threshold of 0.5.

### Conclusions
The methodologies applied in this project demonstrate effective quantum state reconstruction capabilities. Future work may involve exploring deeper machine learning models to enhance performance further.

### Getting Started
1. Clone this repository:
   ```bash
   git clone https://github.com/ShivanshSrivastava2006/QML_Tomography_QCG.git
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the scripts to start data collection and state reconstruction:
   ```bash
   python data_collection.py
   python state_reconstruction.py
   ```

### Author
Shivansh Srivastava

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.