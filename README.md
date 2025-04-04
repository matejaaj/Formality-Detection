## Usage / Reproducing Results

### XLM-R Formality Classifier

To reproduce the evaluation results for the `xlmr_formality_classifier` model:

1. Open [Google Colab](https://colab.research.google.com/).
2. Import or upload the notebook located at:

   `/xlm-roberta/xlm-roberta.ipynb`

3. Run all

The notebook handles loading the model, running predictions on the evaluation dataset, and computing Spearman’s rank correlation.
The part that exports results to Google Drive has been commented out for convenience.

### Squinky Formality Classifier

To reproduce results using the **Squinky** classifier:

1. First, install **Miniconda** (I strongly suggest installing the same version, since I tested it on this). On Windows, you can install it using Chocolatey:

   ```bash
   choco install miniconda3 --version=4.5.4
   ```

2. Open Anaconda Prompt (recommended) and navigate to the squinky directory in this project.

3. Create the Conda environment using the provided squinky_env.yml file:

   ```bash
   conda env create -f squinky_env.yml
   ```

4. Activate the environment:

   ```
   conda activate squinky_env
   ```

5. Reinstall the following dependencies, as some versions may be overridden during environment creation due to `pip` being used when installing Squinky:

   ```bash
   conda install --force numpy=1.13.3 scipy=0.19.0 mkl=2017.0.4 scikit-learn=0.18.1
   ```

6. Once the environment is active and dependencies are fixed, you can run the evaluation script:

   ```bash
   python predict_squinky.py
   ```
