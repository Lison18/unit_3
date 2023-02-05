# Quiz
Write a program that creates the GUI below:

# Code

## Python file 

```.py
from kivymd.app import MDApp
class Quiz040(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
    def build(self):
        return
    def change_appearance(self):
        print(self.root.ids.main_screen.md_bg_color)
        if self.root.ids.main_screen.md_bg_color == [1.0, 1.0, 1.0, 1.0]:
            self.root.ids.main_screen.md_bg_color = "#000000"
            self.root.ids.changebutton.text_color = 1,1,1,1
            self.root.ids.name.text_color = 1, 1, 1, 1
            self.root.ids.changebutton.text = "Light Mode"
        else:
            self.root.ids.main_screen.md_bg_color = "#FFFFFF"
            self.root.ids.changebutton.text_color = 0,0,0,1
            self.root.ids.name.text_color = 0, 0, 0, 1
            self.root.ids.changebutton.text = "Dark Mode"

quiz40 = Quiz040()
quiz40.run()
```



## kv file

```.py
MDScreen:
    size:500,500
    MDBoxLayout:
        id: main_screen
        orientation:"vertical"
        md_bg_color: "#FFFFFF"
        MDLabel:
            id:name
            text: "Lison Hébert"
            halign: "center"
            font_style: "H2"
            theme_text_color: "Custom"
            text_color: 0, 0, 0, 1
            pos_hint: {"center_x": .5, "center_y": .5}
        MDRaisedButton:
            id: changebutton
            text: "Dark Mode"
            pos_hint: {"center_x": 0.06, "center_y": 0.1}
            on_release: app.change_appearance()
```

# Solution 

<img width="794" alt="Screen Shot 2023-02-05 at 6 05 08 PM" src="https://user-images.githubusercontent.com/116609563/216810584-46b425a7-3261-4497-a75b-dbb97f6ea688.png">

<img width="779" alt="Screen Shot 2023-02-05 at 6 05 41 PM" src="https://user-images.githubusercontent.com/116609563/216810585-b62ff72f-9f25-42a0-834f-83e2c7296757.png">
