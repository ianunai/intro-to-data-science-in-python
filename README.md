# Introduction to Data Science in Python
## Description
Offered as course 1 of the specialization [Applied Data Science with Python Specialization](https://www.coursera.org/specializations/data-science-python)

## Virtual Environments in Python

Virtual environments in Python help with keeping separate spaces for different projects in Python, allowing each project to keep its own set of dependencies which avoids installing packages globally for even a small project.  

While working through this course, I created a virtual environment in order to keep a reproducible environment with the full set of dependencies required by the project.

### Creating and Activating

1. __Creating a virtual environment:__ In terminal, issue the following command:
```
python3 -m venv /<path to venv>
```

For example, I issued the following command, which created a virtual environment called `data-science-venv` under the location I specified.

```
python3 -m venv /Users/ianunai/.utils/data-science-venv
```

2. __Activating the virtual environment:__ Navigate to the `bin` directory under your virtual environment and source the `activate` file.

```
$ cd bin
$ source activate
```

__Note:__ In order to deactivate a particular virtual env, simply run the following command:

```
$ deactivate
```

In newer version of venv, `deactivate` is provided as a shell command after activating the virtual environment.

### Using virtual environment as a kernel in Jupyter Notebook

By default, Jupyter Notebook is configured to use the system Python interpreter as its kernel. In order to use the Python interpreter, we need to implement the steps listed below:

1. Ensure that the virtual environment we want to use is active. If not, source the `activate` file as mentioned in step 2 above.

2. Once the venv is active, run the following command on your terminal:
```
pip install ipykernel
```

3. Finally, in order to install the venv as a kernel for Jupyter, run the following command once `ipykernel` is installed:
```
ipython kernel install --user --name=<name of venv>
```

In my case, the command would look something like this:
```
ipython kernel install --user --name=data-science-venv
```

Now, upon running Jupyter Notebook, while creating new notebooks, we should be able to see the option for the venv under kernel.