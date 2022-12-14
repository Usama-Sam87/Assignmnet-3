# Assignmnet-3

Linting is a process for identifying bugs and stylistic errors in your code. The process is carried out by analysis tools called ‘linters’, which are widely available for every major programming language.


So, I setup linting for a python project (exactly a code to see how linting points the errors).
Configuring linting tools for python, I used two different tools
Pylint: which looks for errors, enforces a coding standard that is close to PEP8, and even offers simple refactoring suggestions.
Flake8: which wraps around PyFlakes, pycodestyle and McCabe; this will check Python source code for errors and violations of some of the PEP8 style conventions.


Pylint:
Insatllation


pip install pylint


Setting up the code for linting with Pylint


pylint [script_name].py


Output


Then it gives an output something like this


{path}:{line}:{column}: {msg_id}: {msg} ({symbol})


There will also be an error code before {msg_id} as well 


If we want Pylint to omit a line check and ignore a message for that line of code, we can include the comment # pylint: disable=some-message. 
For example
print("Sum of squares is:") # pylint: disable=invalid-statement


Similarly Flake8 can also be easily configured for python projects


Flake8
Insatllation


pip install flake8


Setting up the running environemnt for linting with Flake8



flake8 [script_name].py


Also, we dont have to specify our script name for flake8, we can simply type "flake8" and it will by default run linting on all the scripts in our folder and display the error messages with their path.


Output


Then it gives an output something like this


{script_name}.py:1:1: F401 'numpy as np' imported but unused


For SAST in python, we explored
Python Taint actually PyT: which is a static analysis of Python web applications based on theoretical foundations (Control flow graphs, fixed point, dataflow analysis)



PyT
Insatllation


pip install python-taint


Setting up the python taint


python -m tests


This will run our tests contained in the tests directory.


These tools are of great use and really help in analysing the code
