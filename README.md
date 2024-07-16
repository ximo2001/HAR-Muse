# HAR-Muse
Project about Human Activity Recognition using a low budget device (Muse S). Currently working with Machine Learning algorithms to analyze EEG data and distinguish between various activities.

## Project Structure

### `DATA` Folder
This folder contains the EEG recordings used in the experiment, as well as the extracted features, which are used to train the machine learning models.

- **`featuresExtended/`**: Contains CSV files with the extracted features from the EEG recordings for each of the windows studied.
  - `features_1.csv`
  - `features_2.csv`
  - `features_3.csv`
  - `features_4.csv`

- **`MusePreprocessedTOTAL/`**: Includes the preprocessed EEG recordings in CSV format.
  - `10_1_c1.csv`, `10_1_c2.csv`, `10_1_c3.csv`, ..., `30_2_m3.csv`
  
### `EXPERIMENTO` Folder
Folder containing all data used to perform the experiments.

### `SOFTWARE` Folder
This folder contains the scripts and notebooks used for data preprocessing, feature extraction, and the execution and evaluation of the machine learning models.

#### `AUXILIAR` Subfolder
Contains the files for data preprocessing and feature extraction, as well as the code for result evaluation.

- `FeatureExtraction.ipynb`: Notebook for feature extraction.
- `Preprocesado.ipynb`: Notebook for data preprocessing.
- `RESULTADOS.ipynb`: Notebook for obtaining and analyzing results.

#### `MULTICLASE` Subfolder
This folder contains data and scripts related to the multiclass experiment, aimed at distinguishing between four activities.

- **`MODELOS/`**: Contains notebooks for grid search of the basic models.
  - `ADABOOST.ipynb`, `CATBOOST.ipynb`, `EXTRATREE.ipynb`, ..., `XGBOOST.ipynb`
  - `tabnet.txt`: Text file with information related to TabNet's parameters.

- `MODELOS_BASICOS.ipynb`: Notebook with the execution of the basic models.
- `parametros.txt`: File with the parameters used in the basic models.
- **`results/`**: Folder that stores the confusion matrices resulting from executing each model, as well as TXT and CSV files with comparative information.
  - `conf_matrix_1_AdaBoost_37.csv`, `conf_matrix_1_CatBoost_41.csv`, ..., `RESULTSVOTING.txt`

- **`resultsEXTRA/`**: Contains additional tests conducted with the most optimal algorithm, Random Forest.
  - `conf_matrix_1_Random Forest_130.csv`, ..., `RESULTS.csv`

- **`resultsIGUALADOS/`**: Stores one execution per window for each model. This was done in order to give a fair comparison.
  - `analisis.txt`, `conf_matrix_1_AdaBoost_37.csv`, ..., `windows.txt0`

- `STACKING.ipynb`: Notebook with the execution of stacking meta-model.
- `VOTING.ipynb`: Notebook with the execution of voting meta-model.

#### `MEDITACION_MATEMATICAS` Subfolder
Includes files related to the analysis of the binary problem of meditation with mathematics.

- `BINARIOMATES.ipynb`: Notebook with the optimal execution of Random Forest for this problem.
- **`resultsBINMATES/`**: Results folder with confusion matrices and execution times.
  - `conf_matrix_1_Random Forest_116.csv`, ..., `RESULTS.csv`

#### `MUSICA-MEDITACION` Subfolder
Contains files related to the analysis of the binary problem of music and meditation.

- `BINARIOMUSICA.ipynb`: Notebook with the optimal execution of Random Forest for this problem.
- **`resultsBINMUSICA/`**: Results folder with confusion matrices and execution times.
  - `conf_matrix_1_Random Forest_123.csv`, ..., `RESULTS.csv`


