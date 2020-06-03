# Building your documentation

## Setting up a local environment to publish markdocs as in docs.dhis2.org

DHIS2 Documentation publishes the documentation using [Mkdocs][mkdocs] as a site generator themed with [Material for Mkdocs][material].

Below are the steps to create this environment on your local machine, tested using a Mac. Setting this environment locally  allows you to test the look-and-feel of your documentation before pushing it on the Github repository either  for publication directly on the repo or on the main DHIS2 Documentation portal.

### Setting up the environment

* Checking version of Python. if running Python 2.7 upgrade -if on Windows or Linux, install -if on Mac a newer version 3.x.
  * On Mac  run `brew install python3`then check that Python3.x is installed running `python3 --version` [Source: https://osxdaily.com/2018/06/13/how-install-update-python-3x-mac/](https://osxdaily.com/2018/06/13/how-install-update-python-3x-mac/)
* Make sure your `pip` is set to Python3.x by running `pip3 install --upgrade --force pip`. You may need to append `sudo` [Source: https://stackoverflow.com/questions/38938205/how-to-override-the-pip-command-to-python3-x-instead-of-python2-7/38938246](https://stackoverflow.com/questions/38938205/how-to-override-the-pip-command-to-python3-x-instead-of-python2-7/38938246)
* To run a similiar look and feel as in docs.dhis2.org, you want to use Material fro Mkdocs running `pip install mkdocs-material`.

### Getting started

* run `mkdocs new PROJECT_DIRECTORY`. Assuming that you have a local repo of your Github repo, the `PROJECT_DIRECTORY` is your local repo. This command will create a docs folder, an index.md file as well as a mkdocs.yml file. [Source: https://www.mkdocs.org/#getting-started](https://www.mkdocs.org/#getting-started)
* run the `mkdocs serve` command to start the built-in server
* Copy/paste the following url `http://127.0.0.1:8000/` in your browser, and you'll see the default home page being displayed  [Source: https://www.mkdocs.org/#getting-started](https://www.mkdocs.org/#getting-started)

### Creating your documentation

* Write your documentation in markdown- [More guidelines here: https://www.mkdocs.org/user-guide/writing-your-docs/](https://www.mkdocs.org/user-guide/writing-your-docs/)
* Edit the `mkdocs.yml` file. Feel free to copy the one used in this repo as a starting point. More guidelines on the [MkDocs website][mkdocs yml]  and [Material for MkDocs][material yml]
* Regularly check  `http://127.0.0.1:8000/` to see the  result of your edits.

[mkdocs]: https://www.mkdocs.org/
[material]: https://squidfunk.github.io/mkdocs-material/
[mkdocs yml]: https://www.mkdocs.org/user-guide/writing-your-docs#configure-pages-and-navigation
[material yml]: https://squidfunk.github.io/mkdocs-material/getting-started/#configuration
