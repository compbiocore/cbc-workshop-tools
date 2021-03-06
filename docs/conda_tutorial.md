# Conda Tutorial




**What is conda?**

conda is a package manager - it allows you to build and install software on any system regardless of whether or not you have administrative priveleges.  conda is largely automated and simplifies the process of installing complex tools by automatically installing the necessary system dependencies.

Most, if not all, of the tools we use in our workshops are available through conda.  Thus, once you install conda, you will easily be able to install the other tools you need.

**Installing conda**

There are multiple versions of conda, differentiated by two things: the number of default packages that it installs, and the version of python it uses.  For our purposes, we recommend using 'miniconda' - the version of conda with the fewest default packages, to enable the most customized installation - and python 2.7.

To install miniconda, simply go to the [miniconda website](https://conda.io/miniconda.html) and select the correct version for your operating system.  miniconda is available for Windows, OS X, and Linux; the installation for Windows uses a typical .exe file, while the process on OS X and Linus is a bit more involved.  We will therefore describe the OS X (conda for Python 2) installation process here.

Rather than being a typical executible file, the conda installer for OS X (and Linux) is actually a script that must be run from the command line.  To do so, first open the terminal:

![blank terminal](https://raw.githubusercontent.com/compbiocore/cbc-workshop-tools/master/docs/assets/blank_terminal.png "Terminal")


Once you have done so, type:

	cd ~/Downloads
	bash Miniconda2-latest-MacOSX-x86_64.sh

(The filename shown here should remain correct as new releases are published, since the current release is always entitled 'latest', but if you receive an error about the file not existing you should double-check it and make sure the filename after 'bash' matches the name of the file you downloaded.)

Running this installer will lead to an interactive session wherein you are asked to accept a licensing agreement.  Do so, and accept the default options as well.

With these steps completed, conda is now installed.  One of the previous steps added conda to your 'PATH', which is the list of directories in which your computer looks for software when you type a command into the terminal.  However, this update will only take effect once you restart your terminal.  You can do so with the folllowing command:

	source ~./bash_profile

To verify that conda is installed, type:

	conda --help

If you see the conda manual, you have successfully completed the installation.
