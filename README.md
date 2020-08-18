# Risk-Score-1-UMichZJU

## [RMDS Lab](https://www.rmdslab.com/)  Risk Score Project (UMichZJU)

*Shravani Kasralikar, Wanying Shao, Victor Qiu 28/07/2020*

*Project Manager: Alicia Wei*

*Open source project in collaboration with University of Michigan, ZJU Team. Link to their project found [here](https://grmds.org/node/744).*


## Technical Solutions Description

For this project, our team used a variation of technical tools and platforms to accomplish the goal at task: creating a output dataset with the LA County community-based risk scores and risk levels. Our team utilized Python and Jupyter Notebooks to create our data pipeline and run our script. We researched the population and income data by data mining through various databases and online resources. We web-scraped mobility data from Apple and Google, and we obtained general population data from the LA Times’ COVID-19 GitHub database. With the data collected, we cleaned and pre-processed the data by changing the structure and creating several new variables in our data frame including: new confirmed cases, average number of days for new cases to occur (7-10 days), etc. These variables are used as features for future analysis. With the completed dataset, out team inputted it into the Long Short-term Model (LSTM Model), which utilizes PyTorch, to gain our predicted daily COVID-19 cases result. Our team then used these predicted results to compute the risk scores. We then used a distribution curve to categorize risk scores into different risk levels based on defined criterias.


## Setup

Have [anaconda](https://www.anaconda.com/products/individual) or miniconda installed. This will automatically install jupyter notebook and other required packages.

**Option 1 (if running locally):**

Clone this repository from github. Open jupyter notebook by running,
```
jupyter notebook
```

Navigate to cloned repository within jupyter notebook. Navigate to script and open: **scripts/final-script/Data_Sourcing_and Solution.ipynb.** Run script.

**Option 2 (run notebook from command line):**

Have [nbconvert](https://github.com/jupyter/nbconver) installed. 

In command line,
```
jupyter nbconvert --execute Data_Sourcing_and_Solution.ipynb
```

## Output

**Output file:** [LA-daily-out.csv](https://github.com/skasralikar/Risk-Score-1-UMichZJU/blob/master/data/output/LA_daily_out.csv)

**Region:**
- City or community in LA County

**Timestamp:**
- Date of newly updated data

**Risk Score Level:**
- Risk score level calculated from risk score to categorizes how dangerous (level -1-3) an certain LA County based community or city is

**Risk Score:**
- Risk score = (number of infectious people x 10,000)/population size; number of infectious people predicted by LSTM model; scored based on LA County community or city. Negative scores are considered very low risk.


## Workflow
![workflow](https://github.com/skasralikar/Risk-Score-1-UMichZJU/blob/master/Risk-Score-UMich-Workflow.png)
