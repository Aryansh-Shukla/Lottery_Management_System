# Lottery Management System
This is a Ethereum-based Lottery Smart Contract written in **Solidity**. Participants can enter the lottery by sending 1 Ether, and once there are at least 3 participants, the manager can randomly select a winner. The entire contract operates securely using keccak256 hashing for randomization.


## 🚀 Features

🔹 Decentralized Lottery System

🔹 Manager-Controlled Operations

🔹 Fair Random Winner Selection

🔹 Secure Fund Transfer

🔹 Automatic Reset After Winner Selection

## 🛠 How It Works

1. **_Deploy the Contract_**: The person deploying the contract becomes the manager.

2. **_Participants Join:_** Users send exactly 1 Ether to enter the lottery.

3. _**Check Balance:**_ The manager can view the total lottery pool.

4. **_Generate Random Number:_** A random number is generated based on block.prevrandao, timestamp, and participants count.

5. **_Select Winner:_** The manager can select a winner once there are at least 3 participants.

6. **_Transfer Funds:_** The total balance is sent to the randomly selected winner.

7. **_Reset Lottery:_** The contract resets for a new round.

## 🏗 Deployment & Usage

### 1️⃣ Deploy the Contract

1. Use Remix IDE or Hardhat to deploy the contract on an Ethereum test network.
2. The deployer becomes the manager.

### 2️⃣ Participate in the Lottery

1. Send 1 Ether to the contract using MetaMask or any Ethereum wallet.
2. Your address will be added to the participants array.

### 3️⃣ Select a Winner

1. Only the manager can execute selectWinner().
2. The contract will randomly pick a winner and send the total balance.

### 4️⃣ Check Balance

1. Only the manager can check the current contract balance using getBalance().


## ⚠️ Security Considerations

**🔐 Fair Randomness:** The contract uses block.prevrandao instead of block.difficulty to ensure better randomness.

**🔐 Only Manager Access:** Certain functions are restricted to the contract manager to prevent unauthorized actions.

**🔐 Minimum Participants Rule:** The contract ensures at least 3 participants before selecting a winner.

## 🎯 Future Enhancements

✅ Automate Winner Selection at a fixed time interval.

✅ Support Multiple Entry Amounts for dynamic lotteries.

✅ Integrate with Frontend UI for better user experience.
