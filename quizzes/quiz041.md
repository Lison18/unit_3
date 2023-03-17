# Stattement
Write a program that creates the GUI below:

# Code

## Python file

from kivymd.app import MDApp

class Quiz041(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.values = [0] * 9
        self.player = "X"

    def button_press(self, button_id):
        current_player = self.player
        current_button = self.root.ids[f"button{button_id}"]
        if self.values[int(button_id)-1] == 0:
            current_button.text = current_player
            self.values[int(button_id)-1] = 1 if current_player == "X" else 2
            current_button.md_bg_color = "#B0D7FF" if current_player == "X" else "#EAE8FF"
            self.player = "O" if current_player == "X" else "X"

        winning_combinations = [(0, 1, 2), (3, 4, 5), (6, 7, 8),
                                (0, 3, 6), (1, 4, 7), (2, 5, 8),
                                (0, 4, 8), (2, 4, 6)]
        for indices in winning_combinations:
            if all(self.values[i] == self.values[indices[0]] and self.values[i] != 0 for i in indices):
                self.root.ids.label2.text = f"Winner is {current_player}"
                return
        self.root.ids.label2.text = f"Current Player: {self.player}"

    def reset(self):
        self.values = [0] * 9
        self.player = "X"
        for i in range(1, 10):
            current_button = self.root.ids[f"button{i}"]
            current_button.text = ""
            current_button.md_bg_color = "grey"
        self.root.ids.label2.text = f"Current Player: {self.player}"

tictactoe = Quiz041()
tictactoe.run()


## Kv file

MDScreen:
    id : screen
    size:500,500
    MDBoxLayout:
        id: main_box
        size_hint: .8, .8
        orientation: 'vertical'
        pos_hint: {'center_x': .5, 'center_y': .5}
        MDBoxLayout:
            id: box1
            size_hint: 1, .2
            orientation: 'vertical'
            MDLabel:
                id: label1
                text: 'Tic Tac Toe'
                halign: 'center'
                font_style: 'H3'
            MDLabel:
                id: label2
                text: "Player:" + app.player
                halign: 'center'
                font_style: 'H5'

        MDBoxLayout:
            id: box2
            size_hint: 1, .8
            orientation: 'vertical'
            pos_hint: {'center_x': .5, 'center_y': .5}
            MDBoxLayout:
                id: layerone
                size_hint:1,.33
                orientation:"horizontal"
                MDRaisedButton:
                    id: button1
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("1")
                MDRaisedButton:
                    id: button2
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("2")
                MDRaisedButton:
                    id: button3
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("3")
            MDBoxLayout:
                id: layertwo
                size_hint:1,.33
                orientation:"horizontal"
                MDRaisedButton:
                    id: button4
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("4")
                MDRaisedButton:
                    id: button5
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("5")
                MDRaisedButton:
                    id: button6
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("6")

            MDBoxLayout:
                id: layerthree
                size_hint:1,.33
                orientation:"horizontal"
                MDRaisedButton:
                    id: button7
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("7")
                MDRaisedButton:
                    id: button8
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("8")
                MDRaisedButton:
                    id: button9
                    text: ""
                    size_hint: .33, 1
                    md_bg_color: "blue"
                    on_release: app.button_press("9")

        MDBoxLayout:
            id: resetbox
            size_hint: 1, .2
            orientation: 'vertical'
            MDRaisedButton:
                id: resetbutton
                text: "Reset"
                size_hint: .5, .75
                pos_hint: {'center_x': .5, 'center_y': .5}
                on_release: app.reset()



## Proof of work

<img width="1440" alt="Screen Shot 2023-03-17 at 12 09 20 PM" src="https://user-images.githubusercontent.com/116609563/225802879-ed292301-091f-483a-ba80-3f8808b43879.png">

https://user-images.githubusercontent.com/116609563/225803628-42f0895f-aa08-4417-8bc3-2d8e09bb7ea2.mov




