### Level 0 DFD (Context Diagram)

| **Entity**          | **Data Flow**                  | **System**                  |
|---------------------|--------------------------------|-----------------------------|
| User                | User Actions                   | Cryptocurrency Wallet System|
| Cryptocurrency Wallet System | Wallet Info, Transaction Status | User                        |
| Cryptocurrency Wallet System | Transaction Requests  | Ethereum Blockchain         |
| Ethereum Blockchain | Transaction Status            | Cryptocurrency Wallet System|
| Cryptocurrency Wallet System | Data Requests         | External APIs (Infura, Etherscan) |
| External APIs       | Data Responses                | Cryptocurrency Wallet System|

### Level 1 DFD: Wallet Management

| **Process**              | **Data Flow In**                   | **Data Flow Out**            | **Data Store**            |
|--------------------------|------------------------------------|------------------------------|---------------------------|
| Wallet Management        | Create Wallet Request, Import Wallet Request | Wallet Details                | User Data, Wallet Data    |
| User Data                | Store Wallet Info                  | Retrieve Wallet Info          | Wallet Data               |

### Level 1 DFD: Transaction Processing

| **Process**              | **Data Flow In**                   | **Data Flow Out**            | **Data Store**            |
|--------------------------|------------------------------------|------------------------------|---------------------------|
| Transaction Processing   | Transaction Request                | Transaction Confirmation      | Transaction Data          |
| Ethereum Blockchain      | Send Transaction                   | Receive Transaction Status    |                           |

### Level 1 DFD: Key Management

| **Process**              | **Data Flow In**                   | **Data Flow Out**            | **Data Store**            |
|--------------------------|------------------------------------|------------------------------|---------------------------|
| Key Management           | Generate Key Request, Import Key Request | Key Details                  | Key Data                  |
| Key Data                 | Store Key Info                     | Retrieve Key Info            |                           |

### Level 1 DFD: Balance Inquiry

| **Process**              | **Data Flow In**                   | **Data Flow Out**            | **Data Store**            |
|--------------------------|------------------------------------|------------------------------|---------------------------|
| Balance Inquiry          | Balance Request                    | Balance Information          | Wallet Data               |
| Ethereum Blockchain      | Fetch Balance                      | Return Balance               |                           |

### Level 1 DFD: View Transaction History

| **Process**              | **Data Flow In**                   | **Data Flow Out**            | **Data Store**            |
|--------------------------|------------------------------------|------------------------------|---------------------------|
| View Transaction History | Transaction History Request        | Transaction History Details  | Transaction Data          |
| Etherscan API            | Fetch Transaction History          | Return Transaction Details   |                           |

### Level 1 DFD: Create Backup

| **Process**              | **Data Flow In**                   | **Data Flow Out**            | **Data Store**            |
|--------------------------|------------------------------------|------------------------------|---------------------------|
| Create Backup            | Backup Request                     | Encrypted Backup File        | Wallet Data, Key Data     |
| Wallet Data              | Retrieve Wallet Info               | Provide Wallet Info          |                           |
| Key Data                 | Retrieve Key Info                  | Provide Key Info             |                           |
