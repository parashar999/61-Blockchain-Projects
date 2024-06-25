
# Component Layout

![image](https://github.com/sharmatarun392000/Blockchain-Projects/assets/83560354/5e9e786f-7f8a-4880-9550-476965542d41)


## Components , Their Description and Responsibilities

| **Component**              | **Description**                                                                                                   | **Responsibilities**                                                                                      |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **User Interface (UI)**    | The front-end component that users interact with. Displays wallet balance and transaction history.                 | Display wallet balance and transaction history, provide forms for creating/importing wallets, facilitate sending/receiving Ether. |
| **Wallet Management**      | Handles the creation and management of user wallets. Generates new wallet addresses and imports existing wallets.  | Generate new wallet addresses, import existing wallets, encrypt and store private keys securely.          |
| **Transaction Management** | Manages all transaction-related functionalities. Creates and signs transactions, sends transactions to the Ethereum network. | Create and sign transactions, send transactions to the Ethereum network, display transaction status and details. |
| **API Gateway**            | Serves as the entry point for all client requests. Routes API requests to the appropriate backend services.        | Receive and route API requests from the client, perform initial validation and authentication of requests. |
| **Authentication Service** | Handles user authentication and authorization. Manages user sessions and tokens.                                   | Authenticate users, manage user sessions and tokens, ensure secure access to other services.              |
| **Wallet Service**         | Manages wallet-related operations such as creation, import, and key management. Stores wallet information in the database. | Create and manage wallets, store wallet information in the database, handle encryption and decryption of private keys. |
| **Transaction Service**    | Manages transactions, including sending Ether and retrieving transaction history.                                  | Send Ether transactions, calculate and provide transaction fees, retrieve and display transaction history from Etherscan. |
| **Database**               | Stores all persistent data required by the system, including user data, wallet information, and transaction history.| Store encrypted private keys, store user information and wallet details, store transaction history.       |
| **Ethereum Blockchain**    | The decentralized network where all Ether transactions are processed and recorded. Provides real-time blockchain data. | Execute and record transactions, provide real-time blockchain data.                                       |
| **Infura**                 | Provides scalable access to Ethereum nodes without the need to run your own. Facilitates interaction with the Ethereum blockchain. | Connect the wallet system to Ethereum nodes, facilitate interaction with the Ethereum blockchain.         |
| **Etherscan**              | An Ethereum block explorer and analytics platform. Provides transaction history and block information.             | Provide transaction history and block information, offer API endpoints for retrieving blockchain data.     |
