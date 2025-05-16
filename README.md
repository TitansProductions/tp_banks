# Development API

`local BankAPI = exports.tp_banks:getAPI()`


| Export                                                                    | Description                                                                                                                                 | Example                                   | Returned Type |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|---------------|
| `BankAPI.getPlayerIBAN(source, identifier, charIdentifier)`               | Returns the player primary (main) IBAN Account                                                                                              |                                           | String        |
| `BankAPI.getPlayerJointAccountIBAN(source, identifier, charIdentifier)`   | Returns the player Joint IBAN Account (if available)                                                                                        |                                           | String        |
| `BankAPI.getAccountMoney(iban, account)`                                  | Returns the account money (Cash / Gold) from an IBAN Account.                                                                               |                                           | Integer       |
| `BankAPI.executeTransactionType(iban, transactionType, account, amount)`  | Executes transaction type ( DEPOSIT, WITHDRAW ).                                                                                            |                                           | N/A           |
| `BankAPI.createBill(iban, reason, issuer, account, cost)`                 | Creates (Generates) an IBAN bill.                                                                                                           |                                           | N/A           |
| `BankAPI.createTransactionHistoryRecord(iban, reason, account, amount)`   | Creates (Generates) a transaction history record.                                                                                           |                                           | N/A           |
| `BankAPI.getPlayerBankAccounts(targetSource, identifier, charIdentifier)` | Returns all the Bank Accounts from a player.                                                                                                |                                           | Table         |
| `BankAPI.depositGovernmentBanksSharedAmount(amount)`                      | Deposits a shared amount to all Government Accounts (That means, if amount is 50, it will shared (/) based on the available bank accounts.  |                                           | N/A           |
| `BankAPI.getBankAccounts()`                                               | Returns all the available Bank Accounts.                                                                                                    |                                           | Table         |
