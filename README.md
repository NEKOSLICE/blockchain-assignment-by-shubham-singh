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

## 🔧 Steps

### 1. Create a file to be added to IPFS

```bash
echo "Hello, IPFS!" > myfile.txt
