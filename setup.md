---
title: Setup
---


## Docker containers

You will be using the Python container as instructed in the [Docker lesson](https://cms-opendata-workshop.github.io/workshopqcd-2024-lesson-docker/03-docker-for-cms-opendata.html#python-tools-container).

You are expected to have worked though the CMS open data example in that python container as instructed in the [Dataset scouting lesson](https://cms-opendata-workshop.github.io/workshopqcd-2024-lesson-dataset-scouting/05-what-is-in-the-data.html#inspect-datasets-with-python-tools). if you have not done it yet, do it now.


## Get the code

Clone the code from the example repository in a working directory that you have shared with the container. If you followed the instructions in the Docker tutorial, the working directory in `cms_open_data_python`: 

```bash
cd cms_open_data_python
git clone git@github.com:thaarres/qcd_school_ml.git
cd qcd_school_ml
```

Add this code to your personal GitHub account. 

In the GitHub Web UI, create a new repository as instructed in the [Git tutorial](https://cms-opendata-workshop.github.io/workshopqcd-2024-lesson-git/04-exercises.html#upload-an-existing-local-repository-to-github).

Go to your GitHub area (https://github.com/[yourgithubname]), choose the “Repositories” tab and click on New.

Choose `qcd_school_ml` as the repository name, choose Public and leave other options as they are. This will create the repository and generate an instruction page.

On the reminal, check the remote:

```bash
git remote -v
```

```output
origin  git@github.com:thaarres/qcd_school_ml.git (fetch)
origin  git@github.com:thaarres/qcd_school_ml.git (push)
```

Change remote’s URL in order to be able to add the code to your personal GitHub account.

```bash
git remote set-url origin git@github.com:<GitHub username>/qcd_school_ml.git
```

Check again the name of the current remote:

```bash
git remote -v
```

Push the code to your new repository with

```bash
git push -u origin main
```

That's it, you are ready to (machine) learn!

