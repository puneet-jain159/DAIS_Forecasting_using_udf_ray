# Forecasting At scale using Pyspark UDF and Ray
This is Repository containing the codes used for the talk ["Hyperparameter Tuning Via Apache Spark™ and Ray"](https://www.databricks.com/dataaisummit/session/hyperparameter-tuning-apache-sparktm-and-ray/)

## Steps to run the forecasting solution
Start a multi-node GPU cluster the current script is tested on following specs:
Runtime: ML-GPU 13.2
Master Node: g4dn.xlarge
Worker Node: g4dn.2xlarge
number of nodes: 2
### Step 1. Use init script to start a ray cluster
The current solution uses init scripts to create a ray cluster. check out the this [link](https://docs.databricks.com/clusters/init-scripts.html) for how to attach and init script to a cluster.

<br></br>
<div style="text-align: center; line-height: 5; padding-top: 20px;  padding-bottom: 20px;">
  <img src="https://raw.githubusercontent.com/puneet-jain159/Image_dump/2f9a57de07ebf199ed5e7d59bb784c3600ac9eac/cluster_init_script.png" alt='Push compute' height="200" width="400">
</div>

### Step 2. Run the preparing_walmart_m5_data notebook
Add your Kaggle credentials to dowmload the data and convert it into delta format
'''
KAGGLE_USERNAME
KAGGLE_KEY
'''
### Step 3. Run the main notebook 
This will trigger the process to run forecasting