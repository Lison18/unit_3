# Quiz 42
Write a program that creates the GUI described by the UML diagram for classes below:

# Python file
```.py
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen


class MysteryA(MDScreen):
    def messageA(self):
        print("Printing from MysteryA")
        self.ids.label1.text = "This is mystery A. you pressed a button"

class MysteryB(MDScreen):
    def messageB(self):
        print("Printing from MysteryB")

class Quiz042(MDApp):
    def build(self):
        return
        
quiz42 = Quiz042()
quiz42.run()
```
# Kv file
```.py
ScreenManager:
    id:screenManager
    MysteryA:
        name: "MysteryA"
    MysteryB:
        name: "MysteryB"

<MysteryA>:
    name: "MysteryA"
    MDBoxLayout:
        orientation: "vertical"
        MDLabel:
            id: label1
            text: "Welcome"
            halign: "center"
        MDRaisedButton:
            text: "Click Me"
            on_press: app.root.current = "MysteryB"
            on_press: root.messageA()

<MysteryB>:
    name: "MysteryB"
    MDBoxLayout:
        orientation: "vertical"
        MDLabel:
            id: label2
            text: "This is mystery B. you pressed a button"
            halign: "center"
        MDRaisedButton:
            text: "Click Me"
            on_press: app.root.current = "MysteryA"
  
  ```
 
  
# Proof of work



https://user-images.githubusercontent.com/116609563/226111553-30118b47-30a0-4dd4-8feb-d2ea02bc2ec8.mov





