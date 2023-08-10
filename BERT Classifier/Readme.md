# BERT Classifier and Explainability Scripts with SHAP and LIME

## BERT Classifier

The provided code is for building a binary text classification model using the BERT (Bidirectional Encoder Representations from Transformers) architecture for sentiment analysis on movie reviews. 

The code performs the following steps:

1. Importing Libraries and Installing Dependencies: The code begins by importing necessary libraries such as torch, transformers, sklearn, pandas, and more. It also installs the required dependencies using pip3 commands.
2. Loading and Preprocessing Data: The movie review dataset is loaded from a CSV file and preprocessed (the dataset without stopwords is recommended). The ratings are converted into binary labels (positive/negative sentiment) based on a predefined threshold.
3. Tokenization and Encoding: The BERT tokenizer from the transformers library is used to tokenize and encode the reviews into token IDs and attention masks. These are essential inputs for the neural network model. The preprocessing function is defined to handle this task.
4. Splitting Data into Training and Validation Sets: The dataset is split into training and validation sets using train_test_split from sklearn. These sets are then transformed into TensorDataset and loaded into DataLoader objects for batch processing during training.
5. Model Initialization: The BERT model (BertForSequenceClassification) is initialized with the pre-trained weights for the discriminator part. This model is designed for sequence classification tasks.
6. Training Loop: The code enters a loop for training the model. It iterates over the training data in batches, calculates loss, performs backpropagation, and updates model parameters using the AdamW optimizer.
7. Validation Loop: The model is evaluated on the validation set after each training epoch. Validation metrics like loss, accuracy, and F1 score are calculated. Early stopping is implemented to prevent overfitting.
8. Checkpointing: The model's state and optimizer's state are periodically saved as checkpoints during training. These checkpoints can be used to resume training or make predictions later.
9. Running on GPU (if available): The code checks for GPU availability and moves the model and data to the GPU if available. This accelerates the training process.

Technologies and Libraries Used:

1. PyTorch: Deep learning framework for building and training neural networks.
2. Transformers (Hugging Face): Library for working with pre-trained language models, including BERT.
3. scikit-learn (sklearn): Library for machine learning tasks, including data splitting and evaluation metrics.
4. pandas: Library for data manipulation and analysis, used for loading and preprocessing the dataset.
5. numpy: Library for numerical computations.
6. tabulate: Library for creating formatted tables.
7. tqdm: Library for displaying progress bars during iterations.
8. CUDA (GPU): The code utilizes GPUs for accelerated training if available.

Results:
After training, the code displays the training and validation losses, accuracy, and F1 score. It also checks if the validation loss has improved and implements early stopping if it hasn't improved for a certain number of epochs. The model output after each epoch and the final checkpoint are available in the following link:

https://drive.google.com/drive/folders/1LFbRj7WMOoHZOszROxTXRrQvUZBG3vnT?usp=sharing

## XAI with SHAP

The code provided focuses on prediction and explainability using SHAP with an BERT model for sentiment analysis on movie reviews. The code demonstrates how to use SHAP with the pre-trained BERT model to predict sentiment and provide SHAP value visualizations for movie reviews in an interactive manner. Users can input their own movie reviews, trigger the prediction and explanation process, and view the SHAP value plots using the provided widgets.

The code performs the following steps:

1. Installing Required Libraries: The code installs necessary libraries using pip3 commands, including torch, transformers, shap, xformers, ipywidgets, scipy, pandas, and numpy.
2. Loading Required Libraries: The required libraries are imported, including shap for SHAP explainability, transformers, pandas, torch, numpy, scipy, ipywidgets for interactive widgets, and display and clear_output from IPython.display.
3. Prediction and Explainability using SHAP: The code sets up the environment, loads the pre-trained BERT model, tokenizer, and dataset. It preprocesses the text data for prediction and creates a SHAP explainer based on a pipeline created with the transformers.pipeline function.
4. Custom Review Widget: The code creates an interactive widget using ipywidgets to allow users to input custom movie reviews. A button triggers the execution of the prediction and explanation process, and the output is displayed below the input field.
5. Execution Loop: The code iterates through a subset of movie reviews from the dataset. For each review, it calls the score_and_visualization function to predict sentiment and generate SHAP values. The prediction result and SHAP visualization are displayed using the print() function and shap.plots.text().
6. Button Click Function: The function defined for the button click event clears the output cell, retrieves the user-input movie review, performs prediction, generates SHAP values, and displays the prediction and SHAP visualization.
7. Interactive Interface: The input box for the movie review, button, and output box are organized using ipywidgets to create an interactive interface. Users can input their own movie reviews, trigger the prediction and explanation process, and view the results.

Technologies and Libraries Used:

1. SHAP: A library for explaining machine learning models' predictions using Shapley values.
2. transformers: A library by Hugging Face for working with pre-trained language models, including BERT.
3. pandas: A library for data manipulation and analysis.
4. torch: The PyTorch library for building and training neural networks.
5. numpy: A library for numerical computations.
6. scipy: A library for scientific and technical computing.
7. ipywidgets: A library for creating interactive widgets in Jupyter notebooks.
IPython.display: A module for displaying rich media in the IPython environment.

## XAI with LIME

The code provided focuses on prediction and explainability using LIME with a BERT model for sentiment analysis on movie reviews. The code demonstrates how to use LIME with the pre-trained BERT model to predict sentiment and interactively provide explanations for movie reviews. Users can input movie reviews, trigger the prediction and explanation process, and visualize the results using the widgets.

The code performs the following steps:

1. Installing Required Libraries: The code begins by installing necessary libraries using pip3 commands, including torch, transformers, lime, xformers, ipywidgets, scipy, pandas, and numpy.
2. Loading Required Libraries: Required libraries are imported, including lime for LimeTextExplainer, transformers, pandas, torch, numpy, ipywidgets for interactive widgets, and display and clear_output from IPython.display.
3. Prediction and Explainability using LIME: The code sets up the environment and loads the pre-trained BERT model, tokenizer, and dataset. It preprocesses the text data for prediction and implements functions for prediction and LIME-based explanation.
4. Custom Review Widget: The code creates an interactive widget using ipywidgets to allow users to input custom movie reviews. A button triggers the execution of the prediction and explanation process, and the output is displayed below the input field.
5. Execution Loop: The code iterates through a subset of movie reviews from the dataset. For each review, it predicts sentiment using the BERT model and generates an explanation using LIME. The prediction result and explanation are displayed using the .show_in_notebook() method. The explanations are also saved to an HTML file.
6. Button Click Function: The function defined for the button click event clears the output cell, retrieves the user-input movie review, performs prediction, and generates an explanation. The prediction and explanation results are displayed using the .show_in_notebook() method and saved to an HTML file.
7. Interactive Interface: The movie review, button, and output box's input box are organized using ipywidgets to create an interactive interface. The interface allows users to input movie reviews, trigger prediction, explanation, and view the results.

Technologies and Libraries Used:

1. LIME: A library for explaining machine learning models' predictions.
2. transformers: A library by Hugging Face for working with pre-trained language models, including BERT.
3. pandas: A library for data manipulation and analysis.
4. torch: The PyTorch library for building and training neural networks.
5. numpy: A library for numerical computations.
6. ipywidgets: A library for creating interactive widgets in Jupyter notebooks.
7. IPython.display: A module for displaying rich media in the IPython environment.
