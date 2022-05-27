# Course Project - Big Data Engineering

## Abstract

The aim of this project has been to experiment in the field of big data which we accomplished by setting up our own data streaming model between a server and a client and then applied ensemble method to train the chunked data based on the following models – LR, SVM, RF, LDA, KNN, CART and Naive-Bayes. A Heterogeneous dataset was created by merging the datasets of all TON IoT devices. We also applied bayesian theorem for model preparation to predict the class of attack based on data received from the other devices.

## File Structure Breakdown

```output
.
├── client
│   ├── client.ipynb    # receives data from server & process it
│   ├── ensemble.log    # logs generated while ensemble model training
│   └── stream.log    # logs generated while data streaming
├── data
│   ├── merged_data.csv    # IoT devices data processed & merged
│   └── test_heterogeneous.csv    # prepared from 'merged_data.csv'
├── data_preparation
│   ├── data_merging.ipynb    # data of all IoT devices processed datasets is merged here
│   ├── data_preprocessing.ipynb    # data of all IoT devices datasets is cleaned and processed
│   ├── merged_data
│   │   └── merged_data.csv    # final output of merging all IoT devices processed datasets
│   ├── processed_data    # removed NaN values and grouped duplicate rows by selecting mode
│   │   ├── IoT_Fridge.csv
│   │   ├── IoT_Garage_Door.csv
│   │   ├── IoT_GPS_Tracker.csv
│   │   ├── IoT_Modbus.csv
│   │   ├── IoT_Motion_Light.csv
│   │   ├── IoT_Thermostat.csv
│   │   └── IoT_Weather.csv
│   └── raw_data    # data downloaded from TON IoT website
│       ├── IoT_Fridge.csv
│       ├── IoT_Garage_Door.csv
│       ├── IoT_GPS_Tracker.csv
│       ├── IoT_Modbus.csv
│       ├── IoT_Motion_Light.csv
│       ├── IoT_Thermostat.csv
│       └── IoT_Weather.csv
├── models
│   ├── h5s    # model structure stored in '.h5' format
│   │   ├── CART.h5
│   │   ├── GRU.h5
│   │   ├── kNN.h5
│   │   ├── linear-discriminant-analysis.h5
│   │   ├── logistic-regression.h5
│   │   ├── LSTM.h5
│   │   ├── naive-bayes.h5
│   │   ├── random-forest.h5
│   │   └── support-vector-machine.h5
│   └── notebooks    # notebook files for individual model by their names
│       ├── CART.ipynb
│       ├── GRU.ipynb
│       ├── kNN.ipynb
│       ├── linear-discriminant-analysis.ipynb
│       ├── logistic-regression.ipynb
│       ├── LSTM.ipynb
│       ├── naive-bayes.ipynb
│       ├── random-forest.ipynb
│       └── support-vector-machine.ipynb
├── README.md
└── server
    └── server.ipynb    # send row-wise data at clients in a stream
```

## Conclusion

The data streaming was successfully setup between the client and server, the server was streaming data to the client and the client on obtaining the data created chunks of variable sizes as per the models requirements and trained them accordingly using the ensemble method and building upon the previously received data.
