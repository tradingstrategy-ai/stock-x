# Stock-X

![License](https://img.shields.io/github/license/Circle-1/Stock-X)
![Stars](https://img.shields.io/github/stars/Circle-1/Stock-X)
![Release](https://img.shields.io/github/v/release/Circle-1/Stock-X)
[![Heroku](https://img.shields.io/badge/Heroku-Active-blue?logo=heroku)](https://stock-x-proj.herokuapp.com/)

## FORK

This is the fork of original Stock-X repository from the paper [Predicting Stock Market time-series data using
CNN-LSTM Neural Network model](https://arxiv.org/pdf/2305.14378) by Aadhitya, Rajapriya, Vineetha and Anurag.

Read the [reproducible CNN-LSTM notebook here](./stock-market-prediction-using-cnn-lstm.ipynb).

- The fork was done for the result reproducibility (code was not runnable) 
- The instructions to run the code were added. 
- The code was modified to run outside Kaggle.
- The project was made to possible to install with its dependencies with [poetry](https://github.com/python-poetry/).
- `stock-market-prediction-using-cnn-lstm.ipynb` was bug fixed 
- The notebook was changed train the model IBM stock data through AlphaVantage (not sure how the origina stock data was accessed)
- The notebook was changed to cross-validate the model on MSFT stock (not sure if this is supposed to work in the first place, because I am not sure if data is normalised at all)
- More common statistics used in machine learning benchmarks added (MAE, MAPE, etc.), 
  these may or may not be sensible in the context of this project
- Bug fixes, bug fixes, bug fixes to make code runnable

The following environment variables are needed

- `ALPHAVANTAGE_API_KEY`: Get the free API key from [AlphaVantage](https://www.alphavantage.co/support/#api-key)

We use [python-dotenv package](https://github.com/theskumar/python-dotenv) so you can edit `.env` file and add there.

To run the original code, clone this repository and then:

```shell
brew install graphviz # MacOS, needed for plot_model()
poetry install
# Open this file in Visual Studio Code to run with Jupyter editor,
# instead of running from command line
ipython stock-market-prediction-using-cnn-lstm.ipynb 
```

## ⚠️ **MODEL is now available at Hugging Face: https://huggingface.co/kryox64/stock-x** with DOI ⚠️

This project is all about analysis of Stock Market and providing suggestions to stockholders to invest in right company

Note: The notebook used here (IPYNB) is made using Kaggle, a data-science and ML community website which provides free Jupyter Notebook environment to work on programs and GPUs and TPUs to work on Neural Networks easily.

Here's the ref link to [Kaggle](https://www.kaggle.com/)

Notebook link for CNN-LSTM: [Click here](https://www.kaggle.com/aadhityaa/stock-cnn-lstm)

Docker Image link (contains bundled libraries): [Click here](https://hub.docker.com/r/aerox86/stock-x) ![Size](https://img.shields.io/docker/image-size/aerox86/stock-x/latest-stable)

Helm charts: [![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/stock-x)](https://artifacthub.io/packages/search?repo=stock-x)

## Libraries used:
    - Tensorflow
    - Keras
    - Pandas
    - Scikit-learn
    - Matplotlib
    - Seaborn

## Neural Network type

Here CNN (with Time Distributed function) and Bi-LSTM combined Neural Network is used to train. Other algorithms like XGBoost, RNN-LSTM, LSTM-GRU are also added for comparison. Here are the links to view the notebooks directly. You can also view the results in the app created using [Mercury](https://mljar.com/mercury/) which is deployed over [Heroku (free dyno)](https://stock-x-proj.herokuapp.com/).

 - [CNN-LSTM](stock-market-prediction-using-cnn-lstm.ipynb)
 - [LSTM-GRU](lstm_gru_model.ipynb)
 - [RNN-LSTM](RNN-LSTM.ipynb)
 - [XGBoost](regressor-model.ipynb)
