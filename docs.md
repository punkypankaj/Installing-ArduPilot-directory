# Installing ArduPilot Directory

# Clone ArduPilot Repo
Clone this in the home directory

    git clone https://github.com/ArduPilot/ardupilot.git
    
    cd ardupilot
    
    git checkout Copter-3.6
    
    git submodule update --init --recursive

We need to install few python dependencies and also other dependencies that we require.

    sudo apt install python-matplotlib python-serial python-wxgtk3.0 python-wxtools python-lxml python-scipy python-opencv ccache gawk python-pip python-pexpect
    
    sudo pip install future pymavlink MAVProxy

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
    
    
