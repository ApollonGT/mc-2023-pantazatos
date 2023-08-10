# ELECTRA Classifier and Explainability Scripts with SHAP and LIME

## ELECTRA Classifier

The provided code is for building a binary text classification model using the ELECTRA (Efficiently Learning an Encoder that Classifies Token Replacements Accurately) architecture for sentiment analysis on movie reviews. 

The code performs the following steps:

1. Importing Libraries and Installing Dependencies: The code begins by importing necessary libraries such as torch, transformers, sklearn, pandas, and more. It also installs the required dependencies using pip3 commands.
2. Loading and Preprocessing Data: The movie review dataset is loaded from a CSV file and preprocessed (the dataset without stopwords is recommended). The ratings are converted into binary labels (positive/negative sentiment) based on a predefined threshold.
3. Tokenization and Encoding: The ELECTRA tokenizer from the transformers library is used to tokenize and encode the reviews into token IDs and attention masks. These are essential inputs for the neural network model. The preprocessing function is defined to handle this task.
4. Splitting Data into Training and Validation Sets: The dataset is split into training and validation sets using train_test_split from sklearn. These sets are then transformed into TensorDataset and loaded into DataLoader objects for batch processing during training.
5. Model Initialization: The ELECTRA model (ElectraForSequenceClassification) is initialized with the pre-trained weights for the discriminator part. This model is designed for sequence classification tasks.
6. Training Loop: The code enters a loop for training the model. It iterates over the training data in batches, calculates loss, performs backpropagation, and updates model parameters using the AdamW optimizer.
7. Validation Loop: The model is evaluated on the validation set after each training epoch. Validation metrics like loss, accuracy, and F1 score are calculated. Early stopping is implemented to prevent overfitting.
8. Checkpointing: The model's state and optimizer's state are periodically saved as checkpoints during training. These checkpoints can be used to resume training or make predictions later.
9. Running on GPU (if available): The code checks for GPU availability and moves the model and data to the GPU if available. This accelerates the training process.

Technologies and Libraries Used:

1. PyTorch: Deep learning framework for building and training neural networks.
2. Transformers (Hugging Face): Library for working with pre-trained language models, including ELECTRA.
3. scikit-learn (sklearn): Library for machine learning tasks, including data splitting and evaluation metrics.
4. pandas: Library for data manipulation and analysis, used for loading and preprocessing the dataset.
5. numpy: Library for numerical computations.
6. tabulate: Library for creating formatted tables.
7. tqdm: Library for displaying progress bars during iterations.
8. CUDA (GPU): If available, the code utilizes GPUs for accelerated training.

Results:
After training, the code displays the training and validation losses, accuracy, and F1 score. It also checks if the validation loss has improved and implements early stopping if it hasn't improved for a certain number of epochs.

## XAI with SHAP

## XAI with LIME
