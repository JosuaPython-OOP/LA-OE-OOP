```python
class BankAccount:
    def init(self, account_num, balance):
        self.account_num = account_num
        self.balance = balance

    def deposit(self,amount):
        if amount > 0:
            self.balance += amount
        else:
            print("Not enough amount")

    def withdraw(self,amount):
        if amount > 0 and amount <= self.balance:
            self.balance -= amount
        else:
            print("The current balance is insufficient or the withdrawal amount is less than 0")

    def display_account_info(self):
        print(f" \nBank Account Number:{self.account_num} \nCurrent Balance: {self.balance}")

    def get_account_number(self):
        return self.account_num

    def get_balance(self):
        self.display_balance()

    def set_balance(self,balance):
        if balance >= 0:
            self.balance = balance
        else:
            print("Not enough balance")

    def display_balance(self):
        print(f"Current Balance:{self.balance}")

acc1 = BankAccount("031234",0.00)
acc1.display_account_info()
acc1.deposit(float(input("Deposit amount: ")))
print("\nNew Bank Account info")
acc1.display_account_info()
acc1.withdraw(float(input("Withdraw amount: ")))
print("\nNew Bank Account info")
acc1.display_account_info()
```python
