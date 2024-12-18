# Revised Jupyter Notebook for TinyML Custom Keyword Spotting (KWS)

This repository provides a fix for a jupyter notebook used for Keyword Spotting (KWS) with a custom dataset.  The notebook is used as part of Section 1.5, "Deploying a KWS Model with Your Favorite Keyword(s)" in Course 3, "Deploying TinyML".  This course is part of the <a href="https://www.edx.org/professional-certificate/harvardx-applied-tiny-machine-learning-tinyml-for-scale">Applied Tiny Machine Learning (TinyML) for Scale Professional Certificate Program</a> offered through <a href="[url](https://www.edx.org)">edx.org</a>.

Below is an image of the kit that is used in the course.

<img src="https://store-usa.arduino.cc/cdn/shop/files/AKX00028_02.unbox_643x483.jpg?v=1727104419" alt="Arduino TinyML Kit" style="width:80%;" class="center"> 

Issues arose because the code needs Tensorflow ver. 1.15. Documentation states that TF 1.15 requires either Python 3.6.x or 3.7.x, both of which are no longer supported within Google Colab (at least the free version.) 

If you would like to view the original notebook that was used in the class, it is available <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb">here.</a>

After an investigation, I decided to separate the task into two major parts.  The first notebook is to be run in Colab.  It is available by clicking <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_rev4_part1.ipynb">here.</a>  You will need to download this notebook to your own computer and then upload it into <a href="https://colab.research.google.com/">Google Colab</a>.

The second notebook needs to be run within an install of Anaconda.  I have written some documentation to get students quickly working with a local anaconda install.  (Anaconda has recently introduced a cloud based service which I have not tested, but may also work.)  This allows the user to easily define and install specific versions of Python. The second notebook is available <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_rev4_part2.ipynb">here</a>.
 
#  Using Google Colab

To use the first notebook, first sign in to Google Colab by clicking <a href="https://colab.research.google.com/">here.</a>

Once the link has loaded, you should see a pop-up window.  Go ahead and click new notebook.

Go ahead and click "connect" as located on the upper right hand side.

Go to File in the main menu and click on Upload Notebook.  A window will pop up.  Browse to the jupyter notebook "4-6-8-CustomDatasetKWSModel-rev4-part1.ipynb" which you have already saved to your drive. After a few moments of uploading, it will appear.

Well done.  You are ready to proceed with part 1.

To run the second notebook, one will have to install Andaconda on their own personal computer.  Although Anaconda is available for Windows, Linux, and MacOS, I have only tested the code on Fedora 37.  It should run on any RHEL-based OS.  

A complete list of the h/w test config, OS details, and installed conda related s/w is <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/hardware-and-software-config-and-versions">here</a>.  This may prove helpful when troubleshooting.  

#  Fedora install

If you do not have Fedora 37 installed on bare metal, consider a Virtual Machine (VM).  If you are new to VMs, I suggest <a href="https://www.virtualbox.org/">VirtualBox.</a>  Installs are available for MacOS, Linux, and Windows.  There are an abundance of tutorials available on YouTube and the web to get you started.

If you are on a Linux distro, I suggest Virtual Machine Manager.  (There is not as much support as VirtualBox, but I prefer it.)

If you need an .iso image of Fedora Workstation, it is available <a href="https://fedoraproject.org/workstation/">here.</a>  There are an abundance of tutorials available on YouTube and the web to get you started.

#  Anaconda install

Once you have Fedora setup, you will want to download Anaconda from within Fedora.  Anaconda is available <a href="https://www.anaconda.com/">here.</a>  Since you will be installing this on Fedora 37, you will want to go <a href="https://docs.anaconda.com/free/anaconda/install/linux/">here for information about the install.</a>  

As a prerequisite, you will want to run the following code from the command line from within the Fedora install:

sudo dnf install libXcomposite libXcursor libXi libXtst libXrandr alsa-lib mesa-libEGL libXdamage mesa-libGL libXScrnSaver xxd

Note that all of the packages before xxd are required to run conda.  The application xxd must be installed on Fedora for this lab.

This jupyter notebook assumes that the user follows all defaults as defined.  This is because we will be changing some of the installed python files within the virtual dev env, and we need the files to be in a specific directory.

Once you have verified your conda install, close the terminal.  Then relaunch your terminal program.

#  Create a virtual developer environment

Now that you have Anaconda installed within a Fedora 37 instance, let's create a conda virtual development environment.  This is necessary because we wish to have control over the version of python.  We will install 3.7.16. 

Feel free to download a Conda cheat sheet <a href="https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf">here</a> for reference.  (I find it comes in handy.)

To see your current list of development environments, enter

conda env list

You most likely will see only one listed, which is your base development environment.

To create a new environment with python version 3.7.16 (named myenv37) enter

conda create -n myenv37 python=3.7.16

Click enter to proceed with the install.  Once it has installed, enter the dev env with

conda activate myenv37

You are now in the new environment!

Once there, we will install Jupyter Notebook.  Do that be running the code

pip install notebook

To launch a jupyter server, enter at the command line

jupyter notebook

Well done!  Now the fun begins!

#  Running your local jupyter notebook

Navigate to the new window/tab that was launched.  (This will most likely be a new tab.)  The url will show something along the lines of "http://localhost:8888/tree".  Navigate to your saved copy of the part2 notebook, which you will click on.  It will launch in a new tab/window.

This should look somewhat like Colab.  Carry on as normal.

When you are done, save files as you normally would and close the windows/tabs.  Upon returning to the terminal from which jupyter was launched, enter ctrl-c twice.  This will close out the server.

At the command line you may at some point wish to leave the dev env.  Enter:

conda deactivate

I have found this setup to be a little finicky.  I have not found a way to install TF 1.15 from within the dev env before launching Jupyter and for the code to reliabley run.  So, TF 1.15 has to be installed each time from within the notebook.  Once completed, a user must remove the dev env and install a new dev env each time for a fresh dev env.  Don't worry.  Once you get the hang of it, it is a quick process. 

This is a little quirky, but it works.

To remove the earlier installed dev env, enter at the command line:

conda remove --name myenv37 --all

Good luck

#  Update June 22 2023

->  Same procedure as above was used, but with Fedora 38 instead of Fedora 37.  All code ran without issue.

->  Typos fixed, clarification added, deadwood removed.

