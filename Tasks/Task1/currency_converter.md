# Task
Create a Currency Converter GUI that takes an integer representing an amount from your home country currency and converts it into USD and JPY rounded to 2 decimals.
⚠️ Remember to validate user inputs

# Solution
## Code

from kivymd.app import MDApp


class task1(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.amount = 0

    def build(self):
        return

    def converter_dollar(self):
        amount = self.root.ids.user_input.text
        if not amount.isdigit():
            self.root.ids.convertion.text = f"Please enter an amount in EUR"
        else:
            self.root.ids.conversion.text = f"{int(amount)} EUR is {round((int(amount) * 1.09), 2)} Dollar"

    def converter_yen(self):
        amount = self.root.ids.user_input.text

        if not amount.isdigit():
            self.root.ids.conversion.text = f"Please enter an an amount in EUR"
        else:
            self.root.ids.conversion.text = f"{int(amount)} EUR is {round((int(amount) * 141.29),2)} Yen"

task1().run()

## Proof of work

<img width="792" alt="Screen Shot 2023-01-31 at 12 08 42 PM" src="https://user-images.githubusercontent.com/116609563/215654024-d60004fb-e604-433b-b4e8-51c5a8cd4030.png">




