# How to create HR Agent for overdue trainings

## 1. Create a new agent

Create a new agent and give him some initial instructions. Here, we want the agent to interact with some mock data for employee trainings and remind them with a mail if the training is overdue.


<img width="1432" height="663" alt="Screenshot 2025-07-16 at 19 28 04" src="https://github.com/user-attachments/assets/ccfef9f5-3fc1-4dc9-9085-c7f43f2d6a86" />


To get started quickly, use the following prompt: 

You are a HR Manager Assistant making sure the manager and his team are in compliance with the mandatory security and informational trainings required each year. Given a list of training deadlines, you take action and remind the team members in a nice but decisive way. The ultimate goal would be that all team members complete the trainings before the deadline.

In addition, you can work on some other settings like data masking (not needed) or LLM selection.

## 2. Add Tools

Click "Add Tool" and add the following 3 tools to interact with the systems.


<img width="1429" height="675" alt="Screenshot 2025-07-16 at 19 30 15" src="https://github.com/user-attachments/assets/a2bdba0b-d59a-4bb5-a53c-21b1adb4b17c" />



For each tool, you need to define an openapi specification, that is calling different endpoints of our mock system. This is happening via the destination "AGENT_MOCK_TOOLS" that we already have setup in our BTP subaccount. These are the endpoints for our system: 

### GET /get_employees

Param: manager_email (required)

Returns: List of employees (name, email, position) managed by the given email.

### GET /get_trainings

Param: employee_email (required)

Returns: List of trainings with name and due date for the given employee.

### POST /send_mail 

Body: recipient, subject, body (all required)

Returns: Confirmation string if email was sent successfully.


The JSON files for the openapi specification are in this folder and can be added to the tool definition as seen below.


<img width="1434" height="677" alt="Screenshot 2025-07-16 at 20 36 54" src="https://github.com/user-attachments/assets/a646fd4b-72b2-4ded-979d-691bb70fad29" />



## 3. Start a Chat

You can first try with this message to start the conversation: 

Please remind all of my team members about their assigned trainings, the upper management is eager to have our unit complete them ahead of time. 1 am the Example Manager 1 with the email manager1@example.com. Today is the 28th of Febuary 2025. Please contact all employees that have trainings due with reference to the request of the upper management. Report back to me who you contacted and by when I should contact them personally in case of non compliance.


## 4. Investigate the trace

<img width="1437" height="682" alt="Screenshot 2025-07-16 at 21 23 31" src="https://github.com/user-attachments/assets/e8f95363-d5b6-457b-8a06-b7b6aca069dc" />

Click on the agent node to see the thinking process!

<img width="1431" height="676" alt="Screenshot 2025-07-16 at 21 26 00" src="https://github.com/user-attachments/assets/651a8d1f-8e7f-4b67-829b-e927e0845724" />

