# blockchain-assignment-by-shubham-singh
# IPFS DOWNLOAD STEP

🔹 **Step 1**: Go to the official website  
Visit: [https://docs.ipfs.tech/install/ipfs-desktop/](https://docs.ipfs.tech/install/ipfs-desktop/)

---

🔹 **Step 2**: Download IPFS Desktop  
Choose the right version for your operating system:


---

🔹 **Step 3**: Install it  
For Windows: Run the `.exe` and follow the installer.

---

🔹 **Step 4**: Run IPFS Desktop  
Open the app — it will start the IPFS daemon and give you a friendly GUI to interact with your node.

- **Windows**: Add the `ipfs.exe` directory to your system's `PATH` environment variable.  
- **Desktop**: Open the app, it should show your peer ID and connected nodes.

---
![image 1](https://github.com/user-attachments/assets/e6144e63-1389-4613-b87b-e3e4ceb2fd74)

# File Upload

To upload a file:

1. Navigate to the **Files** section within IPFS Desktop.  
2. Click the **+ Import** button.  
3. Upload files (like a presentation, e.g. SQL Notes).  

Once uploaded, IPFS automatically generates a unique CID (Content Identifier) for each file.

---

![image 2](https://github.com/user-attachments/assets/239a7786-be77-4aa7-b944-77bff2fd4384)


---

# Assignment 5: IPFS Privacy and Encryption

This assignment demonstrates how to use the **InterPlanetary File System (IPFS)** along with **OpenSSL** to perform file encryption and ensure privacy for the uploaded content.

---
# Steps
# 1. Create a file to be added to IPFS
```

echo "Hello, IPFS!" > myfile.txt
```
<br>

# 2.Add the original file to IPFS
```

ipfs add myfile.txt
```
# 3.Encrypt the file using OpenSSL (AES-256-CBC)
```

openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -salt -in myfile.txt -out myfile_encrypted.txt -pass pass:yourpassword
```
# 4.Add the encrypted file to IPFS
```

ipfs add myfile_encrypted.txt
```
# 5.View the encrypted file (optional)
```

cat myfile_encrypted.txt
```
# 6.Decrypt the file
```

openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -in myfile_encrypted.txt -out decrypted_file.txt -pass pass:yourpassword
```
# 7.Verify the decrypted file content
```

cat decrypted_file.txt
```
# 8.Add the decrypted file to IPFS
```

ipfs add decrypted_file.txt
```

![image 3](https://github.com/user-attachments/assets/cb660e74-5c6e-4b42-98d5-469d8c554df7)



 # Notes
● Replace `yourpassword` with a strong, secure password of your choice.
<br>
● Ensure that IPFS is properly installed and initialized before running these commands.
# Blockchain Practical - MetaMask Wallet & Sepolia Testnet

This repo contains my blockchain practical work for creating a MetaMask wallet, receiving Sepolia test ETH, and making a transaction on the Sepolia testnet.

---

## 🔐 MetaMask Wallet Creation (Sepolia Testnet)

### Introduction
In this practical, I created a MetaMask wallet and performed a transaction using the Sepolia testnet. This includes setting up MetaMask, connecting to Sepolia, claiming test ETH from the faucet, and sending a transaction.

---

## ✅ Transaction Details

- **Network:** Sepolia Testnet  
- **Amount Sent:** 0.01 ETH  
- **Transaction Hash:**  
`0xa64bf5b7ddcd28172e6f536a78806045c60b25489057507aaa7268527de8afc3` 
[🔗 View on Etherscan](https://sepolia.etherscan.io/tx/0xa64bf5b7ddcd28172e6f536a78806045c60b25489057507aaa7268527de8afc3)  
- **Status:** Successful ✅

---
## 💸 Getting Sepolia ETH from Faucet

1. Opened the Sepolia Faucet hosted on Google Cloud.
2. Logged in using my Google account.
3. Copied and pasted my MetaMask wallet address into the input field.
4. Clicked on **"Request 0.05 ETH"**.
5. ETH was successfully sent to my wallet in a few seconds.
6. Verified the deposit by checking on Sepolia Etherscan.

### 📸 Screenshot:
Sepolia Faucet transaction request page:
![image 4](https://github.com/user-attachments/assets/0ec4a5ec-1d9d-4142-8c53-735fa0171300)

---

## 🔁 Steps Followed for the Transaction

1. Installed MetaMask extension on my browser.
2. Created a new wallet and backed up the Secret Recovery Phrase.
3. Connected MetaMask to **Sepolia Testnet** (added custom network manually).
4. Claimed **test ETH** from the faucet.
5. Sent **0.03 ETH** to another wallet address using MetaMask.
6. Verified transaction success on Sepolia Etherscan.

---
## 📤 Transaction Screenshot

Below is the screenshot showing the transaction confirmation inside MetaMask:
![image 5](https://github.com/user-attachments/assets/28aa0bdf-668c-44d0-89ba-1063c9eee784)
---

> Created by: *[Shubham Singh]*  

# Hyperledger-Fabric

## 1. Install Golang  
```bash
sudo apt install golang-go
```
Installs Golang, which is necessary for running Hyperledger Fabric binaries.

## Screenshot 

![image 6](https://github.com/user-attachments/assets/38d854d4-23d0-46ae-b7e8-2db941843c5b)

---

## 2. Check Docker Version  
```bash
docker --version
```
Verifies that Docker is installed and running correctly.

## Screenshot 
![image 7](https://github.com/user-attachments/assets/d2369d0e-75db-407a-b45d-d77cf4c9ae8c)
_

---

## 3. Check Docker Compose Version  
```bash
docker compose version
```
Verifies the installation of Docker Compose.

## Screenshot
![image 8](https://github.com/user-attachments/assets/697dcb58-b9d2-4068-bebd-47689f1d8ce3)



---

## 4. List Files in Current Directory  
```bash
ls
```
Shows the list of files and folders in the current directory.

---

## 5. Clone the Fabric Samples Repository and Move into the Cloned Folder  
```bash
git clone https://github.com/fabric-samples.git; cd fabric-samples
```
Downloads the official Hyperledger Fabric sample code from GitHub.  
Enters the cloned folder where Fabric examples are available.

## Screenshot 
![image 10](https://github.com/user-attachments/assets/a55ab6e6-d8f8-4c98-a94d-f6b310b97152)



---

## 6. Download Fabric Binaries  
```bash
curl -sSL https://bit.ly/2ysbOFE | bash -s
```
Downloads necessary Fabric binaries and Docker images like peer, orderer, and cryptogen.

## Screenshot
![image 11](https://github.com/user-attachments/assets/e3eab6a7-a89b-426d-8aab-b618dfb6b8a4)
![image 12](https://github.com/user-attachments/assets/a6cc56f8-b537-4ba5-a459-95e3a8d05988)
![image 13](https://github.com/user-attachments/assets/1e87c5fe-fe51-4858-b64a-b212d325a169)




---

## 7. Enter the Test Network Directory  
```bash
cd test-network
```
Navigates to the directory that contains scripts for running a sample Fabric network.

## Screenshot
![image 14](https://github.com/user-attachments/assets/c4b35d77-66ea-493e-89f8-f95cbc9cea5a)


---

## 8. View the Network Script  
```bash
./network.sh
```
Shows the options available with the `network.sh` script.

## Screenshot
![image 15](https://github.com/user-attachments/assets/a1674006-c577-449c-9f4f-1dcfd9fb6228)
![image 16](https://github.com/user-attachments/assets/f321a9dc-63ff-48cb-9724-ef2878c406e8)



---

## 9. Start the Fabric Network  
```bash
./network.sh up
```
Starts the network by launching peer, orderer, and CA containers, and generates the required cryptographic materials.

## Screenshot 
![image 17](https://github.com/user-attachments/assets/b0d9229e-9c6f-48bc-be8e-33c1608bac42)




---

## 10. Create a Channel  
```bash
./network.sh createChannel
```
Creates a default channel (usually named `mychannel`) and joins the peers to it.
## Screenshot 

![image 18](https://github.com/user-attachments/assets/b6473f66-e87c-4176-992b-6d94e1995aaa)
![image 19](https://github.com/user-attachments/assets/6ec3a61a-ec82-4af4-910a-f2b36944ebac)



---

## 11. Shut Down the Network  
```bash
./network.sh down
```
Stops all containers and deletes the crypto material and artifacts created during the setup.

## Screenshot 
![image 20](https://github.com/user-attachments/assets/d701c39d-7508-4765-a115-ddbf1792a71c)



# SOLIDITY
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

/*
HelloWorld Solidity Smart Contract - Beginner Tutorial

💻 SETTING UP THE ENVIRONMENT:

1. Open the Remix IDE in your browser: https://remix.ethereum.org  
   (No installation required — everything runs in the browser.)

📁 CREATE A NEW CONTRACT FILE:

2. In Remix:
   - Click the "File Explorer" icon on the left sidebar.
   - Click the "+" button to create a new file.
   - Name your file: HelloWorld.sol

🧾 WRITE YOUR SMART CONTRACT:

3. You can either:
   - Paste the code provided below, or
   - Type it manually to better understand each line.

🛠️ COMPILE THE CONTRACT:

4. Click the "Solidity Compiler" tab (3rd icon in sidebar).
   - Select compiler version 0.8.0 or above.
   - Click the "Compile HelloWorld.sol" button.

🚀 DEPLOY THE CONTRACT:

5. Navigate to the "Deploy & Run Transactions" tab (4th icon).
   - Set the environment to **JavaScript VM (London)**.
   - Click the orange **Deploy** button.

🧪 INTERACT WITH THE CONTRACT:

6. After deployment, under "Deployed Contracts":
   - a. Click the `greeting` function to see the current message.
   - b. To update the greeting:
       - Enter a new message in the `updateGreeting` field.
       - Click the **transact** button (only the owner can update it).

📜 SMART CONTRACT CODE:
*/

contract HelloWorld {
    string public greeting;
    address public owner;

    constructor() {
        greeting = "Hello Web3 World!";
        owner = msg.sender;
    }

    function updateGreeting(string memory newGreeting) public {
        require(msg.sender == owner, "Only the contract owner can update the greeting.");
        greeting = newGreeting;
    }
}

/*
🛠️ CUSTOMIZATION OPTIONS:
- Set a different default greeting message in the constructor.
- Rename the contract from `HelloWorld` to something relevant to your project.
- Change function names like `updateGreeting` to match your app's terminology.
- Add additional public or private functions based on requirements.

🔐 SECURITY OPTIONS:
- Implement time-lock mechanisms for sensitive changes.
- Require multi-signature approval for updates.
- Use a proxy pattern for upgradable contracts.

🚀 NEXT STEPS:
- Emit events for key actions (e.g., GreetingUpdated).
- Write unit tests in JavaScript using frameworks like Mocha/Chai or Hardhat.
- Deploy the contract to a public Ethereum testnet (e.g., Goerli or Sepolia).
*/









# Blockchain-Practicals
## Question 1
Create a voting system with multiple candidates. Each address can vote only once.
## Code

