### Tools and utilities to be installed before starting the network
### 1.	MyCrypto Destop App
Download MyCrypto Desktop App from  https://download.mycrypto.com/

### 2.	Go Ethereum Tools
Download Go Ethereum Tools from https://geth.ethereum.org/downloads/
Select version “Geth & Tools 1.9.7” in the Stable Releases section
Decompress the downloaded zip file in the folder of the network

# Description of the network
#### Nodes and jason files are saved in "fujioka" folder
#### Network name: fujioka
#### Chain ID: 335
#### Passwords for the nodes: 10969
#### node1: Public address of the key: 0x83dB998A12AB5E416cE813cD91876e74f2Ec45Ff
#### node2: Public address of the key: 0xeF29ef94842Ece93B91EAB8EDEAf39951df83CAF

# How to start the network
#### Open a terminal (Git Bash in Windows) and navigate to the directory of the network folder, named "fujioka"
### To unlock the node1:
./geth --datadir node1 --unlock "83dB998A12AB5E416cE813cD91876e74f2Ec45Ff" --mine --minerthreads 1
#### Put the public address of the node1 within the quotation mark after --unlock. Do not include the leading "0x"   
#### Enter the password: 10969 and hit enter

### To unlock the node2
#### Open another terimal and navigate to the directory of the network folder
./geth --datadir node2 --unlock "eF29ef94842Ece93B91EAB8EDEAf39951df83CAF" --port 30304 --rpc --bootnodes "enode://{add the enode address of node1}" --ipcdisable --allow-insecure-unlock
#### Put the public address of the node2 within the quotation mark after --unlock. Do not include the leading "0x"
#### Location to find node1's enode address is shown below
![image](https://user-images.githubusercontent.com/76085861/119761788-16066880-be72-11eb-9012-7d907f3f8258.png)
#### Enter the password: 10969 and hit enter

# Configurations 
#### Open a terminal window, navigate to the directory of the network folder, and type ./puppeth Name the network
#### Select # 2. Configure new genesis
#### Select #1. Create new genesis from scratch
#### Select #2. Clique –  proof-of-authority
#### Block time: (default = 15)  just hit enter	
#### Paste both addresses of node1 and node2 to the list of accounts to seal
#### Paste both addresses again to the list of prefunded accounts.
#### Type “no” for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei
#### Type “335” as chain Id
#### Select #2 Manage existing genesis
#### Select #2 Export genesis configurations
#### To create json files, hit enter
#### After json files are created, terminate puppeth by using “Ctrl C”
#### For the further details of the configurations, see the image below  

![image](https://user-images.githubusercontent.com/76085861/119597268-4e407500-bda6-11eb-9f32-e06c208cfd1b.png)

# How to connect MyCrypto
#### Open MyCrypto desktop app., and click "Change Network" at the bottom left 
![image](https://user-images.githubusercontent.com/76085861/119598101-ee4ace00-bda7-11eb-8e0f-aa62a36130a9.png)
#### Select "fujioka" network on the left
![image](https://user-images.githubusercontent.com/76085861/119598568-cf007080-bda8-11eb-8216-ddef7ba854ef.png)
#### Click "Keystore File" at the bottom
![image](https://user-images.githubusercontent.com/76085861/119599008-bc3a6b80-bda9-11eb-9b93-2931f25f1f6a.png)
#### Click "SELECT WALLET FILE" and select Keystore file in the node1 folder
![image](https://user-images.githubusercontent.com/76085861/119599263-4551a280-bdaa-11eb-9dfd-346a33b0b591.png)
![image](https://user-images.githubusercontent.com/76085861/119599306-54385500-bdaa-11eb-8f63-255ad571f4d1.png)
#### Enter the password and click "Unlock"
![image](https://user-images.githubusercontent.com/76085861/119599346-6f0ac980-bdaa-11eb-92af-1536a9d4d506.png)

# How to send a transaction
#### Click "Send Ether & Tokens" tab at the top, and paste the public address of node2 to the "To Address" box
#### Enter the amount and click "Send Transaction" 
![image](https://user-images.githubusercontent.com/76085861/119599791-4df6a880-bdab-11eb-9040-de2dc3281bd2.png)
#### Confirm the transaction and click "Send"
![image](https://user-images.githubusercontent.com/76085861/119599894-85655500-bdab-11eb-88e6-df8cd9f1dc30.png)
#### To check the status of the transaction, click "TX Status" on the left, and enter the Transaction Hash and Click "Check TX Status"
![image](https://user-images.githubusercontent.com/76085861/119600349-7b902180-bdac-11eb-8e86-30f466d2e85f.png)




