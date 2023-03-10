# unit_3

## Criteria A: Planning

## Problem definition

Verlon Taisei Sakaguchi studies in UWC Isak Japan and wants to be updated of his school progress. He is asking for an aplication which records his new IB grades. Indeed, his objectif is to get a perfect score to get into his dream university in the United States. To achive this goal, he has to improve his grades by focusing more on the subjects that he is struggling with. Moreover, Verlon wants to know how much he has to study for each subjects
However, sometimes he is feeling very demotivated because of his school academic pressure and the lack of sleep. But he wants to always remember that every challenges that he is facing are at the end always going to make him stronger and that he has to move on by doing his best.

## Proposed Solution

### Design Statement

To address the client's requirements, a customized application can be developed utilizing the Python programming language and the Kivy MD library for user interface design. Python was selected due to the facility of use, extensive community support, and rich library collection, as well as its cross-platform compatibility. Kivy MD was chosen for its material design aesthetic, which enhances usability and intuitiveness for employees.

Regarding rental transaction data, SQL is an ideal choice for its robust and adaptable database management capabilities. Its ability to handle large amounts of data, safeguard it with security features, and accommodate concurrent users makes it well-suited for this application. SQL is truly impressive in its capabilities. By leveraging SQL to store grades information, client can input the grades and view averages.

### Justificaltion of the tools
Python is a multifunction and popular programming language with a lot of advantages:

- Easy to learn : Python is considered to be one of the easiest programming languages to learn, meaning that we can incorporate diverse functionalities .
- Large Community and Library Support: Python has a vast community of developers who create and share libraries, frameworks, and tools, making it easier to develop applications quickly and efficiently. 
- Versatile: Python can be used for various tasks such as, data analysis, machine learning, automation and  web development in this case.
- Readability: Python's clean syntax and readability make it easier to understand and maintain code.
- Dynamically Typed: Python is dynamically typed, which means you don't need to specify the data type of a variable when declaring it. This feature reduces the amount of code required to write, making it easier to understand and maintain.
- Open source: Python is free and open-source, meaning that anyone can download and use it for free, making it an accessible programming language for everyone.

The advantages of using KivyMD include:
- Material design look: KivyMD provides a material design look for the user interface, which is intuitive and easy to use for user.
- Crossed platform: KivyMD works on multiple platforms, including Windows, Linux, macOS, Android, and iOS, which makes it easy to develop cross-platform applications.
- Easy to Use: KivyMD is easy to use and implement, making it a great option for developers who want to create attractive and functional user interfaces quickly.
- Customizable: KivyMD provides a wide range of customization options, including colors, themes, and styles, allowing developers to create unique and personalized user interfaces.
- Large community and support: KivyMD has a large and active community of developers who create and share libraries and resources, making it easier to develop applications quickly and efficiently.

Some of the advantages of using SQL include:
- Efficient data storage: SQL provides an efficient way to retrieve data from a database, allowing users to quickly access the data they need without having to sift through large amounts of irrelevant data.
- Data security: SQL provides a high level of security for databases by allowing administrators to restrict access to specific users and control what data they can access.
- Scalability: SQL databases can handle large amounts of data and can be easily scaled up or down to accommodate changing needs.
- Standardization: SQL is a standardized language, meaning that it is widely recognized and used across different platforms and systems.
- Flexibility: SQL can be used to perform a wide range of functions, from simple data retrieval to complex data analysis.

## Success Criteria


1. The application has to provide a login system demanding the username and password in order to login and sign up
2. The application has to allow the user to input all his grades in IB
3. The application has to provide a function which calculates the average score of the client 
4. The application has log out
5. The application has to show a motivating quote each time the customer sign up 
6. The application has to provide a space for the client to write his positive note of the day

# Criteria B: Design

## System Diagram **SL**
<img width="1150" alt="Screen Shot 2023-03-09 at 8 44 16 AM" src="https://user-images.githubusercontent.com/116609563/223878626-0c7edc99-d039-4f9c-9d36-666409f2dd1d.png">


Figure 1- Represents the system diagram for the application. The development of the program is achieved through the use of Pycharm and the KivyMD library. Data are stored in the databas "project3.db", while the data come from the SQLite database engine. The arrows indicate the data transfer between the various components of the application.

## ER Diagram
<img width="1046" alt="Screen Shot 2023-03-09 at 10 25 49 AM" src="https://user-images.githubusercontent.com/116609563/223891389-1f2f7b77-2de1-4a1b-bfce-14d62ea9fa1f.png">

Figure 2- Represents the ER diagram for the database to store the data for the application. The database for the project has two tables, one for "user" and an other for "grade". The first one on the left side consists of being able to log in and sign up with the costumer ID: username, password and email. 

The second one on the right side is for the customer to be able to store his grades and subjects asigned to the ID

## UML Diagram
<img width="595" alt="Screen Shot 2023-03-10 at 9 46 05 AM" src="https://user-images.githubusercontent.com/116609563/224194991-98eb7bf7-3098-4bdb-b6b2-0c39f753c17a.png">

Figure 3 - The diagram illustrates the UML representation of the application's classes and methods employed during its development. Two primary parent classes, namely MDApp and MDScreen, are displayed in the diagram. The subclasses derive their attributes and methods from these parent classes.

Furthermore, the database_worker class present in the diagram provides methods to connect with SQLite3 database, search and retrieve information from it, store data into it, and terminate the connection with the database.

## Wireframe diagram

<img width="537" alt="Screen Shot 2023-03-10 at 11 22 28 AM" src="https://user-images.githubusercontent.com/116609563/224207300-42ee748c-de8e-45f3-9bd2-eb843c3e4d9c.png">

Figure 4- Represents all the screens that are in the application inculding the login screen, the signup screen, the menu, the today's quote screen (the quote is saved, and the grade table where you can get the average. It is showing how the screens are organized and what buttons are clicked on to make a certain screen appears thanks to the arrows. 

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
Check if the reflection of the day is saved	| functional: Integration testing |	The not should be saved and go back to the menu screen.
Check if the table is giving the average of all grades	| functional: Intergration testing|	Press average button in the grade table screen.	|	a white screen should pop up with the average written on it.



# Criteria C: Development

## List of techniques used

## Development


# Criteria D: Functionality

A 7 min video demonstrating the proposed solution with narration
