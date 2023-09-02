# Annihilate Hate: Hasoc Fire Task 4

## About

## Dataset Overview

## Evaluation Metrics

## Directory Navigation

### docs

- Related docs such as references, articles, documentation, etc to be saved in this directory.

### inp

- Input data folder.

### models

- Trained weights/ pretrained-weights of various models used/referred in the solution.

### notebooks

- EDA, modelling, pipeline notebooks to be added here.

### out

- contains the output data such as submission files, etc.

### src

- Code package, consisting of modularised code for data preparation, cross validation, feature engineering, modelling, inference code snippets.

## VENV set-up

For the starter, I've used *pip* over *miniconda* for package management. Follow the steps mentioned to set up your work ennvironment and get going.

1. Create a virutal environment using `python venv`

```sh
cd proj-dir
python -m venv hasoc-task4-ah
```

2. On successful creation of the env, activate the env by navigating to the `activate` script depending on your operating system.  
If using `WSL` on windows or linux, run the following:

```sh
cd hasoc-task4-ah
source ./hasoc-task4-ah/bin/activate
```

To make sure you're using the correct python env, run the following command. You should get the `bin/python` path of your virutual env as output.

```sh
which python
```

3. Now that the env is there, time to install some initial packages to get going. Note that, you can and should install your project specific requirements as you proceed.

To install from the `requirements.txt` file:

```sh
python -m pip install -r requirements.txt
```

Note that, it's recommended to follow the given directory structure. Meaning, `src`, `logs`, etc. along with your venv folder should be a subfolder inside your `proj-dir` folder. And all the files should be placed accordingly.

4. Now that the initial libs are installed, you can run the logger and the configuration to make sure things are in-place and working. And, execute the first cell of the starter notebook as well, you should get the config loaded in there.

To run logger and the configuration for sanity check:

```sh
cd src
python logger.py
python configuration.py
```

5. Now that the code base is set-up, we can create the validation folds for a particular seed. `2023` is used here as seed. To create the folds, we can run the following command:

```sh
cd src
python validation_folds.py
```

Note that, you can edit the `_LANG` variable in the `validation_folds.py` to corresponding languages such as `assamese`, `bodo`, or `bengali`. The folders will be created inside the `/inp/{_LANG}/folds` folders. These validation folds will be used for training in the `train.py` script.

6. Once the validation folds are in the appropriate folders, run the following command to do training and inference:

```sh
cd src
python train.py
```

Note that, update the corresponding language and model name in the `train.py` file before proceeding.
