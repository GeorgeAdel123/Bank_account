# Simple Bank Account (Python)
 
A small Python class that models a bank account. It demonstrates **encapsulation** with private attributes, plus basic deposit, withdraw, and info methods.
 
## Features
 
- Create an account with a starting balance, account number, routing number, and owner name
- Deposit and withdraw money
- Check the current balance
- View account info
- Sensitive data (balance, account number, routing number) is stored in private attributes (`__name` mangling) so it can't be changed accidentally from outside the class
## Requirements
 
- Python 3.6+ (uses f-strings)
- No external libraries (only the built-in `os` module)
## Usage
 
1. Save the code below in a file named `bank_account.py`
2. Run it:
```bash
python bank_account.py
```
 
## Code
 
```python
import os
 
class form:
    def __init__(self, money, account_num, routing_num, name):
        self.__money = money
        self.__acc_num = account_num
        self.__rout_num = routing_num
        self.name = name
 
    def deposit(self, money):
        self.__money += money
 
    def withdraw(self, money):
        self.__money -= money
 
    def getbalance(self):
        return self.__money
 
    def getinfo(self):
        return f"your name is {self.name} your accnum {self.__acc_num} your routing num {self.__rout_num}"
 
    def exit(self):
        return os._exit(0)
 
f1 = form(100, 122783, 44975895, "george")
print(f1.name)
f1.deposit(100)
print(f1.getbalance())
f1.withdraw(100)
print(f1.getbalance())
print(f1.getinfo())
f1.exit()
print(f1.getinfo())   # never runs, see note below
```
 
## Example Output
 
```
george
200
100
your name is george your accnum 122783 your routing num 44975895
```
 
## Methods
 
| Method | Description |
|--------|-------------|
| `deposit(money)` | Adds `money` to the balance |
| `withdraw(money)` | Subtracts `money` from the balance |
| `getbalance()` | Returns the current balance |
| `getinfo()` | Returns a string with the name, account number, and routing number |
| `exit()` | Immediately terminates the program using `os._exit(0)` |
 
## Notes
 
- `exit()` calls `os._exit(0)`, which stops the program instantly without cleanup. That's why the final `print(f1.getinfo())` never runs.
- `withdraw()` does not currently check for insufficient funds, so the balance can go negative.
- The account and routing numbers in the example are fake sample values.
## Possible Improvements
 
- Block withdrawals larger than the balance
- Reject negative or zero deposit/withdraw amounts
- Rename the class from `form` to `BankAccount`
- Replace `os._exit(0)` with `sys.exit()`
- Add a transaction history
## Author
 
George
 
