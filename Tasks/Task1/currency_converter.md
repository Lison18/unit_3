# Task
Create a Currency Converter GUI that takes an integer representing an amount from your home country currency and converts it into USD and JPY rounded to 2 decimals.
⚠️ Remember to validate user inputs

# Solution
## Code
### Python file
```.py
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
```
### Kv file 

```.kv
Screen:
    size: 500,500

    MDLabel:
        text: "Currency Converter"
        font_style: "H5"
        pos_hint: {'center_y': .75}
        halign: "center"

    MDTextField:
        id: user_input
        hint_text: "Enter an amount in EUR"
        pos_hint: {'center_x': .5, 'center_y': .5}
        halign: "center"
        size_hint_x: .75
        mode: 'rectangle'
        text_color_focus: "black"
        line_color_normal: "#000000"
        hint_text_color_normal: "#000000"


    MDLabel:
        text: "Click to convert"
        pos_hint: {"center_x": .625, 'center_y':.4}
        font_style: "H6"

    MDChip:
        text: "$"
        pos_hint: {"center_x": .725, "center_y": .4}
        md_bg_color: "000000"
        text_color: "#FFFFFF"
        mode: "rectangle"
        on_press: app.converter_dollar()

    MDChip:
        text: "¥"
        pos_hint: {"center_x": .800, "center_y": .4}
        md_bg_color: "#D62828"
        text_color: "#FFFFFF"
        mode: "rectangle"
        on_press: app.converter_yen()

    MDLabel:
        id: conversion
        text: ""
        font_style: "H5"
        pos_hint: {'center_y': .2}
        halign: "center"
```


## Proof of work
### Screenshot

<img width="792" alt="Screen Shot 2023-01-31 at 12 08 42 PM" src="https://user-images.githubusercontent.com/116609563/215654024-d60004fb-e604-433b-b4e8-51c5a8cd4030.png">

### Video




https://user-images.githubusercontent.com/116609563/216876750-a8e3c9e2-f32b-4ea3-87d4-053823d9b21a.mov







