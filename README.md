# CNN_timeseries_forecast

Timesiries forecasting using Convolutional neural network (CNN).

# Daily Female Births Dataset

This dataset describes the number of daily female births in California in 1959. The units are a count and there are 365 observations. The source of the dataset is credited to Newton (1988).

Below is a plot of the entire dataset.

<img src="img/Daily-Female-Births-Dataset.png" width="700"/>

Dataset has two columns: Date and Births.

<img src="img/dataset_columns.png" width="400"/>

# Dataset Split

Training dataset will have 55 percent of the data (200 observations).
Validation dataset will have 45 percent of the data (165 observations).

<img src="img/data_split.png" width="400"/>

To make this task a supervised learning task we need to split our data to sequences. To predict next observation we will use previous three observation.

# CNN Forecast Model

Inside our model we will have one 1D convolution layer with 3 input channels and 64 output channels. Then we will have activation function ReLU and 2 fully connected layers. Output is gonna be one number (prediction).

<img src="img/cnn.png" width="400"/>

We will use optimizer Adam and loss function MSE.

<img src="img/optimizer_loss_function.png" width="400"/>

# Training

We will train our model on 200 epochs and store train and validation losses.

Below is a plot of train and validation losses.

<img src="img/losses.png" width="700"/>

# Prediction

And then we will try to make a prediction.

<img src="img/prediction.png" width="1000"/>
