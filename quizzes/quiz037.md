# Quiz
An Accounting firm needs a software package to calculate compound interest. Draw the UML diagram.

# Code

## Python file 
```.py
class CompountInterest:
    def __init__(self, principal, rate, time) -> None:
        self.principal = principal
        self.rate = rate
        self.time = time

    def compound_interest_calculator(self):
        return int(self.principal) * (1+int(self.rate)) ** int(self.time)

class AccountingProgram:
    def __init__(self):
        self.data = CompountInterest(principal=0, rate=0, time=0)

    def set_principal_test(self, principal):
        self.data.principal = principal

    def set_rate(self, rate):
        self.data.rate = rate

    def set_time(self, time):
        self.data.time = time

    def calculate_interest(self):
        return f"The compound interest for Principal:{self.data.principal}, Rate:{self.data.rate}, Time:{self.data.time} is {(self.data.compound_interest_calculator())}"


interest_john_doe = AccountingProgram()
interest_john_doe.set_principal_test(2)
interest_john_doe.set_rate(2)
interest_john_doe.set_time(2)
print(interest_john_doe.calculate_interest())
```



## ULM Diagram


# Solution 

<img width="700" alt="Screen Shot 2023-02-05 at 5 37 37 PM" src="https://user-images.githubusercontent.com/116609563/216809514-f6a01db5-8fee-4167-aef2-472b01c6bd88.png">



