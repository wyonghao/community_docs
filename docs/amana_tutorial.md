# Amana Deployment Tutorial (using Amana Privnet Launcher)

## Install Go
Instructions regarding the downloading & installation of Go can be found on its official site: https://go.dev/doc/install. Alternatively, if Snap is enabled (such as if you're running a Ubuntu distribution) you can download and install the latest version of Go via the command: `sudo snap install go --classic`

## Clone `qng` source code
Clone the source code directly from Qitmeer's `qng` repository (https://github.com/Qitmeer/qng) selecting the `dev/2.0` branch: `git clone https://github.com/Qitmeer/qng.git -b dev/2.0`

## Install `qng` Dependencies
Tools such as `make` need to installed to successfully compile the `qng` binary. If `apt` is already installed, you can the run the command to install the neccesary dependencies: `sudo apt install build-essential`.

## Install Python Dependencies
The script requires the installation of some Python dependencies. Before installing any dependencies, is strongly suggested to create a `virtualenv` to isolate dependencies between seperate projects. A `virtualenv` called `venv` can be created by running `python3 -m venv venv`. 

There is a seperate file listing all the neccesary dependencies named `requirements.txt`. This can be fed into `pip` to install all dependencies at once: `pip install -r requirements.txt`.   

## Run Script
By default, the script would generate a 3-node network on localhost. All three act as *sealers* (these nodes are responsible for producing blocks on the network) although deciding who can be a sealer can be configured from within the script. 

To run the script: `python3 launch-privnet.py`.