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

Go to your GitHub area (`https://github.com/[yourgithubname]`), choose the "Repositories" tab and click on New.

Choose `qcd_school_ml` as the repository name, choose Public and leave other options as they are. This will create the repository and generate an instruction page.

On the terminal, check the remote:

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

Whoops!

We noticed that they are changes in the original repository. Let us define it as `upstream`:

```bash
git remote add upstream git@github.com:thaarres/qcd_school_ml.git
```

Now you can pull the changes to the local repository:

```bash
git pull upstream main
```

and push them to your remote GitHub repository with

```bash
git push origin main
```

## Check the container

Open the `my_python` container and check that you see the code repository:

```bash
docker start -i my_python
ls
```

The code should be visible under `qcd_school_ml`.

## About the file list

Take note the file names of the CMS open data files used in the tutorial can be downloaded with the `cernopendata-client` as explained in the [Dataset scounting tutorial](https://cms-opendata-workshop.github.io/workshopqcd-2024-lesson-dataset-scouting/04-cli-through-cernopendata-client.html#get-dataset-information)

```bash
docker run -i -t --rm docker.io/cernopendata/cernopendata-client  get-file-locations --recid 63168 --protocol xrootd 
docker run -i -t --rm docker.io/cernopendata/cernopendata-client  get-file-locations --recid 33703 --protocol xrootd
```

A subset of them is already in the notebook, but this is how you would get them.

::::::::::::::::::::::::::::::::::::::: callout

That's it, you are ready to (machine) learn!

:::::::::::::::::::::::::::::::::::::::