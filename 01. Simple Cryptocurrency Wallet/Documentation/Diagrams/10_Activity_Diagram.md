### Activity Diagram for Wallet Creation

1. **Start**
2. **User Input**: User initiates wallet creation.
3. **Validate Input**: System validates user input.
4. **Generate Keys**: Wallet Service generates key pair.
5. **Store in Database**: Save wallet details in the database.
6. **Display Wallet Info**: Show wallet info to user.
7. **End**

### Activity Diagram for Wallet Import

1. **Start**
2. **User Input**: User initiates wallet import.
3. **Validate Private Key**: System validates the private key.
4. **Store Wallet Info**: Save wallet details in the database.
5. **Display Wallet Info**: Show wallet info to user.
6. **End**

### Activity Diagram for Sending Ether

1. **Start**
2. **User Input**: User initiates Ether transfer.
3. **Validate Input**: System validates transaction details.
4. **Create and Sign Transaction**: Transaction Service creates and signs the transaction.
5. **Send Transaction**: Transaction sent to the Ethereum network via Infura.
6. **Store Transaction Details**: Save transaction details in the database.
7. **Display Transaction Status**: Show transaction status to user.
8. **End**

### Activity Diagram for Receiving Ether

1. **Start**
2. **Check Wallet Address**: User checks wallet address.
3. **Share Wallet Address**: User shares wallet address with sender.
4. **Sender Sends Ether**: Sender initiates Ether transfer.
5. **Process Transaction**: Transaction processed by Ethereum blockchain.
6. **Notify Incoming Transaction**: Infura notifies Transaction Service of incoming transaction.
7. **Update Balance and Transaction History**: Transaction Service updates balance and transaction history in the database.
8. **Display Updated Balance and Transaction History**: UI displays updated balance and transaction history to user.
9. **End**

### Activity Diagram for Viewing Transaction History

1. **Start**
2. **User Request**: User requests to view transaction history.
3. **Retrieve Transaction History from Database**: Transaction Service retrieves transaction history from the database.
4. **Retrieve Additional Details from Etherscan**: Transaction Service retrieves additional transaction details from Etherscan.
5. **Display Transaction History**: UI displays transaction history to user.
6. **End**

### Activity Diagram for Balance Inquiry

1. **Start**
2. **User Request**: User requests to check wallet balance.
3. **Retrieve Balance from Blockchain**: Wallet Service retrieves balance from the Ethereum blockchain via Infura.
4. **Display Balance**: UI displays the wallet balance to user.
5. **End**

### Activity Diagram for Creating Backup

1. **Start**
2. **User Request**: User initiates backup creation.
3. **Retrieve Wallet Data**: Wallet Service retrieves wallet data from the database.
4. **Encrypt Wallet Data**: Wallet Service encrypts wallet data.
5. **Generate Backup File**: Wallet Service generates a backup file.
6. **Provide Backup File for Download**: UI provides the backup file for user to download.
7. **End**
``
