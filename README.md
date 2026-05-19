# Transaction Processing System

## Project Description

This project is a C-based bank account transaction processing system. It uses a random-access binary file, `credit.dat`, to store account records and allows the user to create, update, delete, search, list, and analyze account information.

The project is based on file handling concepts in C, especially binary files, structures, random access using `fseek`, and record-based data storage.

## Account Structure

Each account record stores:

- Account number
- Last name
- First name
- Account balance

```c
struct clientData
{
    unsigned int acctNum;
    char lastName[15];
    char firstName[10];
    double balance;
};
```

## Features

The program includes the following features:

1. Generate a formatted text file called `accounts.txt`
2. Update an account balance
3. Add a new account
4. Delete an account
5. List all active accounts
6. Search account by first name or last name
7. Count total active accounts
8. Sort accounts by balance
9. Initialize or regenerate the account database
10. Display the account with the highest balance
11. Generate a low balance report
12. Prevent negative opening balance
13. Confirm before deleting an account
14. Maintain transaction history in `transactions.txt`

## Files Used

| File | Purpose |
|---|---|
| `trans.c` | Main C source code |
| `credit.dat` | Binary file used to store account records |
| `accounts.txt` | Generated text report of account records |
| `transactions.txt` | Transaction history log |
| `README.md` | Project documentation |

## How to Run in VS Code

Open this folder in VS Code:

```text
C:\Users\KiTE\Desktop\711725UIT141_JUMAANA
```

Open the terminal:

```text
Terminal -> New Terminal
```

Compile the program:

```powershell
gcc -Wall -Wextra -Wconversion -std=c11 trans.c -o trans.exe
```

Run the program:

```powershell
.\trans.exe
```

## Menu Options

```text
1  - Create accounts.txt file
2  - Update an account
3  - Add a new account
4  - Delete an account
5  - List all accounts
6  - Search account by name
7  - Count active accounts
8  - Sort accounts by balance
9  - Initialize account database
10 - Show highest balance account
11 - Low balance report
14 - Exit program
```

## Sample Testing

### List Accounts

```text
Enter your choice: 5
```

### Add Account

```text
Enter your choice: 3
Enter new account number: 2
Enter lastname, firstname, balance:
Kumar Ravi 5000
```

### Search by Name

```text
Enter your choice: 6
Enter first or last name to search: Ravi
```

### Count Accounts

```text
Enter your choice: 7
```

### Low Balance Report

```text
Enter your choice: 11
Enter low balance limit: 1000
```

### Exit

```text
Enter your choice: 14
```

## Important Note

Option `9` initializes `credit.dat` with 100 blank records. This will erase existing account data, so it should be used only when a fresh database is required.

## Error Handling Added

The program handles:

- Invalid account numbers
- Invalid menu input
- Negative opening balance
- Failed file reads and writes
- Delete confirmation
- Corrupted or invalid account records

## Conclusion

This project demonstrates the use of C structures, binary files, random-access file handling, input validation, and transaction reporting. The added features improve usability, reliability, and project presentation quality.
