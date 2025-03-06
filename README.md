# Deep Traffic Simulation

A self-driving car simulation environment using reinforcement learning, built with Python, TensorFlow, and Pygame. The project simulates autonomous vehicles learning to navigate through traffic while optimizing for speed and safety.

## Features

- Realistic traffic simulation with multiple AI-controlled vehicles
- Advanced visualization system with:
  - Top-down road view
  - 3D perspective road view
  - Speed gauge
  - Input vision display
  - Action visualization
  - Score tracking
- Multiple AI agent types:
  - Deep Q-Network (DQN) based agent
  - Aggressive driving agent
  - Sticky (lane-following) agent
- Configurable vision parameters for AI agents
- Performance metrics tracking and visualization
- Real-time visualization of agent decision making

## Technical Details

### Neural Network Architecture
- Input: State representation (36x3x1)
- Convolutional layers for spatial feature extraction
- Dense layers for action-value prediction
- Output: Q-values for 5 possible actions (Accelerate, Decelerate, Maintain, Left, Right)

### Learning Algorithm
- Deep Q-Learning with experience replay
- Target network for stable learning
- Epsilon-greedy exploration strategy
- Configurable hyperparameters

### Environment
- Multi-lane highway environment
- Dynamic speed control
- Collision detection
- Safety constraints
- Performance scoring system

## Requirements

- Python 3.x
- TensorFlow
- Pygame
- NumPy
- Pillow (PIL)
- Other dependencies listed in requirements.txt

## Installation

1. Clone the repository:
   git clone https://github.com/nisargbhatt09/rl-self-driving-car/
2. Install dependencies:
   pip install -r requirements.txt

## Usage

Run the simulation:
python gui.py


Configure simulation parameters in `config.py`:
- Vision parameters (VISION_W, VISION_F, VISION_B)
- Learning parameters (LEARNING_RATE, BATCH_SIZE)
- Visualization settings (VISUALENABLED)
- Training episodes and testing parameters

## Project Structure

- `car.py`: Vehicle class and movement logic
- `cnn.py`: Neural network architecture
- `deep_traffic_agent.py`: DQN agent implementation
- `gui.py`: Main simulation interface
- `players/`: Different AI agent implementations
- `advanced_view/`: 3D visualization components
- `config.py`: Configuration parameters
