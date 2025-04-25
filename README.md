# ANI-1 Molecular Energy Prediction Pipeline
**A supervised ANN model trained on the ANI-1 dataset, completed as the final project for Chem C142 'Machine Learning, Statistical Models, and Optimization for Molecular Problems' (Prof. Teresa Head-Gordon), Spring 2025 @ UC Berkeley. Group work of Jae Won Kim and Yunmin Kim.**

## 🗒️ Project Synopsis

This endeavor constructs a robust deep learning pipeline to predict molecular energies from atomic configurations. By harnessing Atomic Environment Vectors (AEVs) and PyTorch-based artificial neural networks, we explore regularization techniques, perform hyperparameter optimization, and validate model performance.

## 📁 Repository Architecture

```
├── final_project.ipynb        # Comprehensive Jupyter Notebook
├── environment.yml           # Python Package Dependencies and Environment Settings
└── README.md                 # Project overview and usage instructions
```

## 📂 Data Preparation

1. **Environment Setup** All Python dependencies for this project are captured in the `environment.yml` file. To create and activate the environment, run:

   ```bash
      conda env create -f environment.yml
      conda activate ani
   ```
2. **Download** the ANI-1 dataset archive (`ani-1_dataset.tar.gz`) from Figshare.

   ```bash
   curl -L https://ndownloader.figshare.com/files/9057631 -o ANI1_release.tar.gz
   ```
4. **Merge** relevant subsets (s01–s04 or s01-s06) into a single HDF5 file:
5. **Invoke** the dataset loader within the notebook to apply self-energy corrections and species indexing.

## 🚀 Execution

All core data preparation, model construction, training loops, and evaluation are incorporated within `final_project.ipynb`. Launch the notebook and execute cells sequentially to:

- Initialize the AEV computer
- Load and preprocess the merged dataset
- Instantiate and train the model with chosen hyperparameters
- Visualize learning curves and performance metrics

## 🔍 Optimization Strategies

- **Regularization:** Dropout, L1, and L2 penalties to mitigate overfitting
- **Hyperparameter Tuning:** Grid search for learning rate, dropout rate, and regularization strengths
- **Cross-Validation:** True K-fold CV to ensure robustness and generalizability

## 🤝 Contributing

Jae Won Kim and Yunmin Kim contributed equally. 

