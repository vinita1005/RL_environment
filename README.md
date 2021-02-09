# RL_environment
![caption](https://github.com/vinita1005/RL_environment/blob/main/RL_env_render.gif)
# Abstract

In this project, a reinforcement learning algorithm SARSA is implemented to enable an
agent to learn and solve an environment such that we get a maximized reward. The agent
learns about the environment by taking suitable actions and progressing onto the next
states in the environment. After enough exploration, the agent can then take optimal
path to solve the environment based on his previous knowledge.

# Environment

An environment in RL is the physical world in which the agent acts in. This environment
can be of two types:

Deterministic:
A deterministic environment is the one in which agent’s current state and current action
uniquely determine the outcome. This type of environment is fully observable.

Stochastic:
An environment is called Stochastic if it is random in nature. This means that the current
state and action do not determine the outcome. This type of environment is difficult to
analyse as you never know in which state the agent could end up being. Here, you have
to store the outcomes of previous states as well to be able to predict your agent’s next
state.

In this project we have a 5x5 grid world. We have obstacles and a goal state. Rewards
are assigned such that the agent knows to get the maximized reward it has to reach the
goal state. Moreover, most of the times the agent will take a random action based on the
action set to add some randomness to the environment.

# Blocks in the env:

• yellow block - Agent’s current position

• green block - Goal state

• grey blocks - Obstacles

# Actions

Actions define the agent’s behaviour of moving in a certain direction.
The Action set is defined as:

Action = A 2 { down, up, right, left }

In numerical format:
Action = A 2 { 0, 1, 2, 3 }

# States

In a 5x5 grid environment, we have 25 states. We have starting state at (0,0). The goal
state is at (4,4). We also have obstacles as shown in the environment diagram.

# Rewards

Rewards are returned outcomes when the agent takes certain action and end’s up in a
certain state.

Here, the reward set is defined as:
R 2 {-20, -10, 0, +100}

• The -20 reward is returned when the agent hits an obstacle state. This will add
onto the agent’s experience that it should avoid this state.

• +100 reward is given when agent reaches the goal state.

• Now, the -10 reward is given in two cases - when the agent takes an action and
ends up in the same state or when it goes away from the goal state. This
is added to ensure that agent always keeps moving forward towards the goal state
and does not stay idle.

• The rest of the states return just a 0.
