# How to create a Weekend Planner

## 1. Create Agent

Create the agent and provide him some initial instructions. In this use case, we want the agent to plan our weekend based on the weather and the available events in the city. 

<img width="1435" height="674" alt="Screenshot 2025-07-16 at 20 51 02" src="https://github.com/user-attachments/assets/412ac7e2-6d28-4f31-b581-16a520b5a5ec" />

We want to connect to weather api and search the web for events in the city.

## 2. Add Tool

For the weather api, we use Open Meteo Weather Forecast API, which is taking coordinates as input and gets back a 7-day weather forecast. As you will see later in the output, the agent is able to infer the coordinates from the city name. 

<img width="1436" height="683" alt="Screenshot 2025-07-16 at 21 11 39" src="https://github.com/user-attachments/assets/8990d938-1f08-4012-8219-f050a46cbd3b" />

Next, we can easily select the web search tool.

<img width="1436" height="678" alt="Screenshot 2025-07-16 at 21 14 09" src="https://github.com/user-attachments/assets/0da391cc-3866-4dc1-816a-8f31ceda747d" />

## 3. Start Chat

Start a chat and tell the agent that you are spending the next weekend in a specific city.

## 4. Investigate the trace

<img width="1427" height="672" alt="Screenshot 2025-07-16 at 21 21 18" src="https://github.com/user-attachments/assets/8ccad1e0-4263-4bff-83b0-7baa68a222b6" />

Click on the agent node to see the thinking process!

<img width="1434" height="675" alt="Screenshot 2025-07-16 at 21 33 58" src="https://github.com/user-attachments/assets/6de9070f-a942-49aa-8e3a-f32d810ad23a" />



