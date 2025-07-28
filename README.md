# Supporting-materials-Vector-Based-Analysis-of-Phonetic-Iconicity-in-SDAs
Supplementary materials for the revisions of a paper submitted for publication.
Phonological Analysis Pipeline - README  
1. Overview
This project automates phonological feature analysis through an enhanced pipeline that processes vowel and consonant data. The workflow progresses sequentially from feature extraction to dimensionality reduction and visualization, covering both basic and filtered analysis stages for vowels and consonants, now including trustworthiness evaluation of dimensionality reduction methods before concluding with spatial visualizations.

2. Workflow Description
The pipeline begins with vowel basic processing: counting phonological features, performing initial PCA, and fitting planes. Next, vowel-filtered processing constructs language matrices, runs filtered PCA, optimizes plane fitting, analyzes feature contributions, and generates heatmaps. Consonant processing follows the same two-stage pattern: basic processing for feature counting, PCA, and plane fitting, then filtered processing for matrix creation, filtered PCA, optimized plane fitting, contribution analysis, and heatmap generation. A crucial trustworthiness evaluation stage then assesses the reliability of different dimensionality reduction methods using established metrics (In the actual operation, when selecting the data processing method, the reliability of different dimension reduction methods will be evaluated after the word pair vector is obtained, but in order to facilitate the repeated implementation of the workflow, it is placed here). The workflow concludes with post-processing spatial visualizations.

3. Directory Structure
Main components include the Tool directory containing all analysis scripts, the run_all.py pipeline controller, and the Data directory, which houses Input (raw phonological data) and Output (generated results) subdirectories.

4. Requirements
Python 3.8+
Libraries: numpy, pandas, scipy, scikit-learn, matplotlib, seaborn, xlsxwriter, joblib, umap-learn, 

5. Usage
Execute the complete pipeline by running: `python run_all.py`.

6. Output Information
All results are saved to Data/Output/ including PCA variance plots, fitted plane visualizations, feature contribution heatmaps, dimensionality reduction trustworthiness metrics, spatial distribution plots, and language matrices in CSV format.
