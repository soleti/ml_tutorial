[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/soleti/ml_tutorial/HEAD?labpath=Tutorial.ipynb)

# Machine learning tutorial

In this tutorial we will try to train one _multi layer perceptron_ using [Keras](https://keras.io) and one _boosted decision tree_ using [XGBoost](https://xgboost.readthedocs.io/en/stable/) in order to distinguish between _true_ and _fake_ conversion electron hits in the Mu2e experiment.

## Install

The first step to run the notebook is to install `mamba` (or `conda`) and JupyterLab. I personally prefer `mamba`. Installation packages are available [here](https://github.com/conda-forge/miniforge#mambaforge).

Once you have installed Mamba, you can install JupyterLab with:

```bash
mamba install -c conda-forge jupyterlab
```

Now, we need to create an environment containing the packages required by the tutorial. In the `ml_tutorial` directory run:

```bash
mamba create -n ml_tutorial --file requirements.txt
```

This will create a `ml_tutorial` environment. In order to access it you can run
```bash
mamba activate ml_tutorial
```
We then want to add this environment to the list of _kernels_ available to JupyterLab:
```bash
python -m ipykernel install --user --name ml_tutorial --display-name MLTutorial
```

Now, go back to your `base` environment and launch JupyterLab:
```
mamba activate base
jupyterlab Tutorial.ipynb
```

In order to use the `ml_tutorial` environment you just created select "MLTutorial" in the list of kernels in the upper right part of the interface.
