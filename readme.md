# Feature Selection Using Genetic Algorithm on RAVDESS Facial Landmark Tracking Dataset

## Project Overview

This project implements feature selection using a Genetic Algorithm (GA) on the RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song) Facial Landmark Tracking dataset. The goal is to enhance a neural network's ability to classify emotions by selecting the most discriminative facial landmarks.

## Background

The RAVDESS dataset contains tracked facial landmark movements, allowing for the classification of various emotional expressions. For this project, we focus on two emotions, "happy" and "sad," and employ a GA to iteratively select the most relevant facial landmarks, improving the classification accuracy of a neural network.

## Tasks

### 1. Data Preparation

1. **Acquire the RAVDESS Facial Landmark Tracking dataset**:
    - Download from [Kaggle](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-facial-landmark-tracking) or [Zenodo](https://zenodo.org/records/3255102).
2. **Extract relevant data**:
    - Extract data entries corresponding to speech (modality code 03) and emotions happy (emotion code 03) and sad (emotion code 04).

### 2. Feature Selection Using Genetic Algorithm

1. **Implement a Genetic Algorithm for feature selection**:
    - Define a chromosome to represent a subset of facial landmarks (e.g., binary string where 1 indicates a selected landmark and 0 excludes it).
    - Implement selection (e.g., roulette wheel), crossover (e.g., single-point), and mutation operators for the GA.
    - Set termination conditions for the GA (e.g., 150-200 iterations).
    - Conduct experiments using different configurations of the GA (e.g., population size, mutation rate).

2. **Evaluate the effectiveness of feature selection**:
    - Measure the classification accuracy of the neural network with the selected features.

### 3. Document

1. **Explain the chromosome representation and genetic operators used in the GA**.
2. **Present the performance evaluation results for the final model**.
3. **Analyze the impact of feature selection on model performance and the features selected by the GA**.

## Dataset Details

### Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)

- Contains 7356 files (24.8 GB).
- Includes 24 professional actors (12 female, 12 male) vocalizing two lexically-matched statements.
- Emotions: calm, happy, sad, angry, fearful, surprise, disgust.
- Formats: Audio-only, Audio-Video, Video-only.

### Facial Landmark Tracking Data

- Produced by OpenFace 2.1.0.
- Includes facial landmark detection, head pose estimation, facial action unit recognition, and eye-gaze estimation.

## File Naming Convention

- Example: `02-01-06-01-02-01-12.mp4`
    1. Modality: 01 = full-AV, 02 = video-only, 03 = audio-only
    2. Vocal channel: 01 = speech, 02 = song
    3. Emotion: 01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised
    4. Emotional intensity: 01 = normal, 02 = strong
    5. Statement: 01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door"
    6. Repetition: 01 = 1st repetition, 02 = 2nd repetition
    7. Actor: 01 to 24 (odd numbered actors are male, even numbered actors are female)

## RAVDESS Facial Landmark Tracking

- Tracking results for each trial are provided as individual CSV files.
- Columns include timing and detection confidence, eye gaze detection, head pose, facial landmarks locations (2D and 3D), rigid and non-rigid shape parameters, and facial action units.

## Neural Network for Fitness Function

A basic neural network can be used for evaluating the fitness function of the GA. The network architecture includes several dense layers with ReLU activation, ending with a softmax layer for classification.

## References

- RAVDESS Dataset: [Zenodo](https://zenodo.org/records/1188976)
- Facial Landmark Tracking Data: [Zenodo](https://zenodo.org/records/3255102)

## How to Run

1. **Clone the repository**:
    ```bash
    git clone https://github.com/mahad002/Feature-Selection.git
    ```
2. **Navigate to the project directory**:
    ```bash
    cd Feature-Selection
    ```


## Results

The results of the feature selection process, including the performance evaluation and selected features, will be documented and analyzed in the final report. The impact of feature selection on model performance will be discussed, highlighting the benefits of using a GA for this task.
