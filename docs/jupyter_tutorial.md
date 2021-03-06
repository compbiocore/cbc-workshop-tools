# Jupyter Tutorial


To install Jupyter, please first install conda.  A link to the conda installation tutorial can be found on the sidebar to the left.

**What is Jupyter?**

Jupyter is a piece of software for interactively writing and running code in a web browser using 'notebooks'.  We use Jupyter notebooks in all of our interactive workshops, so if you're reading this, odds are you're familiar with their use and looking to configure Jupyter on your own system.

**Installing Jupyter**

The best way to install Jupyter is using the [conda package manager](https://compbiocore.github.io/cbc-workshop-tools/conda_tutorial/).  The rest of this guide will assume that you have a functioning installation of conda on the system you're using to install Jupyter.


Actually installing Jupyter is very simple - simply open a terminal and type:

	conda install jupyter

and conda will take care of the entire process!  By default, Jupyter can only run Python code; to configure it to run R code takes a few additional steps.

**Configuring Jupyter to Run R**

There are several R packages that must be installed in order to allow Jupyter to recognize R.  To prepare R, open an interactive R session and install the 'devtools' package by typing the following into R:

	install.packages("devtools")

devtools is an R package that allows you to install packages from locations other than the typical centralized repositories like CRAN and Bioconductor.  Once devtools is installed, install the 'IRkernel' package by typing:

	devtools::install_github('IRkernel/IRkernel')

This command installs the IRkernel package from the IRkernel github (the 'IRkernel/IRkernel' part is not a typo - it is specifying the github repository name and then the package name, which happen to be called the same thing).  The IRkernel package is a Jupyter R 'kernel' - a piece of software that allows Jupyter to interact with R.  Once the IRkernel package is installed, there is only one remaining step.  Once again, in your R window, type:

	IRkernel::installspec()

This command runs the installspec() function within the IRkernel package.  This command syntax, with the two colons, is a way of explicitly calling a function from within a specific package; as such, you do not need to call library() first.  installspec() will automatically configure your Jupyter R kernel based on the installation of R you have on your system.

Full documentation relating to IRkernel can be found at [their repository](https://github.com/IRkernel/IRkernel).
