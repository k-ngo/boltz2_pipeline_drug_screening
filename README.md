# 🧬 Boltz-2 Pipeline for Pharmacogenomic Screening

Welcome to our interactive platform for rapid, deep learning-driven pharmacogenomic analysis. This tool, implemented as a Google Colab notebook, leverages the power of the **Boltz-2 structure prediction model** to assess how genetic mutations affect drug binding. It provides an end-to-end solution for researchers in computational biology, pharmacology, and precision medicine. This repository contains the open-source code to replicate our findings and to use this tool for your own research.

Click here to visit the notebook on Google Colab: 
<a target="_blank" href="https://colab.research.google.com/drive/1tUon8MrjdjtpE6pSUMcGQ86WYWqXCIBn?usp=sharing">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

---

## 🔬 Key Features

- **State-of-the-Art Structure Prediction**: Utilizes Boltz-2 to generate high-quality 3D structures of protein-ligand complexes from sequence alone.  
- **Automated Mutation Discovery**: Queries the UniProt database to automatically find known mutations for your protein of interest and predicts their functional impact.  
- **Comprehensive Screening Modes**:
  - *Protein-Drug Screening*: Test a panel of drugs against one or more proteins.  
  - *Mutation-Drug Screening*: Evaluate the effect of specific mutations on the binding of one or more drugs.  
  - *Structure-Only Mode*: Predict the structure of a protein without a ligand.  
- **Flexible and Customizable**: Supports multi-chain proteins, essential co-factors, post-translational modifications, and advanced modeling constraints.  
- **Interactive Visualization**: Includes an integrated 3D molecular viewer and a suite of plots to analyze binding affinity and structural quality metrics.  
- **Accessible and Reproducible**: Packaged in a user-friendly Google Colab notebook that requires no local installation.  

---

## 🚀 Getting Started: A Quick Tutorial

This tool is designed to be run in Google Colab. Follow these steps to perform your first screening.  

---

### Step 1: Open and Configure the Notebook

1. **Open the Notebook**: Click the "Open in Colab" badge at the top of this page.  
2. **Run the Setup Cell**: The first cell in the notebook (*1️⃣ 🔧 Installation & Setup*) will install all necessary dependencies. Simply run it and wait for it to complete.  

---

### Step 2: Provide Your Inputs

The second cell (*2️⃣ 📱 Basic Input Configuration*) is where you will define your experiment.  

- **Choose Your Mode**:  
  - *Protein-Drug Screening – Manual Protein Entry*: To test one protein against many drugs. Paste your protein's amino acid sequence directly.  
  - *Protein-Drug Screening – Upload FASTA File*: To test multiple proteins. Upload a FASTA file containing their sequences.  
  - *Mutants-Drug Screening*: To study how mutations affect drug binding. Provide the wild-type sequence.  

- **(For Mutation Screening) Discover and Specify Mutations**:  
  - Check the *Discover mutations from databases* box to automatically search UniProt for known variants of your protein.  
  - After running the cell, a list of suggested mutations will be printed. Copy and paste the mutations you want to test into the *Mutations input box* (e.g., `Y652A`, `F656A`, `V625A`).  

- **Provide Ligands (Drugs)**:  
  - In the *Ligand SMILES Input* section, enter the SMILES strings for your drugs, separated by semicolons (e.g., `CCO;CCN;CC(C)O`).  
  - You can also provide a name for each (e.g., `Ethanol,CCO;Ethylamine,CCN`).  

---

### Step 3: Set Advanced Parameters (Optional)

The third and fourth cells (*3️⃣ ⚙️ Additional Parameters* and *4️⃣ 🚀 Configure Computational Settings*) allow for fine-tuning. For most users, the default settings are sufficient. Here you can:  

- Add biological co-factors like ATP or NAD.  
- Define a specific binding pocket to guide the prediction.  
- Adjust computational parameters like sampling steps to balance speed and accuracy.  

---

### Step 4: Run the Prediction

Execute the fifth cell (*5️⃣ 🌠 Run Structure Predictions*). This is the main computational step and may take several minutes per protein-drug pair (typically 3–5 minutes). The notebook will print progress updates for each prediction.  

---

### Step 5: Visualize and Download Your Results

The final cell (*6️⃣ 📊 Visualize Results & 3D Structures*) will display the output of your screening. You will see:  

- **Interactive Plots**: Scatter plots of binding affinity vs. confidence, and distributions of key quality metrics.  
- **A Results Table**: A summary of the predicted pIC50 values and confidence scores for each complex.  
- **3D Structures**: An interactive 3D viewer showing the predicted structures of your top protein-ligand complexes.  

All results, including the 3D structure `.pdb` files, will be saved and can be downloaded.  
