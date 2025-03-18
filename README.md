# Graph Coloring using Genetic Algorithm

## Overview
This project implements a **Genetic Algorithm (GA)** to solve the **Graph Coloring Problem**, where the goal is to assign colors to the vertices of a graph such that no two adjacent vertices share the same color. The aim is to minimize the number of colors used while avoiding conflicts (i.e., adjacent vertices having the same color).

## 📂 Input Files
- The program begins by reading `.txt` files containing graph data. These files specify the graph's structure, including vertices and edges.

## 🔍 Hyperparameter Search (Grid Search)
- A **grid search** is performed to find the best hyperparameters for the genetic algorithm. These hyperparameters include:
  - Population size
  - Mutation rate
  - Crossover points

## 🧪 Tests on Files `test1.txt`, `test2.txt`
- Once the optimal hyperparameters are found, the algorithm is tested on multiple input files to evaluate its performance.

## Algorithm Steps:

### 1. **Initialization**
   - A population of **random colorings** is created, where each individual is a possible solution to the graph coloring problem.

### 2. **Selection**
   - **Tournament selection** is used to choose individuals for reproduction based on their fitness.
   - Random selection is introduced to maintain diversity in the population.

### 3. **Crossover**
   - **Multi-point crossover** combines parts of two parent solutions to create a child solution.
   - The child solution is **repaired** to ensure no conflicts (adjacent vertices with the same color).

### 4. **Mutation**
   - Mutation introduces small **random changes** to an individual’s coloring.
   - After mutation, the coloring is **repaired** to resolve any conflicts.

### 5. **Fitness Evaluation**
   - The **fitness** of each individual is evaluated by:
     - Counting the number of **conflicts** (adjacent vertices sharing the same color).
     - Counting the number of **unique colors** used.

### 6. **Diversity and Mutation Rate Adjustment**
   - The **mutation rate** is adjusted based on the population's diversity.
     - When diversity is low, the mutation rate increases to encourage exploration.
     - When diversity is high, the mutation rate decreases to encourage exploitation.

## 💾 Results Logging
- The results of each generation, including the number of colors used, fitness score, mutation rate, and population diversity, are saved to a **CSV file** for further analysis.


## 🚀 Exécution sur Google Colab  
Vous pouvez exécuter ce projet directement sur Google Colab en suivant ce lien :  

[![Ouvrir sur Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1b9sDAfJgMbeRnrYFH1OGhED9Fg5LICbF?usp=sharing)

