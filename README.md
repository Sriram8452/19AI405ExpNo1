<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Saravanan N</h3>
<h3>Register Number/Staff Id: TSML006</h3>

<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Vacuum Cleaning Agent:</h3>
<p></p>
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
    <td><strong>Vacuum Cleaning</strong></td>
    <td><strong>Cleaning Agent</strong></td>
     <td><strong>Rooms</strong></td>
    <td><strong>Vacuum Cleaners</strong></td>
    <td><strong>Dust Sensors</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>Define the Environment:</h3> 
<p>Understand the environment in which the vacuum cleaner operates. This includes identifying the size and layout of the environment, the locations of dirt, and any obstacles or boundaries.</p>

<h3>Define Percepts and Actions:</h3>
<p>Determine what the vacuum cleaner can perceive and how it can act in the environment. Percepts may include information about the cleanliness of the current location, while actions may include moving to adjacent locations or cleaning the current location.</p>

<h3>Choose a Representation:</h3>
<p>Decide how to represent the state of the environment and the actions of the vacuum cleaner. This could be done using data structures such as arrays, grids, or graphs.</p>
<h3>Select an Algorithm:</h3> 
<p>Choose an appropriate algorithm for the vacuum cleaner agent. Common algorithms include Simple Reflex Agents, Model-Based Reflex Agents, Goal-Based Agents, and Utility-Based Agents. The choice of algorithm depends on factors such as the complexity of the environment and the desired level of autonomy.</p>

<h3>Implement the Agent:</h3>
<p>Implement the vacuum cleaner agent according to the chosen algorithm. This involves writing code to handle percepts, make decisions based on those percepts, and execute actions in the environment.</p>

<h3>Test and Evaluate:</h3>
<p>Test the agent in various environments to ensure that it behaves as expected and effectively cleans the environment. Evaluate its performance based on criteria such as cleanliness achieved, efficiency of movement, and robustness to different environments.</p>

<h3>Refine and Optimize:</h3>
<p>Iterate on the design and implementation of the agent to improve its performance and efficiency. This may involve refining the algorithm, optimizing code, or incorporating additional features such as learning mechanisms./p>

<h3>Deployment and Maintenance:</h3>
<p>Deploy the agent in real-world environments, such as robotic vacuum cleaners in homes or commercial settings. Monitor its performance and address any issues that arise through maintenance and updates.</p>

<H4>PROGRAM</H4>
'''
class VacuumCleanerAgent:
    def __init__(self):
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
<H5>OUTPUT</H5>
