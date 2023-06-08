# Cryptocurrency Forecasting with LSTM and Dynamic GNN

This repository contains code and notebooks for a project focused on cryptocurrency price prediction. The project aims to explore and compare different machine learning approaches, including graph neural networks (GNNs) and Long Short-Term Memory (LSTM) models, to forecast cryptocurrency prices accurately.

<div align="center">
  <img src="https://github.com/nikgeokar/tgcn_lstm_for_crypto_forecasting/files/11642661/DynamicGraph.pdf" alt="1" width="500"/>
</div>

## Acknowledgments

### Introduction 
<li>Cryptocurrency popularity necessitates accurate forecasting. There is a growing interest in cryptocurrencies as investment options. </li>
<li>There is high volatility in cryptocurrency prices. </li>
<li>Deep learning addresses volatility and nonlinear patterns.</li>
<li>LSTM and GNN models improve prediction accuracy. </li>
<li>Dynamic graphs with directed edges are used.</li>
<li>A constructive evaluation method is employed.</li>
<li>This empowers informed decision-making in the cryptocurrency market</li>

### Inovation
<li>The proposed approach to the problem is entirely novel, as only one existing work utilizes graph neural networks for cryptocurrency price prediction </li>
<li>In that work, the graph structure remains fixed, and the correlations between cryptocurrencies remain unchanged over time.</li>
<li>However, this approach does not reflect real-life scenarios. Therefore, we employed dynamic graphs to capture the evolving correlations and investor behavior.</li>

### Proposed Method
<li>Incorporating core financial indicators, time-related features, and categorical variables.</li>
<li>Proposing two different architectures: LSTM and GNN+LSTM.</li>
<br>
<b>LSTM:</b>
<li>Training one LSTM network for each cryptocurrency to capture the unique patterns and characteristics of a specific cryptocurrency.</li>
<li>The proposed LSTM architecture combines LSTM layers to capture long-term dependencies in historical price data.</li>
<li>It is followed by fully connected layers to capture complex relationships and includes dropout and batch normalization for overfitting prevention.</li>
<br>
<b>GNN+LSTM:</b>
<li>Utilizing the TGCN2 architecture based on graph neural networks.</li>
<li>Spatializing the problem by using graphs and converting each cryptocurrency into a node.</li>
<li>Constructing dynamic graph datasets with a temporal signal to capture changing relationships.</li>
<li>Constructing directed edges using the Granger causality test to capture predictive relationships between cryptocurrencies.</li>
<li>The GNN+LSTM architecture combines a GNN with a Bidirectional LSTM applied to the spatial dimension.</li>

### Dataset
<li>The dataset encompasses the price history from 2021 to March 2023, consisting of 8,000 timesteps recorded at 4-hour intervals.</li>
<li>The dataset was divided into three sets for training (5,370 data points), validation (2,005 data points), and testing (622 data points).</li>
<li>Information on eight prominent cryptocurrencies is included: ADA, BNB, BTC, DASH, ETH, LINK, LTC, and XRP.</li>
<li>Key features such as high-low values, open-close values, and volume are available for each cryptocurrency.</li>



## Project Structure
The project is divided into several notebooks, each serving a specific purpose:

<b>Data_preprocessing.ipynb:</b> This notebook focuses on loading the raw data and preprocessing it to ensure it is in a suitable format, specifically a Pandas dataframe. The preprocessed data will serve as input for the subsequent notebooks.
<b>Graph_Construction.ipynb:</b> In this notebook, the data that has been transformed into a tabular format by the previous notebook is further processed to be in a suitable format for graph neural networks. The notebook handles the conversion of the data into an appropriate input format for graph-based models.

<b>TGCN_model.ipynb:</b> This notebook revolves around training and evaluating multiple architectures of graph neural networks. The focus is on implementing Temporal Graph Convolutional Networks (TGCN) and exploring their performance for the given task.

<b>LSTM_model.ipynb:</b> This notebook is dedicated to training and evaluating LSTM (Long Short-Term Memory) neural networks. The emphasis is on implementing and assessing the performance of LSTM models for the project.

<b>Comparison_Popular_ML_Algo.ipynb:</b> In this notebook, a variety of commonly used state-of-the-art machine learning algorithms are trained and evaluated. The goal is to conduct a fair comparison between these popular algorithms and the proposed method in the project.

<b>Backtesting.ipynb:</b> This notebook focuses on implementing a backtesting technique, which involves applying the trained models to real-life scenarios. The notebook explores how well the models perform in practical situations and evaluates their effectiveness.
Prerequisites

## Usage
To get started with the project, follow these steps:

Clone this repository to your local machine.
Install the required dependencies using pip install -r requirements.txt.
Run the notebooks in the specified order to preprocess the data, train different models, compare algorithms, and perform backtesting.
Feel free to explore the code, experiment with different approaches, and modify the notebooks to suit your needs.
