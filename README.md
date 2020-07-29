# Risk-Score-1-UMichZJU

#RMDS Risk Score Project (UMichZJU)

*Shravani Kasralikar, Wanying Shao, Victor Qiu 28/07/2020*

*Project Manager: Alicia Wei*


## Setup

Have [anaconda](https://www.anaconda.com/products/individual) or miniconda installed. This will automatically install jupyter notebook and other required packages.

**Option 1 (if running locally):**

Clone this repository from github. Open jupyter notebook and navigate to this cloned repository.

Open script: Data_Sourcing_and Solution_02.ipynb. Run script.

**Option 2 (run notebook from command line):**

Have [nbconvert](https://github.com/jupyter/nbconver) installed. 

In command line,
```
jupyter nbconvert --execute Data_Sourcing_and Solution_02.ipynb
```

**Option 3 (run in environment):** 

Clone this repository from github. In the cloned repository, 
```
conda env create -f environment.yml
```
Switch to the new environment:
```
conda activate rmds-riskscore1
```
Check that the environment was properly activated:
```
conda info
```
The first line should show:
```
active environment: rmds-riskscore1
```

## Workflow
![workflow](https://github.com/skasralikar/Risk-Score-1-UMichZJU/blob/master/Risk-Score-UMich-Workflow.png)
