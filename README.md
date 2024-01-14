# unit_3
<img width="1440" alt="Screen Shot 2023-03-10 at 9 20 20 PM" src="https://user-images.githubusercontent.com/116609563/224541741-f7299adf-cc70-44d1-9db9-73550486ece6.png">

## Criteria A: Planning

## Problem definition

My client is an IB student and would like to be kept informed of his recent academic progress. With a severe physical disability, he takes his courses at home on his computer. His goal is to get a perfect score to get into his dream university, Georgetown University, which requires a score of 43 out of 45 points in the USA. To do this, he needs to know exactly what his grade point average will be to gain admission to this prestigious university. But every time a new grade is added to his ManageBac account, he has to manually calculate his score using a calculator, which takes up a lot of his time and doesn't allow him to see the subjects he needs to improve. 
What's more, he sometimes feels demotivated by the stress of classes and lack of sleep, knowing that he has no one to talk to to support him in his efforts.

## Rationale Proposed Solution

To meet the client's requirements, I propose the development of a tailored application utilizing Python as a cost-free, platform-independent programming language. Employing a Graphical User Interface (GUI) may prove beneficial for the program's usability. To facilitate data storage for the client, the adoption of SQLite is suggested, given its extensive usage as a reliable database. This choice aligns well with the intended functionality of the application, which involves displaying, storing, deleting, and adding data pertaining to the client's grades. The use of KivyMD will enable the coding of a GUI featuring multiple pages. KivyMD's user-friendly nature ensures ease of development, offering visually appealing displays and providing the necessary options as per the client's requirements.

### Design Statement

I will design an application using python and KivyMD wich will use a SQLite database to store data for the user of the application. The application will allow my client to record his grades in different subjects and get his average IB score while staying motivated. It will take approximately 2 months to complete. The application will be evaluated according to the following criterias:

1. The application has to provide a login system demanding the username and password in order to login and sign up
2. The application has to allow the user to add an delate all his grades in IB
3. The application has to provide a function which calculates the average score of the client 
4. The application has to show a motivating quote each time the customer signs up 
5. The application has to provide a space for the client to write his positive note of the day


### Justificaltion of the tools

Python and KivyMD have a lot of advantages for the creation of the client's application:

- Reability: Python's clean syntax and readability make it easier to understand and maintain code.
- Open Source: Python is free, making it an accessible programming language the client.
- Material design look: KivyMD provides a material design look for the user interface, which is intuitive and easy to use for the client
- Crossed platform: KivyMD works on multiple platforms, including Windows, Linux, macOS, Android and iOS wich makes it easy to develop cross-platform applications.

Some of the advantages of using SQL include:

- Efficient data storage: SQL provides an efficient way to retrieve data from a database, allowing the client to quickly access the data of his grades without having to sift through large amounts of irrelevant data.
- Data security: SQL provides a high level of security for databases by allowing the client to restrict access to specific users and control what data they can access.
- Scalability: SQL databases can handle large amounts of data and can be easily scaled up or down to accommodate changing needs.
- Flexibility: SQL can be used to perform a wide range of functions, from simple data retrieval to complex data analysis.


# Criteria B: Design

## System Diagram **SL**
<img width="1150" alt="Screen Shot 2023-03-09 at 8 44 16 AM" src="https://user-images.githubusercontent.com/116609563/223878626-0c7edc99-d039-4f9c-9d36-666409f2dd1d.png">


Figure 1- Represents the system diagram for the application. The development of the program is achieved through the use of Pycharm and the KivyMD library. Data are stored in the databas "project3.db", while the data come from the SQLite database engine. The arrows indicate the data transfer between the various components of the application.

## ER Diagram
<img width="1046" alt="Screen Shot 2023-03-09 at 10 25 49 AM" src="https://user-images.githubusercontent.com/116609563/223891389-1f2f7b77-2de1-4a1b-bfce-14d62ea9fa1f.png">

Figure 2- Represents the ER diagram for the database to store the data for the application. The database for the project has two tables, one for "user" and an other for "grade". The first one on the left side consists of being able to log in and sign up with the costumer ID: username, password and email. 

