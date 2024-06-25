### State Diagram for Wallet

| **State**        | **Event**        | **Next State**   |
|------------------|------------------|------------------|
| Initial          | Create Wallet    | Wallet Created   |
| Initial          | Import Wallet    | Wallet Imported  |
| Wallet Created   | Create Backup    | Backup Created   |
| Wallet Imported  | Create Backup    | Backup Created   |

### State Diagram for Transaction

| **State**              | **Event**             | **Next State**          |
|------------------------|-----------------------|-------------------------|
| Initial                | Create Transaction    | Transaction Created     |
| Transaction Created    | Sign Transaction      | Transaction Signed      |
| Transaction Signed     | Send Transaction      | Transaction Sent        |
| Transaction Sent       | Confirm Transaction   | Transaction Confirmed   |
| Transaction Sent       | Fail Transaction      | Transaction Failed      |

### State Diagram for Backup

| **State**         | **Event**       | **Next State**    |
|-------------------|-----------------|-------------------|
| No Backup         | Create Backup   | Backup Created    |
| Backup Created    | Restore Backup  | Backup Restored   |
