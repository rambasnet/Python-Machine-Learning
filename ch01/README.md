Sebastian Raschka, 2019

Python Machine Learning - Code Examples

# Chapter 1: Giving Computers the Ability to Learn from Data

---

**Chapter 1 does not contain any code examples.**

---

## Setting up Development Environment

- follow the instructions here: [https://github.com/rambasnet/DevEnvSetup](https://github.com/rambasnet/DevEnvSetup)

## Installing Python packages

Python is available for all three major operating systems — Microsoft Windows, macOS, and Linux — and the installer, as well as the documentation, can be downloaded from the official Python website: [https://www.python.org](https://www.python.org).

This book is written for Python version `>= 3.7.0`, and it is recommended
you use the most recent version of Python 3 that is currently available.

**Note**

You can check your current default version of Python by executing on a terminal

```bash
    python -V
```

### Anaconda

A highly recommended alternative Python distribution for scientific computing
is Anaconda by Continuum Analytics. Anaconda is a free—including commercial use—enterprise-ready Python distribution that bundles all the essential Python packages for data science, math, and engineering in one user-friendly cross-platform distribution. The Anaconda installer can be downloaded at [https://docs.anaconda.com/anaconda/install/](https://docs.anaconda.com/anaconda/install/), and an Anaconda quick start-guide is available at [https://docs.anaconda.com/anaconda/user-guide/getting-started/](https://docs.anaconda.com/anaconda/user-guide/getting-started/).

After successfully installing Anaconda, we can create virtual environment with a particular version of Python and install new Python packages in that environment using the following commands:


```bash
    conda create -n ml python=3.7
    conda activate ml
    conda install SomePackage
    conda deactivate
```

Existing packages can be updated using the following command:
#### NOTE: Must always activate ml virtual enviornment to install and run ML-related libraries

```bash
    conda activate ml
    conda update SomePackage
    conda deactivate
```

Throughout this book, we will mainly use NumPy's multi-dimensional arrays to store and manipulate data. Occasionally, we will make use of pandas, which is a library built on top of NumPy that provides additional higher level data manipulation tools that make working with tabular data even more convenient. To augment our learning experience and visualize quantitative data, which is often extremely useful to intuitively make sense of it, we will use the very customizable matplotlib library.

### Core packages

The version numbers of the major Python packages that were used for writing this book are listed below. Please make sure that the version numbers of your installed packages are equal to, or greater than, those version numbers to ensure the code examples run correctly:

- [NumPy](http://www.numpy.org) >= 1.17.4
- [SciPy](http://www.scipy.org) >= 1.3.1
- [scikit-learn](http://scikit-learn.org/stable/) >= 0.22.0
- [matplotlib](http://matplotlib.org) >= 3.1.0
- [pandas](http://pandas.pydata.org) >= 0.25.3

```bash
    conda activate ml
    conda install numpy
    conda install scipy
    conda install scikit-learn
    conda install matplotlib
    conda install pandas
```

### Jupyter Notebook

If you're wondering about the `.ipynb` of the code files -- these files are IPython notebooks. I chose IPython notebooks over plain Python `.py` scripts, because I think that they are just great for data analysis projects! IPython notebooks allow us to have everything in one place: Our code, the results from executing the code, plots of our data, and documentation that supports the handy Markdown and powerful LaTeX syntax!

![Jupyter Example](./images/ipynb_ex1.png)

**Side Note:**  "IPython Notebook" recently became the "[Jupyter Notebook](<http://jupyter.org>)"; Jupyter is an umbrella project that aims to support other languages in addition to Python including Julia, R, and many more. Don't worry, though, for a Python user, there's only a difference in terminology (we say "Jupyter Notebook" now instead of "IPython Notebook").

We can use the Conda installer if we have Anaconda or Miniconda installed:

```bash
    conda activate ml
    conda install jupyter notebook
```

To open a Jupyter notebook, we `cd` to the directory that contains your notebooks, e.g,.

```bash
    cd ~/PythonMachineLearning-Notebooks
```

and launch `jupyter notebook` by executing

```bash
    conda activate ml
    jupyter notebook
```

Jupyter will start in our default browser (typically running at [http://localhost:8888/](http://localhost:8888/)). Now, we can simply select the notebook you wish to open from the Jupyter menu.

![Jupyter File Explorer](./images/ipynb_ex2.png)

For more information about the Jupyter notebook, I recommend the [Jupyter Beginner Guide](http://jupyter-notebook-beginner-guide.readthedocs.org/en/latest/what_is_jupyter.html) and [Jupyter Notebook Basics](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Notebook%20Basics.html).

## Jupyter Lab

An alternative to Jupyter Notebook, called Jupyter Lab, was released in 2018. It operates with the same `.ipynb` file types but offers some extra features in the browser interface. Whether you use Jupyter Notebook or Jupyter Lab is a matter of preference, but

Jupyter Lab can be installed via:

```bash
    conda activate ml
    conda install -c conda-forge jupyterlab
```

and similar to starting Jupyter Notebooks, you can run the command 

```bash
    conda activate ml
    jupyter lab
```

in your command line terminal to launch a Jupyter Lab session in your browser. For more information about the Jupyter Lab project, please visit the official documentation at [https://jupyterlab.readthedocs.io/en/stable/](https://jupyterlab.readthedocs.io/en/stable).
