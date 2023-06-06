# Alternative Set of Jupyter Notebooks for TinyML Custom Keyword Spotting (KWS)

<img src="https://canadianmedicalteams.org/wp-content/uploads/2013/10/Website-Under-Construction-template1.jpg" alt="Under Construction">


This repository is devoted to providing a fix for a set of jupyter notebooks used for Keyword Spotting (KWS).  The original notebook would no longer run due to the need to use Tensorflow 1.15 and the inability of Colab to permit the use of Python 3.6.c or 3.7.x.  

The notebooks are used as part of Section 1.5, "Deploying a KWS Model with Your Favorite Keyword(s)" of Course 3, Deploying TinyML.  This course is part of the <a href="https://www.edx.org/professional-certificate/harvardx-applied-tiny-machine-learning-tinyml-for-scale">Applied Tiny Machine Learning (TinyML) for Scale Professional Certificate Program</a> offered through <a href="[url](https://www.edx.org)">edx.org</a>.

<a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb">The original jupyter notebook that was used in the class is available by clicking here.</a>

After much investigation, I decided to separate the task into two major parts.  The first notebook is designed to be run in colab.  <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb">It is available by clicking here.</a>  You will have to download this notebook to your own computer and then upload into <a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb">Google Colab.</a>

<a href="https://github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb">The original jupyter notebook that was used in the class is available by clicking here.</a>
 

https://colab.research.google.com/github.com/john-mangiaracina/TinyML-CustomKeywordSpotting/blob/main/4_6_8_CustomDatasetKWSModel_original_file.ipynb

To complete the second set of tasks and run the second notebook, one will first have to install Andaconda on their own personal computer.  Although Anadaconda is available for Windows, Linux, and MacOS, I have to date only released a version for the RHEL-based Linux OS.  The second notebook has been tested on Fedora 37, although it should run on any RHEL-based OS.  If there is interest, I might draft an alternative notebook for Debian-based distros.

A complete list of the h/w test config, OS details, and installed conda related s/w is here.

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

