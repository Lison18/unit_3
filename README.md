# unit_3

## Criteria A: Planning

## Problem definition

Verlon Taisei Sakaguchi studies in UWC Isak Japan and wants to be updated of his school progress. He is asking for an aplication which records his new IB grades. Indeed, his objectif is to get a perfect score to get into his dream university in the United States. To achive this goal, he has to improve his grades by focusing more on the subjects that he is struggling with. Moreover, Verlon wants to know how much he has to study for each subjects
However, sometimes he is feeling very demotivated because of his school academic pressure and the lack of sleep. But he wants to always remember that every challenges that he is facing are at the end always going to make him stronger and that he has to move on by doing his best.

## Proposed Solution

### Design Statement

To solve Verlon motivation problem and to inform him of hi progress, 


## Success Criteria


1. The application has to provide a login system demanding the username, email and password in order to sign up
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
