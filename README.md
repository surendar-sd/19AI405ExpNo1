ExpNo 1 :Developing AI Agent with PEAS Description

Name: SURENDAR S.D

Register Number:21222411052

AIM:

To find the PEAS description for the given AI problem and develop an AI agent.


Theory

Medicine prescribing agent:
Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.

PEAS DESCRIPTION:

Agent Type	Performance	Environment	Actuators	Sensors
Medicine prescribing agent	Treating unhealthy, agent movement	Rooms, Patient	Medicine, Treatment	Location, Temperature of patient
DESIGN STEPS
STEP 1:Identifying the input:
Temperature from patients, Location.

STEP 2:Identifying the output:
Prescribe medicine if the patient in a random has a fever.

STEP 3:Developing the PEAS description:
PEAS description is developed by the performance, environment, actuators, and sensors in an agent.

STEP 4:Implementing the AI agent:
Treat unhealthy patients in each room. And check for the unhealthy patients in random room

STEP 5:
Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented

Program
```
class VacuumCleanerAgent:
    def __init__(self):
        self.location = "A"  # Initial location
        self.dirt_status = {"A": False, "B": False}

    def move_left(self):
        if self.location == "B":
            self.location = "A"

    def move_right(self):
        if self.location == "A":
            self.location = "B"

    def suck_dirt(self):
        if self.dirt_status[self.location]:
            self.dirt_status[self.location] = False
            print(f"Sucked dirt in location {self.location}")
        else:
            print(f"No dirt at location {self.location}")

    def do_nothing(self):
        pass

    def perform_action(self, action):
        if action == "left":
            self.move_left()
        elif action == "right":
            self.move_right()
        elif action == "suck":
            self.suck_dirt()
        elif action == "nothing":
            self.do_nothing()
        else:
            print("Invalid action")

    def print_status(self):
        print(f"Location: {self.location}, Dirt Status: {self.dirt_status}")


# Create agent object
agent = VacuumCleanerAgent()

# Perform actions
agent.perform_action("left")
agent.print_status()

agent.perform_action("suck")
agent.print_status()

agent.perform_action("nothing")
agent.print_status()
```
Output

<img width="738" height="153" alt="image" src="https://github.com/user-attachments/assets/f7e5f93e-adaf-4845-90b5-72875b8c5d93" />


Result

The above algorithem run successful and the cleaning process was running successfully
