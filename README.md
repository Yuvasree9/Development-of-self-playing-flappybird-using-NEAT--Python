# Development-of-self-playing-flappybird-using-NEAT--Python
# Flappy Bird with NEAT Python

## Project Overview

This project implements the Flappy Bird game using Python and employs the NEAT (NeuroEvolution of Augmenting Topologies) algorithm to train an AI to play the game. The project consists of two primary files:

1. `flappy.py`: Contains the game implementation and NEAT algorithm integration.
2. `configure-feedforward.txt`: Contains the configuration settings for the NEAT algorithm.

## Game Development (`flappy.py`)

The `flappy.py` script is responsible for setting up the Flappy Bird game environment, defining the bird, pipe, and base classes, and integrating the NEAT algorithm to train the bird to play the game autonomously.

### Key Components

1. **Game Setup**
   - Initialize game window, load images, and define game constants.

2. **Bird Class**
   - Handles the bird's movement, animation, and collision detection.

3. **Pipe Class**
   - Manages the pipes' generation, movement, and collision detection with the bird.

4. **Base Class**
   - Represents the moving base (ground) in the game.

5. **Game Loop**
   - Controls the game's main loop, including event handling, updating game state, and rendering.

6. **NEAT Integration**
   - Implements NEAT to evolve a neural network that controls the bird's actions based on game state inputs.

## NEAT Configuration (`configure-feedforward.txt`)

The `configure-feedforward.txt` file contains the NEAT algorithm's configuration parameters, which define how the neural networks are evolved.

### Key Parameters

- **[NEAT]**
  - `fitness_criterion`: Criterion used to measure fitness (max).
  - `fitness_threshold`: Threshold for fitness to be considered successful (100).
  - `pop_size`: Population size (50).
  - `reset_on_extinction`: Whether to reset on extinction (False).

- **[DefaultGenome]**
  - `activation_default`: Default activation function for nodes (tanh).
  - `activation_mutate_rate`: Mutation rate for activation function (0.0).
  - `aggregation_default`: Default aggregation function for nodes (sum).
  - `aggregation_mutate_rate`: Mutation rate for aggregation function (0.0).
  - `bias_init_mean`: Initial mean for bias (0.0).
  - `bias_init_stdev`: Initial standard deviation for bias (1.0).
  - `bias_max_value`: Maximum value for bias (30.0).
  - `bias_min_value`: Minimum value for bias (-30.0).
  - `bias_mutate_power`: Mutation power for bias (0.5).
  - `bias_mutate_rate`: Mutation rate for bias (0.7).
  - `bias_replace_rate`: Replacement rate for bias (0.1).
  - `compatibility_disjoint_coefficient`: Disjoint coefficient for genome compatibility (1.0).
  - `compatibility_weight_coefficient`: Weight coefficient for genome compatibility (0.5).
  - `conn_add_prob`: Probability of adding a connection (0.5).
  - `conn_delete_prob`: Probability of deleting a connection (0.5).
  - `enabled_default`: Default state of connections (enabled).
  - `enabled_mutate_rate`: Mutation rate for connection enablement (0.01).
  - `feed_forward`: Whether the network is feedforward (True).
  - `initial_connection`: Initial connection state (full).
  - `node_add_prob`: Probability of adding a node (0.2).
  - `node_delete_prob`: Probability of deleting a node (0.2).
  - `num_hidden`: Number of hidden nodes (0).
  - `num_inputs`: Number of input nodes (3).
  - `num_outputs`: Number of output nodes (1).
  - `response_init_mean`: Initial mean for node response (1.0).
  - `response_init_stdev`: Initial standard deviation for node response (0.0).
  - `response_max_value`: Maximum value for node response (30.0).
  - `response_min_value`: Minimum value for node response (-30.0).
  - `response_mutate_power`: Mutation power for node response (0.0).
  - `response_mutate_rate`: Mutation rate for node response (0.0).
  - `response_replace_rate`: Replacement rate for node response (0.0).
  - `weight_init_mean`: Initial mean for connection weights (0.0).
  - `weight_init_stdev`: Initial standard deviation for connection weights (1.0).
  - `weight_max_value`: Maximum value for connection weights (30).
  - `weight_min_value`: Minimum value for connection weights (-30).
  - `weight_mutate_power`: Mutation power for connection weights (0.5).
  - `weight_mutate_rate`: Mutation rate for connection weights (0.8).
  - `weight_replace_rate`: Replacement rate for connection weights (0.1).

- **[DefaultSpeciesSet]**
  - `compatibility_threshold`: Threshold for species compatibility (3.0).

- **[DefaultStagnation]**
  - `species_fitness_func`: Fitness function for species (max).
  - `max_stagnation`: Maximum stagnation generations (20).
  - `species_elitism`: Number of elite species (2).

- **[DefaultReproduction]**
  - `elitism`: Number of elite individuals (2).
  - `survival_threshold`: Threshold for survival (0.2).

## Running the Project

To run the project, follow these steps:

 **Install Dependencies**
   ```bash
   pip install neat-python pygame
```
## Understanding NEAT

NEAT is a genetic algorithm designed to evolve neural networks. It uniquely evolves both the topology and weights of the networks, starting with simple networks and gradually complexifying them through mutations and crossovers. The goal is to evolve a network that can control the bird to navigate through the pipes effectively.

### Key Features of NEAT

- **Speciation**: Protects new innovations by grouping similar individuals into species.
- **Complexification**: Gradually increases the complexity of the networks by adding new nodes and connections.
- **Crossover**: Combines the genomes of parent networks to produce offspring.

By using NEAT, this project aims to create an AI that learns to play Flappy Bird autonomously, improving its performance over successive generations.

## Conclusion

This project demonstrates the application of the NEAT algorithm in training an AI to play Flappy Bird. The combination of Python's Pygame library for game development and the NEAT algorithm for AI training provides a robust framework for creating intelligent game agents. The configuration settings in `configure-feedforward.txt` allow fine-tuning of the NEAT algorithm to achieve optimal performance.

   
