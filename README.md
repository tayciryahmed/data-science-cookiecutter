### Author 
Taycir Yahmed

### Requirements to use the cookiecutter template

 - Cookiecutter Python package: This can be installed with pip or conda.

### To start a new project, run:

    cookiecutter ***


### The resulting directory structure

The directory structure of your new project looks like this: 

```
Project name
├── config
│   │   ├── dev_configfile.json          <- app configs for execution in the dev 
│   │   ├── local_configfile.json        <- app configs for execution in the local debugging
│   │   ├── prod_configfile.json         <- app configs for execution in the prod 
│   │   └── test_configfile.json         <- app configs for execution in the test 
├── jobs
│   └── workflows
│       └── workflow_ml
│           └── workflow.xml             <- configure your workflow here
├── data                           <- a sample from the prod data to debug the code locally
│   ├── external                         <- data from external sources (web scraping ...)
│   │   └── external_data.txt
│   ├── internal                         <- internal data 
│   │   └── internal_data.txt
│   └── processed                        <- result of combining data from different sources
│       ├── test                         <- test data for evaluating models 
│       │   └── test_data.txt
│       └── training                     <- training data 
│           └── training_data.txt
├── log_template
│   └── log.template                     <- find a log template here
├── Makefile                             <- makefile (if needed)
├── models                               <- where to serialize trained models
│   └── serialize_your_models_here
├── README.md
├── shell_scripts
│   └── script.sh                        <- shell script that specifies the execution steps if any
├── src
│   ├── main.py                          <- starter point to the module pysparkml
│   └── module                           <- the module where to code the ML workflow
│       ├── data_preprocessing.py        <- Class where to integrate your data preprocessing
│       ├── features_building.py         <- Class where to perform feature building / selection
│       ├── __init__.py                  <- starter point for the module
│       ├── model_building.py            <- a class where you build your models 
│       ├── read_config.py               <- a class that reads the configs and parse them (can be unchanged)
│       └── tests.py                     <- code your tests here 
└── visualization_notebooks              <- contains the projects notebooks
    ├── exploring_data.json
    └── presenting_results.json

```
