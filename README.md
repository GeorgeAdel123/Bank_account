# Bank_account
an OOP simulation of creating a bank account
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

f1 = form(100,122783,44975895,"george")
print(f1.name)
f1.deposit(100)
print(f1.getbalance())
f1.withdraw(100)
print(f1.getbalance())
print(f1.getinfo())
f1.exit()
print(f1.getinfo())
