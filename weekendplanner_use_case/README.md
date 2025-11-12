# How to create a Weekend Planner

## 1. Create Agent

Create the agent and provide him some initial instructions. In this use case, we want the agent to plan our weekend based on the weather and the available events in the city. 

<img width="1435" height="674" alt="Screenshot 2025-07-16 at 20 51 02" src="https://github.com/user-attachments/assets/412ac7e2-6d28-4f31-b581-16a520b5a5ec" />

We want to connect to weather api and search the web for events in the city.

## 2. Add Tool

For the weather api, we use Open Meteo Weather Forecast API, which is taking coordinates as input and gets back a 7-day weather forecast. As you will see later in the output, the agent is able to infer the coordinates from the city name. 

Go to the shown json file in the folder of this repository and copy the content. 

<img width="1435" height="681" alt="Screenshot 2025-11-12 at 20 39 49" src="https://github.com/user-attachments/assets/b47e4f2e-c84e-4c77-8b93-9666644f6908" />

In the agent builder, select 'Add Tool' and choose Tool Type 'OpenAPI'. The destination name is 'Weather_API'. Paste the content from the json file.

<img width="1916" height="860" alt="Screenshot 2025-11-12 at 20 34 56" src="https://github.com/user-attachments/assets/1474ebe0-c7e3-4ddb-8145-3ebd6cc44dbc" />

Repeat the process for the Web Search Tool and copy the content from the Perplexity json file in this repository. 

<img width="1916" height="858" alt="Screenshot 2025-11-12 at 20 36 00" src="https://github.com/user-attachments/assets/6c42cb2b-1af7-421f-95bd-088af28ea8c8" />

## 3. Start Chat

Start a chat and tell the agent that you are spending the next weekend in a specific city.

## 4. Investigate the trace

<img width="1427" height="672" alt="Screenshot 2025-07-16 at 21 21 18" src="https://github.com/user-attachments/assets/8ccad1e0-4263-4bff-83b0-7baa68a222b6" />

Click on the agent node to see the thinking process!

<img width="1434" height="675" alt="Screenshot 2025-07-16 at 21 33 58" src="https://github.com/user-attachments/assets/6de9070f-a942-49aa-8e3a-f32d810ad23a" />



