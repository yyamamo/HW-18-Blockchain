# Tools and utilities to be installed before starting the network
### 1.	MyCrypto Destop App
Download MyCrypto Desktop App from  https://download.mycrypto.com/

### 2.	Go Ethereum Tools
Download Go Ethereum Tools from https://geth.ethereum.org/downloads/
Select version “Geth & Tools 1.9.7” in the Stable Releases section.
Decompress the downloaded zip file in the folder of the network.

# Description of the network
##### Network name: fujioka
##### Chain ID: 335
##### Passwords for nodes: 10969
##### node1: Public address of the key: 0x83dB998A12AB5E416cE813cD91876e74f2Ec45Ff
##### node2: Public address of the key: 0xeF29ef94842Ece93B91EAB8EDEAf39951df83CAF

# How to start the network.
#### Open a terminal (Git Bash in Windows) and navigate to the directory of the network folder
### To unlock the node1:
./geth --datadir node1 --unlock "0x83dB998A12AB5E416cE813cD91876e74f2Ec45Ff" --mine --minerthreads 1
##### Put the public address of the node1 within the quotation mark after --unlock   
### To unlock the node2
./geth --datadir node2 --unlock "0xeF29ef94842Ece93B91EAB8EDEAf39951df83CAF" --port 30304 --rpc --bootnodes "enode://<replace with node1 enode address>" --ipcdisable --allow-insecure-unlock
##### Put the public address of the node2 within the quotation mark after --unlock

# Configurations 
##### Open a terminal window, navigate to the directory of the network folder, and type ./puppeth Name the network
##### Select # 2. Configure new genesis
##### Select #1. Create new genesis from scratch
##### Select #2. Clique –  proof-of-authority
##### Block time: (default = 15)  just hit enter	
##### Paste both addresses of node1 and node2 to the list of accounts to seal
##### Paste both addresses again to the list of prefunded accounts.
##### Type “no” for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei.
##### Type “335” as chain Id
##### Select #2 Manage existing genesis
##### Select #2 Export genesis configurations
##### To create json files, hit enter
##### After json files are created, terminate puppeth by using “Ctrl C”
##### For the further details of the configurations, see the image below.  




# How to connect MyCrypto
