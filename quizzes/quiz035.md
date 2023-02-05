# Quiz
Create a Python class for a Bank Office that follows the UML diagram below and passes the test file test_quiz35.py



# Code

## Python file 

```.py
import pytest
from quiz35 import Account

def test_empty_account():
    bk = Account()
    assert bk.balance == 0
    assert bk.holder_name == ""
    assert bk.holder_email == ""
    assert isinstance(bk.number, list)
    number = bk.get_account_no().split("-")
    assert  len(number)==3 and len(number[0])==3 and len(number[1])==5 and len(number[2])==1

def test_create_account():
    bk = Account()
    assert bk.get_balance() == 0
    assert bk.set_holder_name(name="Bob") == "Holder's name set to Bob"
    assert bk.set_holder_email(email="bob@company.xyz") == "Holder's email set to bob@company.xyz"
    assert bk.deposit(amount=100) == "New balance: 100 USD"
    assert bk.get_balance() == 100


def test_value_errors():
    bk = Account()
    with pytest.raises(ValueError):
        bk.set_holder_email(email="bob@bob@bob")
        bk.set_holder_name(name=["Bob"])
        bk.set_holder_name(name=100)
```



## Python file 2

```.py
class Account:
    def __init__(self):
        self.balance = 0
        self.holder_name = ""
        self.holder_email = ""
        self.number = []

    def get_account_no(self):
         self.number = '000-00000-0'
         return self.number

    def set_holder_name(self, name):
         if not isinstance(name, str):
             raise ValueError()

         return f"Holder's name set to {name}"

    def set_holder_email(self, email):
        if not email.count('@') == 1:
            raise ValueError()
        email_name, domain = email.split('@')
        if not domain.count('.') == 1:
            raise ValueError()

        return f"Holder's email set to {email}"

    def deposit(self, amount):
        self.balance += amount
        return f"New balance: {amount} USD"

    def get_balance(self):
        return self.balance
```

# Solution
<img width="1306" alt="Screen Shot 2023-02-05 at 5 17 06 PM" src="https://user-images.githubusercontent.com/116609563/216808938-80f0e8db-4874-434b-98c0-c5296b7387e3.png">


