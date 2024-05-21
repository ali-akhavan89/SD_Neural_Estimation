# System Dynamics Neural Estimation Replication Instructions
You can find all the codes and models from the link below:

https://github.com/ali-akhavan89/SD_Neural_Estimation 

To run the scripts, you need to have Vensim DSS, Python, and relevant Python libraries and packages installed on your computer. Note that some functionalities, like DLL, are not available on macOS and, on Windows, require administrative permissions to be installed and used. Below are the general instructions, which may need some minor adjustments if you are on macOS. Follow these instructions to install the necessary packages:



1.	Download and install Miniconda from 

https://docs.anaconda.com/free/miniconda/

2.	Open a Command Prompt or a Terminal window connected to Conda

3.	Install BayesFlow and related libraries with the command:

```python 
pip install bayesflow
```

4.	Install packages required for VST scripts with the following commands:

```python
pip install keyboard
pip install regex
```

5.	If you want to use the DLL functionality, download the VenPy package from:

https://github.com/VensimSoftware/venpy

6.	Unzip the folder in a familiar location (e.g., Desktop). Using the Command Prompt window, navigate to that directory (e.g., ‘cd Desktop’)

7.	Navigate to the VenPy package directory, ‘venpy-master’.


8.	From within the directory in the command prompt window, install the VenPy package with:

```python
pip install .
```


After completing these steps, you can run the scripts using the command line or an interactive environment such as Jupyter Notebook. To open the interactive environment, navigate to the model’s folder in the command prompt window and use the command:

```python
jupyter notebook
```


The folder includes:
* Vensim models (Random Walk and SEIRb)
* Vensim Packaged Models (used with the DLL workflow)
* VST scripts
* Vensim Optimization Control files
* Python scripts
For replication, the Vensim-related files do not need to be changed, although they can be modified through the Python scripts.


Each section of the Jupyter notebooks includes several parts, some of which require adjustments to produce the desired outcomes.
* **General Settings**: The initial cell sets up configurations such as parameter names, output variables, and model timelines. You can also switch between using the DLL functionality or the script-based (VST) connection with Vensim. In addition, you can adjust basic neural network settings. Comments are provided next to each hyperparameter, explaining their definitions and functionalities.
* **Importing Libraries**: These cells import the necessary libraries for running the script and establishing the BayesFlow framework.
* **Framework Setup**: Functions to define the summary network, inference network, generative model, amortizer, and trainer are included in these cells.
* **Running Experiments**: This section includes conditions for running various experiments to observe the behavior of neural network training with respect to changes in hyperparameters. Choose which experiment to run by updating the flags (e.g., update_flags(exp_flags,[0,1,3,4,5,6,13,14],1)). You can also adjust the experimental settings. 
* **Generating Graphs**: This part contains code for generating graphs to visualize the results of the experiments. Uncomment the relevant plotting commands after enabling the experiment flags to see the results.
* **Optimized Run**: The final section contains settings for running the model with optimized hyperparameters. Modify the values as needed and run the entire script to see the results.
Both the code and the notebook include detailed comments, and the SEIRb Jupyter notebook offers brief explanations for each cell to guide users through the code.


