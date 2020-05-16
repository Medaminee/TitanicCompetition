# Titanic Competition
This repository contains our work for the kaggle titanic competition. 

## Control the container 

```
    docker-compose up: mounts the directories and starts the container 
    docker-compose down: destroys the container 
```    
 

## The compose file: 
``` yaml
version: '3'
    services:
      jupyter-notebook:
        container_name: jupyter-notebook
        image: jupyter/datascience-notebook
        volumes:
            - ./notebook:/home/jovyan/work
            - ./data:/home/jovyan/work/datasets
        ports:
          - "8888:8888"
```

The notebook directory contains the notebook where we detail the solution of this competition. 
data: Contains the data for the competition: 
    - train.csv: the train data for our model. 
    - test.csv: test data for prediction. 
    - output.csv: the result of our final prediction. 
    
# Github configuration for jupyter notebook
## nbstripout
strip output from Jupyter and IPython notebooks. 
[reference](https://github.com/kynan/nbstripout)
### Installation 
```bash
pip install --upgrade nbstripout
```

### Usage
```bash
nbstripout TitanicCompetition.ipynb
```
