### Mininet Installation:
- We have installed mininet on Ubuntu 20.04 VM.
- Get the source code of Mininet using: ***git clone git://github.com/mininet/mininet***
- Go to the mininet folder: ***cd mininet***
- Get all the versions: ***git tag***
- Select the version you prefer: ***git checkout -b mininet-2.3.0 2.3.0***
- Come out of the current folder and Install Mininet: 
    - ***cd ..***
    - ***mininet/util/install.sh -a*** 

### POX Controller Installation:
- Get the source code: ***git clone http://github.com/noxrepo/pox***
- Go to the pox folder: ***cd pox***
- Run the Controller: ***sudo python3 pox.py forwarding.l3_learning openflow.of_01 --port=6666***
    - Default port is *6633*

### Creating and Running our Topology Using Miniedit.py:
- Run the command: ***sudo python3 mininet/mininet/examples/miniedit.py***
- It will open a GUI window where we can create our own topology by *drag and drop* method and also configure all its components.
- Before running the topology, go to: ***Edit -> Preferences***. Select ***Start CLI*** and click ***OK***.
- Run the topology by clicking on *RUN* and go to the terminal window where we have run the *miniedit* program.
- The terminal has already started the **Mininet CLI**.
- Test your network by using *ping* and *pingall* commands.
- Open one of the host's terminal using **xterm**. Sample command: ***xterm h1***
- Run the *hping3 flooding* program on the host terminal: ***sudo python3 pox/ext/hping3_flood.py 10.0.0.31***
    - Here, *10.0.0.31* is the Host IP.
    - This program will flood the network with high volumes of random ICMP packets at regular intervals, hence creating a DDoS attack.