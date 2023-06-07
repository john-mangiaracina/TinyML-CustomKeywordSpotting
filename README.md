# Revised Jupyter Notebook for TinyML Custom Keyword Spotting (KWS)

<img src="https://canadianmedicalteams.org/wp-content/uploads/2013/10/Website-Under-Construction-template1.jpg" alt="Under Construction">


This repository is devoted to providing a fix for a jupyter notebooks used for Keyword Spotting (KWS) which would no longer run within Google Colab.  The notebook is used as part of Section 1.5, "Deploying a KWS Model with Your Favorite Keyword(s)" in Course 3, "Deploying TinyML".  This course is part of the <a href="https://www.edx.org/professional-certificate/harvardx-applied-tiny-machine-learning-tinyml-for-scale">Applied Tiny Machine Learning (TinyML) for Scale Professional Certificate Program</a> offered through <a href="[url](https://www.edx.org)">edx.org</a>.

Below is an image of the embedded dev board that is used in the course
<img src="https://cdn.shopify.com/s/files/1/0506/1689/3647/products/ABX00031_03.front_643x483.jpg?v=1626445224" alt="Arduino Nano 33 BLE Sense board"> 

The original notebook would no longer run due to the need to use Tensorflow version 1.15 and the lack of support for Python 3.6.x or 3.7.x within Google Colab.  These versions of Python are required to use Tensorflow 1.15.  

If you would like to view the original jupyter notebook that was used in the class, it is available by <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb">clicking here.</a>

After a detailed investigation, I decided to separate the task into two major parts.  The first notebook is designed to be run in Colab.  It is available by clicking <a href="https://github.com/john-mangiaracina/4-6-8-CustomDatasetKWSModel-rev2-part1.ipynb">here.</a>  You will have to download this notebook to your own computer and then upload into <a href="https://colab.research.google.com/">Google Colab.</a>

If you are interested in a copy of the original jupyter notebook that was used in the class, it is available by clicking <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb">here.</a>
 
#  Using Google Colab

To use the first notebook, first sign in to Google Colab by clicking <a href="https://colab.research.google.com/">here.</a>

Once the link has loaded, you should see a pop-up window.  Go ahead and click new notebook.

Go ahead and click "connect" as located on the upper right hand side.

Go to File in the main menu and click on Upload Notebook.  A window will pop up and go ahead and browse to the jupyter notebook "4-6-8-CustomDatasetKWSModel-rev2-part1.ipynb" which you have already saved to your drive. After a few moments of uploading, it will appear.

Well done.  You are ready to proceed with part 1.

To complete the second set of tasks and run the second notebook, one will have to install Andaconda on their own personal computer.  Although Anaconda is available for Windows, Linux, and MacOS, I have only tested the code on a version of Fedora 37.  It should run on any RHEL-based OS.  

A complete list of the h/w test config, OS details, and installed conda related s/w is <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/hardware-and-software-config-and-versions">here.</a>

#  Fedora install

If the user does not have access to a system running Fedora, they should use a VM.  The solution was tested on a system running Fedora on bare metal, but this is not required.  If you do not have Fedora installed on bare metal, consider a Virtual Machine (VM).  If you do not have a preference and especially if you are new to VMs, I suggest <a href="https://www.virtualbox.org/">VirtualBox.</a>  Installs are available for MacOS, Linux, and Windows.  There are an abundance of tutorials available to get you started.

If you need an .iso image of Fedora Workstation, it is available <a href="https://fedoraproject.org/workstation/">here.</a>  There are an abundance of tutorials available to get you started.

#  Anaconda install

Once you have Fedora setup, you will want to download Anaconda from within Fedora.  Anaconda is available <a href="https://www.anaconda.com/">here.</a>  Since you will be installing this on Fedora, you will want to go <a href="https://docs.anaconda.com/free/anaconda/install/linux/">here for information about the install.</a>  

As a prerequisite, you will want to run the following code:

sudo dnf install libXcomposite libXcursor libXi libXtst libXrandr alsa-lib mesa-libEGL libXdamage mesa-libGL libXScrnSaver xxd

from the command line.  I am recommending you do the install with sudo because you will not want to install anaconda from root.  Note the first series of executable code is required to run anaconda, and the last application xxd is required to be system installed for this lab.

This jupyter notebook assumes that the user follows all defaults.  This is because we will be changing some of the installed conda files and we need the files to be in the correct directory for the code to run correctly.

Once you have verified your conda install, close the terminal.  Then launch your terminal program again.

Now, the fun begins!

#  Create a virtual developer environment

Now that 

