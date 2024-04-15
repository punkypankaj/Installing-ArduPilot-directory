# Installing ArduPilot Directory

# Detailed Youtube Video Link

https://youtu.be/9cYW2FwJXg4


# Clone ArduPilot Repo
Clone this in the home directory

    git clone --recurse-submodules https://github.com/Ardupilot/ardupilot.git  

    cd ardupilot
    
    
    
   

We need to install few python3 dependencies and also other dependencies that we require. Requirement sheet contains all the packages.

    Tools/environment_install/install-prereqs-ubuntu.sh -y


Reload the path (log-out and log-in to make permanent):

    . ~/.profile

Now lets source it by editing the bashrc file
     
    gedit ~/.bashrc
    
Add this lines at the end of bashrc file   
    
    export PATH=$PATH:$HOME/ardupilot/Tools/autotest
    export PATH=/usr/lib/ccache:$PATH
   
Save and close the text editor

now reload it once

    . ~/.bashrc
    
# Run Simulator

    cd ~/ardupilot/ArduCopter
    sim_vehicle.py -w
    
    
