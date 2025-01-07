# TREX-PHY584: Ministage in HH to bbtautau

This repository contains documentation and instructions for setting up the working environment for the PHY584 course HH to bbtautau at the LHC.

---

## The LHC Complex

## The CMS Experiment

## Setting Up the Working Environment

### One-Time Setup

You should first set up your laptop in a way that you can connect to the LLR servers and use the Jupyter notebook from the outside. For this, you need to create a SSH key and upload it to any LLR server. If you are using an operating system of the Microsoft Windows family, you can install Ubuntu via the Linux Subsystem for Windows and start a terminal emulator this way.

1. **Create an SSH key**:  
   Open a terminal and run:
   ```bash
   ssh-keygen
   
2. **Copy the SSH key to the server**:  
   Run:
   ```bash
   ssh-copy-id -i ~/.ssh/id_rsa appro2@polui01.in2p3.fr

3. **Connect to the Tunneling Machine**:  
   Run:
   ```bash
   ssh -Y appro2@llrgate01.in2p3.fr
4. **Connect to the Working Machine**:  
   Run:
   ```bash
   ssh -Y appro2@polui01.in2p3.fr
5. **Activate the Environment**:
   ```bash
   conda activate py37
6. **Open a Jupyter notebook**
   ```bash
   notebook
   ```
   This should prompt you a link of this kind:
   ```bash
   http://134.158.128.183:<port_number>/?token=7a6d205f71ec2eea66ae613ee3a969e71314ebef3d255989
   ```
   Now open a second terminal window and run the following:
   ```bash
   ssh -L<port_number>:polui01.in2p3.fr:<port_number> appro2@llrgate01.in2p3.fr
   ```
   Now you can past the link inside your favourite browser substituting `134.158.128.183` with `localhost`.  
   The magic is done: the Jupyter Notebook should be open and running
   
