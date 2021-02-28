# true_film_ETL
### Requirements:
This ETL pipeline is designed to run using a Jupiter Notebook with a Python 3 kernel.
It will use multiple python modules (listed in the requirements.txt file). The notebook will install all the dependencies in the first cell.
Postgresql is the required output so it's essential that you have it set up on the computer where the notebook is going to run.

Should you not be familiar with the tools, check these webpages to assist
- Python 3: https://realpython.com/installing-python/
- Jupyter: https://www.dataquest.io/blog/jupyter-notebook-tutorial/
- Postgres:
- - https://www.postgresql.org/download/
- - useful links for troubleshooting username and password: https://stackoverflow.com/questions/46781471/why-postgresql-on-mac-asks-me-for-password-after-fresh-install/49124153
- - useful link for first setup: https://wiki.postgresql.org/wiki/Homebrew

### Datasets:
Two datasets are used for this ETL.
- imdb: https://www.kaggle.com/rounakbanik/the-movies-dataset/version/7#movies_metadata.csv
- - Go to the link above and download the dataset "movies_metadata.csv". When you download it, it will be a compressed file, unzip it and copy/move the `.csv` file in the same directory where there is the notebook ( `true_film_ETL.ipynb` )
- wikipedia: https://dumps.wikimedia.org/enwiki/latest/enwiki-latest-abstract.xml.gz
- - The link above is a direct download of a compressed file, unzip it and copy/move the `.xml` file in the same directory where there is the notebook ( `true_film_ETL.ipynb` )

### Running the notebook:
From the Command Line Interface (CLI) go to the directory of the notebook (eg. `cd ~/path/to/my/directory/`) and run `jupyter notebook` in the CLI.
This command will open a web interface in your default browser showing the content of the directory. Click on `true_film_ETL.ipynb` and it will open another tab with the notebook.

At the top you will see a "play" button and by pressing it once you'll start the pipeline. The play button will run one cell at the time, if you wish to run everything in one go (recommended) use the "forward" button that will restart the kernel and run every cell.

Most likely the last bit of the notebook will fail. This is because it is set up to use the postgres server of my local machine. By updating the variables in the cell you'll be able to re-run it with your configuration.

A few examples of querying the table are at the bottom of the notebook, feel free to modify the variable `query` to run a different query


### Tools used:
#### Jupyter Notebook
Highly flexible interactive environment that allows the developer to write documentation alongside the code.
#### Python 3
A modern standard for Data ETL
#### Pandas library
Widely used industry standard to handle structured data within Python
#### python-sql
Python library that allows running queries for postgres from within the notebook