The second one on the right side is for the customer to be able to store his grades and subjects asigned to the ID

### Example of data Entries

<img width="481" alt="Screen Shot 2024-01-14 at 8 53 18 AM" src="https://github.com/Lison18/unit_3/assets/116609563/7655e4ae-a1a0-4627-8434-833826e6a6e1">

Fig 3. Example of data entry in the users table


## UML Diagram
<img width="595" alt="Screen Shot 2023-03-10 at 9 46 05 AM" src="https://user-images.githubusercontent.com/116609563/224194991-98eb7bf7-3098-4bdb-b6b2-0c39f753c17a.png">

Figure 3 - The diagram illustrates the UML representation of the application's classes and methods employed during its development. Two primary parent classes, namely MDApp and MDScreen, are displayed in the diagram. The subclasses derive their attributes and methods from these parent classes.

Furthermore, the database_worker class present in the diagram provides methods to connect with SQLite3 database, search and retrieve information from it, store data into it, and terminate the connection with the database.

## Wireframe diagram

<img width="681" alt="Screen Shot 2023-03-29 at 9 48 20 PM" src="https://user-images.githubusercontent.com/116609563/228540349-597126c3-89a1-48a4-b05d-4b7de25d61e0.png">

Figure 4- Represents all the screens that are in the application inculding the login screen, the signup screen, the menu, the today's quote screen (the quote is saved, and the grade table where you can get the average. It is showing how the screens are organized and what buttons are clicked on to make a certain screen appears thanks to the arrows. 

## Flow diagrams

### Flow diagram for try_login method in class LoginScreen:



<img width="202" alt="Screen Shot 2023-03-10 at 5 18 39 PM" src="https://user-images.githubusercontent.com/116609563/224304535-30216efb-9cad-495c-aa03-06b3b64a8ede.png">

Figure 5- The LoginScreen class utilizes the try_login method to verify the user's login details. Upon receiving the user's email and password, the method retrieves the hashed password from the "users" table in the database through the use of the get_password_from_email() function from the database_handler_login_signup class. The try_login method plays a pivotal role in the LoginScreen class as it guarantees that only legitimate users are able to access the application's functionalities.

### Flow diagram for get_average method in class TableScreen:

<img width="353" alt="Screen Shot 2023-03-29 at 8 01 55 PM" src="https://user-images.githubusercontent.com/116609563/228514052-869f0127-c78b-4005-9a92-b6a240525afc.png">


Figure 5- This diagram represents the code which calculates the average grade of students stored in a SQLite database called "project3.db". It retrieves all grades from the "grades" table using an SQL query, and then calculates the average grade by adding up all grades and dividing by the total number of grades. The result is displayed in a dialog box using the MDDialog class from the KivyMD library and is also printed to the console. If no grades are found in the database, a message is printed to the console. 

### Flow diagram for try_register in SignupScreen:

<img width="303" alt="Screen Shot 2023-03-29 at 8 54 24 PM" src="https://user-images.githubusercontent.com/116609563/228528052-530282fd-cd06-4b0c-a10d-34c1d82890be.png">

Figure 6- This code creates a method called try_register which registers a new user into the application by retrieving input from the username, email, password, and confirm password fields. If the password and confirm password fields match, the user's data is added to the "users" table in the SQLite database. Otherwise, an error message is displayed on both password fields. A "Registration completed" message is printed to the console, and the current screen view is changed to the "LoginScreen". Finally, the database connection is closed.

