# Invoice validation 






## Part : ML Experiments with MLflow and DagsHub

### Introduction

This project is about conducting Machine Learning experiments using MLflow and DagsHub. MLflow is an open-source platform to manage the ML lifecycle, including experimentation, reproducibility, and deployment. DagsHub is a platform built for data version control and collaboration.


#### Prerequisites

- Python 3.7 or higher
- MLflow
- DagsHub

#### Installation

1. Clone the repository
```bash
git clone <repository-url>
```

#### Configuration Steps : 
This guide will walk you through the steps to configure your model scripts to send metrics to our centralized MLflow server hosted on DagsHub.
##### 1. Set Environment Variables 

Before running your script, set the following environment variables with the provided credentials:

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/akramLh005/PFA-mlflow.mlflow
export MLFLOW_TRACKING_USERNAME=akramLh005
export MLFLOW_TRACKING_PASSWORD=<password>
```
Replace <password> with the actual password provided.

##### 2. Update Your Model Script 

In your model script, add the following lines to configure MLflow to use the DagsHub server:

import mlflow

```bash
remote_server_uri = "https://dagshub.com/akramLh005/PFA-mlflow.mlflow"
mlflow.set_tracking_uri(remote_server_uri)
```



