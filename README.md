# AI Game Bot using NEAT

An AI-powered game that uses the NEAT (NeuroEvolution of Augmenting Topologies) algorithm to train neural networks to play the game autonomously. Watch as the AI learns to navigate through pipes and improve its performance over multiple generations!

## 🎮 Features

- **AI-Powered Gameplay**: Uses NEAT algorithm to evolve neural networks that learn to play the game
- **Real-time Evolution**: Watch multiple birds (AI agents) attempt the game simultaneously
- **Generation Tracking**: Monitor the evolution progress with generation counter and fitness scores
- **Visual Feedback**: See which birds survive and how they adapt their strategies
- **Configurable Parameters**: Easily adjust NEAT parameters in `config.txt`

## 🚀 How It Works

The AI uses a neural network with 3 inputs:
- Bird's current Y position
- Distance to the top pipe
- Distance to the bottom pipe

Based on these inputs, the neural network decides whether the bird should jump or not. The NEAT algorithm evolves these networks over generations, selecting the best performers and creating new variations through mutation and crossover.

## 📋 Requirements

- Python 3.7+
- pygame
- neat-python

## 🛠️ Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd AI-Game-Bot
```

2. Install the required dependencies:
```bash
pip install pygame neat-python
```

## 🎯 Usage

Simply run the main game file:

```bash
python game.py
```

The game will start with a population of 20 AI birds attempting to play Flappy Bird. You'll see:
- Multiple birds flying simultaneously
- Generation counter in the top-left
- Score counter in the top-right
- Birds that crash are removed from the population
- The simulation continues until all birds crash or a bird reaches a score of 101

## ⚙️ Configuration

The NEAT algorithm parameters can be adjusted in `config.txt`:

- **Population Size**: Number of birds per generation (default: 20)
- **Fitness Threshold**: Target score to stop evolution (default: 100)
- **Mutation Rates**: Control how much the networks change between generations
- **Network Structure**: Configure input/output nodes and hidden layer settings

## 🧬 NEAT Algorithm

This project uses the NEAT (NeuroEvolution of Augmenting Topologies) algorithm, which:

1. **Starts Simple**: Begins with minimal neural networks
2. **Evolves Structure**: Adds nodes and connections as needed
3. **Preserves Innovation**: Protects new structural innovations
4. **Speciates**: Groups similar networks to maintain diversity
5. **Selects Fittest**: Keeps the best performers for reproduction

## 📁 Project Structure

```
AI-Game-Bot/
├── game.py          # Main game logic and NEAT implementation
├── config.txt       # NEAT algorithm configuration
├── imgs/            # Game assets
│   ├── bird1.png    # Bird animation frame 1
│   ├── bird2.png    # Bird animation frame 2
│   ├── bird3.png    # Bird animation frame 3
│   ├── pipe.png     # Pipe obstacle
│   ├── base.png     # Ground/base
│   └── bg.png       # Background
└── README.md        # This file
```

## 🎮 Game Mechanics

- **Bird Physics**: Realistic gravity and jump mechanics
- **Collision Detection**: Precise pixel-perfect collision detection using pygame masks
- **Scoring**: Points awarded for successfully passing through pipes
- **Fitness Function**: Birds earn fitness points for survival time and passing pipes
- **Penalties**: Negative fitness for collisions

## 🔬 Learning Process

1. **Generation 1**: Random neural networks attempt the game
2. **Selection**: Best performing birds are selected for reproduction
3. **Evolution**: New generation created through mutation and crossover
4. **Improvement**: Each generation typically performs better than the last
5. **Convergence**: Eventually finds optimal strategies for the game

## 🎯 Expected Results

- **Early Generations**: Birds crash immediately or make random jumps
- **Mid Generations**: Birds start to understand basic timing
- **Later Generations**: Birds develop sophisticated strategies and can achieve high scores
- **Final Result**: AI that can consistently play Flappy Bird better than most humans!
