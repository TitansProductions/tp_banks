# Development API

## Exports

**Getter**
The specified export below is used on the `server` to use the API properly and faster.

```lua
local BankAPI = exports.tp_banks:getAPI()
```

| Export                                                                    | Description                                                                                                                                                                                                                | Returned Type |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| `BankAPI.getPlayerIBAN(source, identifier, charIdentifier)`               | Returns the player primary (main) IBAN Account. If source is available, having identifier and charIdentifier as null is acceptable but if there is no source available, identifier and charIdentifier are required.        | String        |
| `BankAPI.getPlayerJointAccountIBAN(source, identifier, charIdentifier)`   | Returns the player Joint IBAN Account (if available). If source is available, having identifier and charIdentifier as null is acceptable but if there is no source available, identifier and charIdentifier are required.  | String        |
| `BankAPI.getPlayerBankAccounts(source, identifier, charIdentifier)`       | Returns all the Bank Accounts from a player. If source is available, having identifier and charIdentifier as null is acceptable but if there is no source available, identifier and charIdentifier are required.           | Table         |
| `BankAPI.getAccountMoney(iban, account)`                                  | Returns the account money (Cash / Gold) from an IBAN Account.                                                                                                                                                              | Integer       |
| `BankAPI.executeTransactionType(iban, transactionType, account, amount)`  | Executes transaction type ( DEPOSIT, WITHDRAW ).                                                                                                                                                                           | N/A           |
| `BankAPI.createBill(iban, reason, issuer, account, amount)`               | Creates (Generates) an IBAN bill.                                                                                                                                                                                          | N/A           |
| `BankAPI.createTransactionHistoryRecord(iban, reason, account, amount)`   | Creates (Generates) a transaction history record.                                                                                                                                                                          | N/A           |
| `BankAPI.depositGovernmentBanksSharedAmount(amount)`                      | Deposits a shared amount to all Government Accounts (That means, if amount is 50, it will shared (/) based on the available bank accounts, for example, if 5 are the government bank accounts, it will be shared / 5.      | N/A           |
| `BankAPI.getBankAccounts()`                                               | Returns all the available Bank Accounts.                                                                                                                                                                                   | Table         |


## Parameters Explanation

| Parameter                                                                          | Description                                                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `iban`                                                                             | Requires the IBAN account on a string form (text).                                                                                           | 
| `source`                                                                           | Requires an online player id source target                                                                                                   | 
| `identifier`                                                                       | Requires an online or offline player identifier (it is considered as citizenid for RSG)                                                      | 
| `charIdentifier`                                                                   | Requires an online or offline player character identifier (it is considered as cid for RSG)                                                  | 
| `account`                                                                          | The available account types are "CASH" and "GOLD"                                                                                            | 
| `transactionType`                                                                  | The available transaction types are "DEPOSIT" and "WITHDRAW"                                                                                 | 
| `reason`                                                                           | It requires a reason for a bill or a transaction history record, the reason length must be very short such as (DEPOSIT, TAX, POLICE, SALOON) | 
| `issuer`                                                                           | It requires an issuer for a bill, the issuer length must be very short such as (POLICE, SALOON, GOVERNMENT)                                  | 
