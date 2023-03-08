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


1. The application has to provide a login system demanding the username, email and password in order to login and sign up
2. The application has to allow the user to input and delate all his grades in IB
3. The application has to provide a system which calculate the average score of the client 
4. The application has to provide an alarm message when the grade is very low (below 4) and a positive one when the grade is high (higher than 5)
5. The application has to show a motivating quote each time the customer sign up 
6. The application has to provide a space for the client to write his positive note of the day

# Criteria B: Design

## System Diagram **SL**
![](sysdim_sl.png)

**Fig.1** shows the system diagram for the proposed solution (**SL**). The indoor variables will be measured using an Arduino microprocessor and the sensor DHT11 conencted to the local computer (Laptop) located inside a room. The outdoor variables will be requested to the remote server using a GET request to the API of the server at ```192.168.6.147/readings```. The local values are stored in a CSV database locally.

![](sysdim_hl.png)

**Fig.2** shows the system diagram for the proposed solution (**HL**). The indoor variables will be measured using a Raspberry PI and four DHT11 sensors located inside a room. Four sensors are used to determine more precisely the physical values and include measurement uncertainty. The outdoor variables will be requested to the remote server using a GET request to the API of the server at ```192.168.6.147/readings```. The local values are stored in a CSV database locally and POST to the server using the API and TOKEN authentication. A laptop computer is used for remotely controlling the local Rasberry Pi using a Dekptop sharing application (VNC Viewer). (Optional) Data from the local raspberry is downloaded to the laptop for analysis and processing.


## Record of Tasks
| Task No | Planned Action                                                | Planned Outcome                                                                                                 | Time estimate | Target completion date | Criterion |
|---------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|---------------|------------------------|-----------|
| 1       | Write the Problem context                        | 10min         | Nov 22                 | A         |

## Test Plan

# Criteria C: Development

## List of techniques used

## Development


# Criteria D: Functionality

A 7 min video demonstrating the proposed solution with narration
