# Set up
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
