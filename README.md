# Taxi-v3 Q-Learning
A simple Q-learning implementation in OpenAI Gym's "Taxi-v3" environment.

## What is  OpenAI Gym's "Taxi-v3" environment

![p](https://www.gymlibrary.dev/_images/taxi.gif)


**The Taxi-v3 environment**

The Taxi-v3 environment is a strategic simulation, offering a grid-based arena where a taxi navigates to address daily challenges akin to those faced by a taxi driver. This environment is defined by a 5x5 grid where the taxi's mission involves picking up a passenger from one of four specific locations (marked as Red, Green, Yellow, and Blue) and dropping them off at another designated spot. The goal is to accomplish this with minimal time on the road to maximize rewards, emphasizing the need for route optimization and efficient decision-making for passenger pickup and dropoff.

**Key Components**:

**Action Space**: Comprises six actions where 0 moves the taxi south, 1 north, 2 east, 3 west, 4 picks up a passenger, and 5 drops off a passenger.
**Observation Space**: Comprises 500 discrete states, accounting for 25 taxi positions, 5 potential passenger locations, and 4 destinations.
**Rewards System**: Includes a penalty of -1 for each step taken without other rewards, +20 for successful passenger delivery, and -10 for illegal pickup or dropoff actions. Actions resulting in no operation, like hitting a wall, also incur a time step penalty.

Here are the key characteristics and components of the "Taxi-v3" environment:


1) **Grid World**
   * The environment consists of a grid world with a fixed size.
   * The grid world includes walls, empty cells, passenger locations, a taxi, and a destination location.


2) **Taxi and Passengers**
    * The taxi is represented as a yellow rectangle, and its position on the grid can change.
    * Passengers are represented by letters (R, G, Y, and B) that indicate their destinations.
    * Passengers are initially located at random positions within the grid.


3) **Destination Locations**
    * There are four fixed destinations represented by the corresponding letters (R, G, Y, and B).
    * Passengers request rides to one of these destinations.


4) **Objective**
    * The objective of the taxi is to pick up passengers and drop them off at their requested destinations while navigating the grid world.


[Complete Details](https://www.gymlibrary.dev/environments/toy_text/taxi/)



The agent (the taxi) receives a reward for successful pickups and drop-offs and penalties for illegal moves, such as hitting walls or attempting to pick up passengers who are not at the designated location.

The action space consists of discrete actions that the taxi can take, including moving in four directions (up, down, left, right), picking up a passenger, and dropping off a passenger.
