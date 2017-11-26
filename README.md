# steam-ratings
Analysis of Steam store ratings using product information available on the store.  Data in the database dump was originally obtained by running the scraping script in [this repository](https://github.com/jasonnance/steam-store-analysis).

## Usage
This analysis is presented as run on my personal computer; some changes to usernames, file paths, etc. may be necessary to run in a new environment.

### Requirements

 - Python 3 with conda
 - PostgreSQL 9.6+

After all requirements are installed, run the following to load the database dump:

    createdb steam
    pg_restore -d steam -O steam.dump
    
Create a conda environment and install Python packages with the following:

    conda env create -f environment.yml
    
Launch Jupyter Notebook:

    jupyter notebook
    
You should then be able to run any of the following notebooks:

- Exploratory.ipynb: Some exploratory analysis.
- Midway Code.ipynb: Code for the midway project report; trains a LASSO regression model without any text features.
- Steam Ratings Code.ipynb: Final code; trains a LASSO regression model and AdaBoost regression model with text features.