## Record of Tasks
| task no | Planned action                                         | Planned outcome | Time estimate | Target completion | Criterion |
|---------|--------------------------------------------------------|-----------------|---------------|-------------------|-----------|
| 1       | Write the problem context                              | Feb 2           | 10min         | feb5              | A         |
| 2       | meeting with my client                                 | feb 5           | 20min         | feb 5             | A         |
| 3       | write the success criterions                           | feb10           | 10min         | feb10             | A         |
| 4       | draw the flow chart                                    | feb 12          | 30min         | feb12             | B         |
| 5       | create the python file                                 | feb 15          | 2min          | feb15             | C         |
| 5       | create the kv file                                     | feb 15          | 2min          | feb15             | C         |
| 6       | import Dr Ruben's login code to the python file        | feb 16          | 3min          | feb16             | c         |
| 7       | Creation of the kv file for the login system           | feb17           | 20min         | feb17             | c         |
| 8       | modification if the login code                         | feb20           | 20min         | feb25             | c         |
| 9       | creation of the class login                            | feb21           | 15min         | feb21             | c         |
| 10      | creation of the sign up login                          | feb21           | 20min         | feb21             | C         |
| 11      | kv code for the sign up screen                         | feb21           | 20min         | feb21             | c         |
| 12      | creation of the IntroScreen class                      | feb24           | 30min         | feb 21            | C         |
| 13      | kv code for the Introscreen                            | feb24           | 30min         | feb 21            | c         |
| 14      | creation of the  IntroScreen                           | feb25           | 40min         | feb 25            | C         |
| 15      | creation of the menu class                             | feb25           | 40min         | feb25             | C         |
| 16      | kv code for the Table screen                           | feb26           | 40min         | feb26             | C         |
| 17      | creation of the table screen                           | feb26           | 40min         | feb26             | C         |
| 18      | make the code prettier                                 | feb28           | 2h            | feb30             | D         |
| 19      | make the interface prettier                            | Mar 1           | 2h            | Mar9              | D         |
| 20      | draw the UML diagram                                   | mar3            | 40min         | mar3              | B         |
| 21      | draw the ER Diagram                                    | mar5            | 30min         | mar5              | B         |
| 22      | draw the wirefare diagram                              | mar7            | 30min         | mar7              | B         |
| 22      | draw the first flow diagram to login                   | mar8            | 20min         | mar8              | B         |
| 23      | comment the most important parts of the code on github | mar9            | 1h            | mar10             | B         |
| 24      | uploade the most importante piece of code on github    | mar 10          | 20min         | mar10             | C         |


## Test Plan
| Description | Type | Inputs | Outputs | 
| ----------- | ---- | ------ | ------- |
Test if signup page works	|	Functional: Integration testing	|	Press "Sign up", use "lis" for all text fields. Press "Submit".	|	Should bring to login screen
Test if login and logout pages work	|	Functional: Integration testing	|	Enter "lison" for email and password. Press "Login". Press logout button	|	Should bring the user to Menuscreen, should bring the user to login screen
Testing if adding and delete new grades works	|	Functional: Integration testing	|	Enter id, subject, grade. Press submit.	Then delete the row by pressing delete button|	Should see a nex row with the new grade and it should delete
Check if the reflection of the day is saved	| functional: Integration testing |	Write the note |  The note should be saved and go back to the menu screen.
Check if the table is giving the average of all grades	| functional: Intergration testing|	Press average button in the grade table screen.	|	a white screen should pop up with the average written on it.



# Criteria C: Development

## Existing tools
- Pycharm
- Python
- SGLite Database
- ChatGPT
- RGB colors

## Techniques used

- For loops
- Variables
- Database interaction
- Functions
- Methods
- Object Oriented Programming (OOP) -> Inheritance, Classes


## Computational Thinking

###Success criteria 1: The application has to provide a login system demanding the username and password in order to login and sign up

In order to make the customer account securized I implementate a login and sign up system.

#### Login System
```.py

    def try_login(self):
        print("User tried to login")
        # Get the input username and password and print it
        email = self.ids.email_in.text
        passwd = self.ids.passwd_in.text
        query = f"SELECT * from users WHERE email='{email}' and password='{passwd}'"
        db = database_handler("project3.db")
        result = db.search(query=query)
        print(result)
        db.close()
        if len(result) == 1:
            print("Login successful")
            self.parent.current = "MenuScreen"
        else:
            print("Login incorrect")
```
            
The "try_login" method checks if the entered email and password exist in the "users" table of the "project3.db" database. It creates an SQL query, executes it, and prints the result. If the result has a length of 1, the user is directed to the "MenuScreen". Otherwise, an error message is displayed.
     
