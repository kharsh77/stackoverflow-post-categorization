stackoverflow-post-categorization
============================================================


Machine learning models with stackoverflow datasets.


Part 1:

DATASETS:
> We are working on public datasets from stackexchange
> The dataset contains questions which front-end-software-developers use while programming.
> The details about dataset can be found in "POSTS" table in the link below:
        https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede

AIM: 
> To categorize these questions into seven catgories. We have came across these catogaries by doing extensive research on the web according to different domains generally front-end-software-developers mainly work on. The details about these categories can be found in preprosseing code.

STEPS:
> From a observation, we found 30K out of 300k questions (from the dataset) had just single tag associated with it.

> We formulated our categories using these single tag data.

> Then we categoried our single-tags questions data(around 30k) and used it as training data to train our classifiers. We used Naive bayes and SVM to train our classifiers. We selected SVM models to go ahead as we clocked better efficiency.

> Using SVM trained model, we classified (2.5k) multi-tag-questions into seven categories. 

=======================================================================================================


Part 2:

DATASETS:
> Here, we are working on labelled data output from PART 1.

AIM: 
> We want to derive a sense on different types of question front-end-developers solve problems from a particular categories (out of seven which we have earlier used). Say, in a category which demarks questions from different front-end-frameworks (ex- angular, react) what are the type of problems on which developers are working.

STEPS:
> We took questions dataset which belongs to on categories and use k-means clustering algorithm to make few clustures.

> We noted down top keys words which appears per cluster and represented the clustered data into different plots.


FUTURE GOALS:

> To implement clustering algorithm in all categories and implement nlp to derive more sense to the data.



Please refer to /notebooks/ to get access to all ipython code for the above implementation.




Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.testrun.org


--------

<p><small>Project structure based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
