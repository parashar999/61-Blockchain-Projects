### Sequence Diagram 1: Wallet Creation

**Description**: This sequence diagram shows the steps involved when a user creates a new wallet.

#### Steps:
1. User initiates wallet creation via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service generates a new wallet (public-private key pair).
5. Wallet Service stores the wallet information in the Database.
6. Wallet Service sends wallet details back to the API Gateway.
7. API Gateway sends wallet details to the UI.
8. UI displays the wallet information to the user.

![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/a57f06b8-5dfe-4264-9862-195be61a3382)


### Sequence Diagram 2: Import Wallet

**Description**: This sequence diagram shows the steps involved when a user imports an existing wallet.

#### Steps:
1. User initiates wallet import via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service validates the private key and imports the wallet.
5. Wallet Service stores the wallet information in the Database.
6. Wallet Service sends wallet details back to the API Gateway.
7. API Gateway sends wallet details to the UI.
8. UI displays the wallet information to the user.

```plaintext
User -> UI: Initiate Wallet Import
UI -> API Gateway: Request Wallet Import
API Gateway -> Wallet Service: Import Wallet
Wallet Service -> Wallet Service: Validate Private Key
Wallet Service -> Database: Store Wallet Information
Database -> Wallet Service: Confirmation
Wallet Service -> API Gateway: Return Wallet Details
API Gateway -> UI: Return Wallet Details
UI -> User: Display Wallet Information
```

### Sequence Diagram 3: Send Ether

**Description**: This sequence diagram shows the steps involved when a user sends Ether.

#### Steps:
1. User initiates an Ether transfer via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Transaction Service.
4. Transaction Service creates and signs the transaction.
5. Transaction Service sends the transaction to the Ethereum Blockchain via Infura.
6. Infura processes the transaction and returns a transaction hash.
7. Transaction Service stores the transaction details in the Database.
8. Transaction Service sends the transaction hash back to the API Gateway.
9. API Gateway sends the transaction hash to the UI.
10. UI displays the transaction status to the user.

```plaintext
User -> UI: Initiate Ether Transfer
UI -> API Gateway: Request Ether Transfer
API Gateway -> Transaction Service: Process Ether Transfer
Transaction Service -> Transaction Service: Create and Sign Transaction
Transaction Service -> Infura: Send Transaction
Infura -> Transaction Service: Return Transaction Hash
Transaction Service -> Database: Store Transaction Details
Database -> Transaction Service: Confirmation
Transaction Service -> API Gateway: Return Transaction Hash
API Gateway -> UI: Return Transaction Hash
UI -> User: Display Transaction Status
```

### Sequence Diagram 4: Receive Ether

**Description**: This sequence diagram shows the steps involved when a user receives Ether.

#### Steps:
1. User checks wallet address via the UI.
2. UI retrieves the wallet address from the Wallet Service.
3. User shares wallet address to sender.
4. Sender sends Ether to the user's wallet address.
5. Transaction is processed by the Ethereum Blockchain.
6. Infura notifies the Transaction Service of the incoming transaction.
7. Transaction Service retrieves transaction details from Infura.
8. Transaction Service stores the transaction details in the Database.
9. Transaction Service sends transaction details to the API Gateway.
10. API Gateway sends transaction details to the UI.
11. UI updates the user's balance and transaction history.

```plaintext
User -> UI: Check Wallet Address
UI -> API Gateway: Request Wallet Address
API Gateway -> Wallet Service: Retrieve Wallet Address
Wallet Service -> API Gateway: Return Wallet Address
API Gateway -> UI: Return Wallet Address
UI -> User: Display Wallet Address
Sender -> Ethereum Blockchain: Send Ether
Ethereum Blockchain -> Infura: Process Transaction
Infura -> Transaction Service: Notify Incoming Transaction
Transaction Service -> Infura: Retrieve Transaction Details
Infura -> Transaction Service: Return Transaction Details
Transaction Service -> Database: Store Transaction Details
Database -> Transaction Service: Confirmation
Transaction Service -> API Gateway: Send Transaction Details
API Gateway -> UI: Send Transaction Details
UI -> User: Update Balance and Transaction History
```

### Sequence Diagram 5: View Transaction History

**Description**: This sequence diagram shows the steps involved when a user views their transaction history.

#### Steps:
1. User requests to view transaction history via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Transaction Service.
4. Transaction Service retrieves transaction history from the Database.
5. Transaction Service retrieves additional transaction details from Etherscan.
6. Transaction Service compiles the transaction history and details.
7. Transaction Service sends the transaction history to the API Gateway.
8. API Gateway sends the transaction history to the UI.
9. UI displays the transaction history to the user.

```plaintext
User -> UI: View Transaction History
UI -> API Gateway: Request Transaction History
API Gateway -> Transaction Service: Retrieve Transaction History
Transaction Service -> Database: Retrieve Transaction History
Database -> Transaction Service: Return Transaction History
Transaction Service -> Etherscan: Retrieve Additional Details
Etherscan -> Transaction Service: Return Transaction Details
Transaction Service -> API Gateway: Send Transaction History
API Gateway -> UI: Send Transaction History
UI -> User: Display Transaction History
```

### Sequence Diagram 6: Balance Inquiry

**Description**: This sequence diagram shows the steps involved when a user checks their wallet balance.

#### Steps:
1. User requests to check wallet balance via the UI.
2. UI sends a request to the API Gateway.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service retrieves the wallet balance from the Ethereum Blockchain via Infura.
5. Wallet Service sends the wallet balance to the API Gateway.
6. API Gateway sends the wallet balance to the UI.
7. UI displays the wallet balance to the user.

```plaintext
User -> UI: Check Wallet Balance
UI -> API Gateway: Request Wallet Balance
API Gateway -> Wallet Service: Retrieve Wallet Balance
Wallet Service -> Infura: Retrieve Balance from Blockchain
Infura -> Wallet Service: Return Wallet Balance
Wallet Service -> API Gateway: Return Wallet Balance
API Gateway -> UI: Return Wallet Balance
UI -> User: Display Wallet Balance
```
### Sequence Diagram 7: Create Backup

**Description**: This sequence diagram shows the steps involved when a user creates a backup of their wallet.

Steps:
1. User initiates the backup creation process via the UI.
2. UI sends a request to the API Gateway to create a backup.
3. API Gateway forwards the request to the Wallet Service.
4. Wallet Service retrieves the wallet data from the Database.
5. Wallet Service encrypts the wallet data.
6. Wallet Service generates a backup file.
7. Wallet Service sends the backup file to the API Gateway.
8. API Gateway sends the backup file to the UI.
9. UI provides the backup file to the user for download.
```plaintext
User -> UI: Initiate Backup Creation
UI -> API Gateway: Request Backup Creation
API Gateway -> Wallet Service: Create Backup
Wallet Service -> Database: Retrieve Wallet Data
Database -> Wallet Service: Return Wallet Data
Wallet Service -> Wallet Service: Encrypt Wallet Data
Wallet Service -> Wallet Service: Generate Backup File
Wallet Service -> API Gateway: Return Backup File
API Gateway -> UI: Return Backup File
UI -> User: Provide Backup File for Download
```
