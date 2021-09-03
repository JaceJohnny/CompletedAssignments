# Setting up Environments and Installing Packages Using Conda

## Summary of steps to complete

- [X] Fork this repository so you have your own copy to work on.
- [X] Clone the repository on your local machine. 
- [X] Edit this README.md file on your machine.
- [X] Run the Conda commands shown in the video and describe them in the table below.
- [X] Push your changes to your GitHub repository.
- [X] Submit a link to this GitHub repository in Canvas.

## 1. Fork & Clone this repository

* We did this in a previous assignment. Instructions are here: https://github.com/cmcntsh/exerGitPractice
* This can also be done directly in VSCode
  * Create a new folder on your machine where you want to put this repository if you don't already have one you want to use.
  * Copy the Clone or Download path for this repository from GitHub.
  * In VSCode from the command pallette (Ctrl-Shift-P) run Git: Clone
  * Paste the path into the path field which pops up
  * Select your new folder you created on your machine
  * A new folder for the repository with the repository files should be in the folder you selected showing in the Explorer window in VSCode on the left side.
  
## Edit your README.md file

* [X] In an editor of your choice (i.e. VSCode) edit this README.md file to add the answers requested in the tables.

## Follow along with this tutorial

* Conda What and Why? (27 min): https://www.youtube.com/watch?v=23aQdrS58e0&list=PLG9A6ovzPqX6d9uWzx0UYN9pm0zzl5ofA&index=13&t=0s
  * He installs Miniconda. We will be using Anaconda. Don't install Miniconda.
  * Follow along with the rest of the tutorial.
  * Go ahead and create the environments as he creates them in the tutorial.
  * (2021 update: I recommend managing environments as shown in the new Anaconda introduction video. https://anaconda.cloud/tutorials/getting-started-with-anaconda-individual-edition%3Fsource%3Dindividual-edition-tutorial) If you want to try creating the environments using the user interface for Anaconda Navigator instead of the command line shown in the Conda What and Why tutorial, that's fine. But watch the Conda What and Why tutorial to understand some of the differences between Conda environments and other types of virtual environments available in Python.

## Conda Concepts

* [X] Describe the Conda concepts used in the video and listed in the table below.

|   Concept   |         Description or short answer         |
|     ---     |                     ---                     |
|What is the purpose of having different environments?     |It allows the user access to various applications without needing additional hardware, allowing for efficiency in use.|
|What is the default package manager in Python?            |PIP|
|How do you manage environments and packages in Anaconda?  |Conda allows you to manage packages and environments within anaconda.|
|`conda list`       |(Done. A large list resulted in alphabetic order (from alabaster to zstd). Shows available packages.)|
|`conda env list`       |(base and test). Shows a lists of environments|
|How do you keep your base environment unchanged?       |(you have to create additional environments to install packages.)|
|What is the link to the Conda cheat sheet? (link in video notes is broken)      |(https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbWFSQ0Y0OHFnTGtJX0UyaHh1UVdsZHJuUkJfZ3xBQ3Jtc0ttRFpUaTl6Wl9qSWkxb3VQd1JOdUUybldEN1h5cXlkSHYwVm1sRDJjSjJJYlVLd3NSRG1jYzJoRFo0NUJIRzlWbTk5RW9KVF8tcUVTTEFzQ3VFd2puejBRekZkaXcydHZaWHFpOU9lc3RYQkZUSm1BSQ&q=https%3A%2F%2Fconda.io%2Fdocs%2F_downloads%2Fconda-cheatsheet.pdf)|
|`conda create --name XXXX`       |(It appears that I previously created a test environment.)|
|`source activate XXXX`       |('source' does not work in CLI. But 'activate test' did.')|
|`conda install YYYY`       |('conda install numpy')|
|channels in Conda       |(Package channel gives a path to determine if a package is available. Sometimes the default is unable to identify the package. You can add other channels to find packages.)|
|`conda install -c ZZZZ YYYY`       |('conda install -c pytorch pytorch')|
|`conda config --show channels`       |(channels: - defaults)|
|`conda config --add channels ZZZZ`       |(conda config --add channels pytorch)|
|conda-forge.org       |(a community led collection of packages. It is not part of the default channel however. YOu can add the channel for conda-forge by placing the code 'conda config --add channels conda-forge).|
|`source deactivate`       |(Source does not work. but 'conda deactivate' does.)|
|`conda config --get channels`       |(Channels: -defaults. [I did not add conda-forge but will if it is needed in a future assignment. My computer seems to struggle with downloading timewise.])|

* After creating the environments he created in the video on your computer, what would the results of running the command `conda env list` look like with the da35 environment activated. Paste the output from your command prompt in the code block below.

```
base                  *  C:\Users\jaced\anaconda3
DataAnalysis35           C:\Users\jaced\anaconda3\envs\DataAnalysis35
test                     C:\Users\jaced\anaconda3\envs\test


```
* What command would you use to remove the environments you created for this exercise from your computer?

```
# conda remove --DataAnalysis35

```
## 2021 Update
Python, Anaconda, and many programming languages are constantly evolving. The video Conda What and Why provides a great explanation of why you may want to use virtual environments for your Python projects, and it provides a nice demonstration of how to work in the command line. However, environment management using Anaconda Navigator is more user friently than ever. I personally will be using Anaconda Navigator to manage environments and packages since it seems easier to see what is going on using the GUI. If you haven't done so already watch the introduction to Anaconda video and pay close attention to the section on using Anaconda Navigator to create environments and install packages. https://anaconda.cloud/tutorials/getting-started-with-anaconda-individual-edition%3Fsource%3Dindividual-edition-tutorial
