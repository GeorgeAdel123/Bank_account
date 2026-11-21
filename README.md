Simple Bank Account (Python)

A small Python class that models a bank account. It demonstrates encapsulation with private attributes, plus basic deposit, withdraw, and info methods.

Features
Create an account with a starting balance, account number, routing number, and owner name
Deposit and withdraw money
Check the current balance
View account info
Sensitive data (balance, account number, routing number) is stored in private attributes (__name mangling) so it can't be changed accidentally from outside the class
Requirements
Python 3.6+ (uses f-strings)
No external libraries (only the built-in os module)
Usage
Save the code below in a file named bank_account.p

Methods
Method	Description
deposit(money)	Adds money to the balance
withdraw(money)	Subtracts money from the balance
getbalance()	Returns the current balance
getinfo()	Returns a string with the name, account number, and routing number
exit()	Immediately terminates the program using os._exit(0)
Notes
exit() calls os._exit(0), which stops the program instantly without cleanup. That's why the final print(f1.getinfo()) never runs.
withdraw() does not currently check for insufficient funds, so the balance can go negative.
The account and routing numbers in the example are fake sample values.
Possible Improvements
Block withdrawals larger than the balance
Reject negative or zero deposit/withdraw amounts
Rename the class from form to BankAccount
Replace os._exit(0) with sys.exit()
Add a transaction history
Author

George
