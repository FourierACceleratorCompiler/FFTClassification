# FFT Classification

This directory contains the reproducibility steps for the machine learning part of the article (i.e., Figure 11).

We assume that the data (data/) is already present. It contains the data from the OJClone algorithm classification dataset introduced in Mou et al. 2015 + our extra class consisting of FFTs.

## Setup

Assume a Python3.8 installation in a Unix machine.

Run: 


```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Run


```

1. Run training and evaluation with cross-validation (this bash loop will execute train.py with different data splits, saving the results for each run in output/):

```

bash run_cv.sh
```


2. Gather results from the cross-validation (this will generate a results.csv file):


```
source venv/bin/activate
python gather_results.py
```

3. Plot results from the previous step (obtaining figure 11)

```
source venv/bin/activate
python plot.py
```
