# Course Project - Big Data Engineering

## Abstract

The aim of this project has been to experiment in the field of big data which we accomplished by setting up our own data streaming model between a server and a client and then applied ensemble method to train the chunked data based on the following models – *LR*, *SVM*, *RF*, *LDA*, *KNN*, *CART* and *Naive-Bayes*. For this project, I chose `IoT_Garage_Door` data from TON IoT datasets and the `label`(type of attack) as target variable.

## File Structure Breakdown

```output
.
├── client
│   ├── client.ipynb    # receives data from server & process it
│   ├── ensemble.log    # logs generated while ensemble model training
│   └── stream.log    # logs generated while data streaming
├── data
│   ├── IoT_Garage_Door.csv    # IoT_Garage_Door raw data
│   └── test_garage.csv    # prepared from 'IoT_Garage_Door.csv'
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