#### Sign up system

```.py
    def try_register(self):
        uname = self.ids.uname.text
        email = self.ids.email.text
        passwd = self.ids.e_passwd.text
        passwd_check = self.ids.c_passwd.text
        if passwd != passwd_check:
            self.ids.e_passwd.error = True
            self.ids.c_passwd.error = True
        else:  # password match
            db = database_handler("project3.db")
            db.create_table_users()
            db.insert_user(email, passwd, uname)
            db.close()
            print("Registration completed")
            self.parent.current = "LoginScreen"
```            
            
This code defines a method "try_register" for user registration that receives input data from four different text fields: "uname", "email", "e_passwd", and "c_passwd". If the entered passwords do not match, an error is displayed in both password fields. Otherwise, the method creates a new object of the "database_handler" class using the "project3.db" database and creates a new table named "users" in the database if it doesn't exist already. The user's information is then inserted into the "users" table using the "insert_user" method, and the database connection is closed. The method prints the message "Registration completed" and sets the current screen to the "LoginScreen".

#### MDtextField 
```.kv

        MDTextField:
            id: email_in
            hint_text: "Enter your username or email"
            icon_left: "email"
```
This code belonging to the kv file of the project is an exemple of how to create a text boxe on a screen where the user can input his username and email.


### Success criteria 2:  The application has to allow the user to add and delate all his grades in IB

#### adding grades
```.PY
    def update(self):
        db = database_handler("project3.db")
        query = "select user_id, subject, grade from grades"
        data = db.search(query)
        db.close()
        print(data)
        self.data_table.update_row_data(None, data)
 ```       
        
This code is a method called "update" that updates data displayed on the screen. Then, it creates a new object of the "database_handler" class and executes an SQL query to select user_id, subject, and grade columns from the "grades" table of the "project3.db" database. It stores the result in "data" and prints it. Then, it updates the data displayed on the screen using the "update_row_data" method of the "data_table" object with the new data.

### Delete grades
```.py
    def delete_selected_row(self):
        checked_rows = self.data_table.get_row_checks()
        print(checked_rows)
        db = database_worker("project3.db")
        for row in checked_rows:
            id = row[0]
            query = f"delete from grades where id = {id}"
            db.run_save(query)
        db.close()  # move this statement inside the for loop
        self.update()
   ```     
This method deletes selected rows from a table displayed on the screen. It gets the list of checked rows, creates a new object of the "database_worker" class, iterates over the checked rows, retrieves the "id" of each row, constructs an SQL query to delete the corresponding row from the "grades" table, and executes the query. Finally, it updates the table displayed on the screen by calling the "update" method.

#### MDRaiseButton
```.kv
        MDRaisedButton:
            id: delete
            text: "delete grade"
            on_press:
                root.delete_selected_row()
```
This code from the kv file of the project is an exemple of how to create the button which allow the user to delate his grades by row.

### Success criteria 3:  The application has to provide a function which calculates the average score of the client 
```.py
    def get_average(self):
        db = database_handler("project3.db")
        query_grades = "SELECT grade from grades"
        result = db.search(query=query_grades)
        grades = [row[0] for row in result]  # Extract grades from the query result
        if grades:
            grades = [int(grade) for grade in grades]  # Convert grades to floats
            average_grade = sum(grades) / len(grades)
            dialog = MDDialog(title="Grade average",
                              text=f"Average grade: {average_grade:.2f}")
            dialog.open()
            print(f"Average grade: {average_grade:.2f}")
        else:
            print("No grades found in the database")
        db.close()
 ```      
This code defines a method called "get_average" that calculates the average of all grades stored in the "grades" table of the "project3.db" database.
Creates furthermore a new object of the "database_handler" class and executes an SQL query to retrieve all grades from the "grades" table. The grades are extracted from the query result and stored in the "grades" variable.
If there are any grades in the "grades" variable, the method converts the grades to integers, calculates the average grade, and displays the result in a dialog box using the "MDDialog" class. The average grade is also printed to the console.
If there are no grades in the "grades" variable, the method prints a message to the console indicating that no grades were found in the database.
Finally, the method closes the database connection.

