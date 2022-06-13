##DESCRIPTION

An RL algorithm is implemented in Python for the agent's global path planning task. It is said that such a system has feedback. Agents affect the environment, and environments affect agents.

At each step the agent:
Executes action.
Receives observation (new state).
Receives reward.

The environment:
Receives action.
Emits observation (new state).
Emits reward.

Goal is to learn how to take actions in order to maximize the reward. The objective function is as following:

Q_[s_, a_] = Q[s, a] + λ * (r + γ * max(Q_[s_, a_]) – Q[s, a]),

where,
Q_[s_, a_] - value of the objective function on the next step,
Q[s, a] - value of the objective function on the current position,
max(Q_[s_, a_]) – Q[s, a]) - choosing maximum value from the possible next steps,
s – current position of the agent,
a – current action,
λ – learning rate,
r – reward that is got in the current position,
γ – gamma (reward decay, discount factor),
s_ - next chosen position according to the next chosen action,
a_ - next chosen action.

The main component of the RL method is the system state weight table Q-table. Matrix Q is the set of all possible states of the system and is the weight of the system's reaction to various actions. While trying to cross a given environment, mobile robots learn to avoid obstacles and find a way to their destination. The result is a Q-table. You can see the values ​​in the table to determine what action the agent will take next.

##EXPERIMENTAL RESULTS

The environment and results obtained are displayed below:


| SARSA Simulation |  Output  |
|--|--|
| ![enter image description here](https://github.com/NITHIN1606/python_spring_21.git/GIF.gif) | ![enter image description here](https://github.com/NITHIN1606/python_spring_21/blob/main/Output.jpeg)|

|  Q-Table  |  Final Q-Table |
|--|--|
|  ![enter image description here](https://github.com/NITHIN1606/python_spring_21/blob/main/Q-table.jpeg)| ![enter image description here](https://github.com/NITHIN1606/python_spring_21.git/Final Q table.jpeg) | 

| Analytics 1 |  Analytics 2  |
|--|--|
| ![enter image description here](https://github.com/NITHIN1606/python_spring_21.git/Analytics.jpeg) | ![enter image description here](https://github.com/NITHIN1606/python_spring_21/blob/main/Analytics 2.jpeg)|

| Analytics 3 |
|--|--|
| ![enter image description here](https://github.com/NITHIN1606/python_spring_21.git/Analytics 3.jpeg) |