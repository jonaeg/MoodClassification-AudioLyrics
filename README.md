# Mood Classifier based on Audio and Lyrics of Songs

## Overview

This project aims to classify songs into four moods (Angry, Happy, Sad, Relaxed) based on their lyrics and audio features. It uses SVM classifiers to make predictions from the features, then employs meta-models that leverage confidence values from both lyrics and audio predictions to enhance accuracy.

A holistic perspective on the project is offered with the slides `MoodClassification-AudioLyrics_slides.pdf`
### Structure

- **`0_database`**: Contains scripts for feature extraction from lyrics and audio, database generation, data preprocessing and train/test splitting. The lyrics embedding process is optimized for Google Colab's GPU.

- **`1_classifier`**: Includes code for training SVM models on audio and lyrics features, followed by meta-models to improve prediction outcomes. 

### Getting Started

1. **Setup**: Clone the repository and install dependencies listed in `requirements.txt`.

   ```bash
   pip install -r requirements.txt
   ```

2. **Data Preparation**: Run notebook in `0_database/GenerationDatabase.ipynb` to prepare your data. If you want to recalculate the features look into the notebooks `0_Database/feature_extraction_audio.ipynb` and `0_database/feature_extraction_lyrics.ipynb`

3. **Model Training**: Copy folder `0_Database/database` to `1_classifier` and run the notebooks `1_classifier/Audio_Model.ipynb` and `1_classifier/Lyrics_Model.ipynb` to train the Audio and Lyrics models, which are saved to the folder `1_classifier/models`. For an overview over different combined models consult `1_classifier/Bimodel.ipynb`.

4. **Data analysis**: The folder **`2_DataAnalysis`** contains the notebook **`Analysis.ipynb`** for the data analysis. To run the data analysis notebook with the trained models, copy the **`models`** instance from **`1_classifier`** after training the models into **`2_DataAnalysis`** .