### Success criteria 4:  The application has log out
```.py
    def try_log_out(self):
        self.parent.current = "MenuScreen"
 ```       
This simple code is a method called "try_log_out" that is used to log out the user by changing the current screen to the "MenuScreen".
The method simply sets the value of the "current" attribute of the "parent" object (which refers to the parent widget of the current screen) to "MenuScreen". This causes the screen to be changed to the "MenuScreen".

#### MDCard

```.kv
    size: 500, 500
    FitImage:
        source: "image2.jpeg"

    MDCard:
        size_hint: .5, .9
        elevation: 2
        orientation: "vertical"
        pos_hint: {"center_x": .5, "center_y": .5}
        padding: dp(50)
        md_bg_color: "#DCDCDC"
```

This code from the kv file of the project is creating the log out screen for the client called "MDCard". It is basically the primary screen for every pages on wihich we can personify with different colors, size, writing style, and even add image: "image2.jpeg" by downloading it.

### Success criteria 5: The application has to show a motivating quote each time the customer signs up 
```.py
    def on_pre_enter(self, *args):

        quotes = [
            "Believe you can and you're halfway there. -Theodore Roosevelt",
            "You are never too old to set another goal or to dream a new dream. -C.S. Lewis",
            "Positive anything is better than negative nothing. -Elbert Hubbard",
            "In the middle of every difficulty lies opportunity. -Albert Einstein",
            "The best way to predict your future is to create it. -Abraham Lincoln",
            "Be the change that you wish to see in the world. -Mahatma Gandhi",
            "Success is not final, failure is not fatal: it is the courage to continue that counts. -Winston Churchill"

        ]

        rand_num = random.randint(0, 6)
        self.ids.quote.text = quotes[rand_num]
```        

This code defines a method called "on_pre_enter" that is called before the screen associated with this class is entered.
The method first creates a list of quotes and stores it in the "quotes" variable.
Then, a random number is generated using the "randint" method of the "random" module, and the quote corresponding to that random number is displayed on the screen by setting the text of the "quote" widget to the selected quote.


### Success criteria 6: The application has to provide a space for the client to write his positive note of the day
```.py
    def Today_notes(self):
        if not self.ids.notes.text():
            print("Write your reflection!")
        else:
            # do something else here
            self.parent.current = "MenuScreen"
 ```                       
This code defines a method called "Today_notes" that is used to check if the user has written a reflection or note for the day.
First, the code checks if the "notes" field is empty or not by calling the "text" method on the "notes" widget using the "ids" attribute. If the "notes" field is empty, the method prints the message "Write your reflection!" to the console.
If the "notes" field is not empty, the method sets the current screen to "MenuScreen" by calling the "current" attribute on the "parent" widget using the "ids" attribute.
Overall, this code is used to ensure that the user has written a reflection or note for the day before proceeding to the next screen.

# Criteria D: Functionality

##A 7 min video demonstrating the proposed solution with narration

https://www.youtube.com/watch?v=UXBvzNz27bs

## Complete code

- Python file: https://github.com/Lison18/unit_3/blob/main/Python%20file
- Kv file: https://github.com/Lison18/unit_3/blob/main/Kv_file

## Citations

https://www.sqlite.org/aff_short.html
https://emeritus.org/blog/coding-what-is-pycharm/#:~:text=What%20is%20PyCharm%20Used%20For,by%20programmers%20using%20various%20APIs.
https://stackoverflow.com/questions/73157765/kivymd-using-main-for-events-and-kv-file-for-layout
https://stackoverflow.com/questions/67982460/how-do-i-get-the-average-age-or-grade-of-my-stored-list
https://www.google.fr/search?q=fond+d%27%C3%A9cran+arbre+rouge+et+noir&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjkifK0q9H9AhW1mVYBHWh7CXQQ_AUoAXoECAEQAw&biw=1440&bih=789&dpr=2#imgrc=O6cdarYoBA-V6M&imgdii=Tfs8yAK9JlVU2M

