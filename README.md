<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>



<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>

## DESIGN STEPS
Define the Environment:
Understand the environment in which the vacuum cleaner operates. This includes identifying the size and layout of the environment, the locations of dirt, and any obstacles or boundaries.

### Define Percepts and Actions:
Determine what the vacuum cleaner can perceive and how it can act in the environment. Percepts may include information about the cleanliness of the current location, while actions may include moving to adjacent locations or cleaning the current location.

### Choose a Representation:
Decide how to represent the state of the environment and the actions of the vacuum cleaner. This could be done using data structures such as arrays, grids, or graphs.

### Select an Algorithm:
Choose an appropriate algorithm for the vacuum cleaner agent. Common algorithms include Simple Reflex Agents, Model-Based Reflex Agents, Goal-Based Agents, and Utility-Based Agents. The choice of algorithm depends on factors such as the complexity of the environment and the desired level of autonomy.

### Implement the Agent:
Implement the vacuum cleaner agent according to the chosen algorithm. This involves writing code to handle percepts, make decisions based on those percepts, and execute actions in the environment.

### Test and Evaluate:
Test the agent in various environments to ensure that it behaves as expected and effectively cleans the environment. Evaluate its performance based on criteria such as cleanliness achieved, efficiency of movement, and robustness to different environments.

### Refine and Optimize:
Iterate on the design and implementation of the agent to improve its performance and efficiency. This may involve refining the algorithm, optimizing code, or incorporating additional features such as learning mechanisms./p>

### Deployment and Maintenance:
Deploy the agent in real-world environments, such as robotic vacuum cleaners in homes or commercial settings. Monitor its performance and address any issues that arise through maintenance and updates.


## Program
```
NAME : Ashwin Kumar.S
REG NO : 212222240013

class VacuumCleanerAgent:
    def init(self):
        self.location = 0  # Current location of the vacuum cleaner
        self.environment = ['Clean', 'Dirty', 'Clean']  # Example environment, you can customize as needed

    def sense(self):
        """Sense the current location"""
        return self.environment[self.location]

    def act(self, percept):
        """Act based on the percept"""
        if percept == 'Dirty':
            self.clean()
        else:
            self.move()

    def clean(self):
        """Clean the current location"""
        print("Cleaning...")
        self.environment[self.location] = 'Clean'

    def move(self):
        """Move to the next location"""
        print("Moving...")
        self.location = (self.location + 1) % len(self.environment)


# Main function to test the agent
def main():
    agent = VacuumCleanerAgent()
    print("Initial environment:", agent.environment)
    for _ in range(len(agent.environment)):
        percept = agent.sense()
        print("Percept:", percept)
        agent.act(percept)
    print("Environment after cleaning:", agent.environment)


if __name__ == "__main__":
    main()

```
## Output:

![AI](https://github.com/Sriram8452/19AI405ExpNo1/assets/118708032/09bb1c60-ddd7-4eef-936a-2b15629ad401)


## Result:
Thus, an AI agent is developed.
