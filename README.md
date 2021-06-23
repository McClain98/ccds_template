template
==============================

## How to Replicate

1. `pip install cookiecutter`

2. `mkdir {project_name}`

3. `cd {project_name}`

4. `cookiecutter https://github.com/drivendata/cookiecutter-data-science`

5. ```
   echo "# {project_name}" >> README.md
   git init
   git add README.md
   git commit -m "first commit"
   git branch -M main
   git remote add origin https://github.com/{github_username}/{project_name}.git
   git push -u origin main
   ```

6. `git branch gh-pages`

7. `git checkout gh-pages`

8. `mkdir docs`

9. `echo "# this file just tells gh to note use jekl" >> docs/.nojekyll`

10. add commit and push to github

11. got to GitHub > settings > pages and set source to the `gh-pages` branch and `/docs` folder

Thats pretty much it. You now have working sphinx docs. When you want to publish just build the html docs by going to the `{project_name}/docs` directory and running `make html`. Then move this to root with `cd ../..` , `mv {project_name}/docs/_build/html/* docs/` and it should autmomatically but published. 

Check out this project example if you want to use markdown: https://github.com/serra/sphinx-with-markdown

This is a template repo for ccds projects with nice published documentation

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
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
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
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
# ccds_template
