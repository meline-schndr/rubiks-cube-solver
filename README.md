# Rubik’s Cube Solver using Computer Vision

## Table of contents

- [Overview](#overview)
- [Project Objectives](#project-objectives)
- [System Architecture](#system-architecture)
    - [1. Computer Vision Module](#1-computer-vision-module)
    - [2. Cube Representation](#2-cube-representation)
    - [3. Solving Algorithm](#3-solving-algorithm)
    - [4. Output Generation](#4-output-generation)
- [Technologies Used](#technologies-used)
- [Mathematical Background](#mathematical-background)
- [Limitations](#limitations)
- [Conclusion](#conclusion)
- [License](#license)

## Overview

This project consists in the design and implementation of a **Rubik’s Cube solver** combining **computer vision**, **algorithmic modeling**, and **combinatorial problem solving**.

The system is able to:

- acquire the state of a real Rubik’s Cube using a camera,
- interpret and model this state in a formal internal representation,
- compute a valid sequence of moves that solves the cube,
- output the solution as a list of standard cube instructions.

The project is developed as part of the **second semester of the second and final year of an integrated preparatory cycle**, prior to entering the **Cyberdefense engineering cycle**.

## Project Objectives

The main objectives of this project are:

- to model a complex physical system using appropriate data structures,
- to implement an algorithmic solution to a large combinatorial problem,
- to apply computer vision techniques for real-world data acquisition,
- to justify technical and algorithmic choices in an engineering context.

> [!IMPORTANT] 
> Rather than focusing on optimality, the project emphasizes **clarity, correctness, and explainability** of the implemented solution.

## System Architecture

The system is organized into four main components:

### 1. Computer Vision Module
- Image acquisition using a camera.
- Detection of cube faces and individual stickers.
- Color recognition under varying lighting conditions.
- Mapping detected colors to cube faces.

### 2. Cube Representation

- Formal representation of the cube state.
- Modeling of pieces (corners and edges), their positions and orientations.
- Definition of elementary moves using standard notation (`U`, `D`, `L`, `R`, `F`, `B`).

### 3. Solving Algorithm

- Algorithm implemented from theoretical descriptions found in the literature.
- No use of external “black-box” solving libraries.
- Deterministic and structured approach (e.g. layer-by-layer or staged resolution).
- Use of predefined move sequences with controlled effects on cube state.

> [!NOTE]
> Although the Rubik’s Cube can be formally described using **group theory**, the project adopts a **practical and algorithmic perspective**, exploiting these properties implicitly rather than through heavy mathematical formalism.

### 4. Output Generation

- Generation of an ordered list of moves (e.g. `R`, `U'`, `F2`).
- Optional visualization or textual display of the solution.

## Technologies Used

- **Language:** Python
- **Libraries:**
    - `OpenCV` – image acquisition and processing
    - `NumPy` – data structures and numerical operations


> [!IMPORTANT] 
> All libraries are used strictly as **technical tools**.
> The solving logic itself is entirely implemented within the project.

## Mathematical Background

The Rubik’s Cube can be viewed as a system of permutations acting on a finite set of pieces.
Each move corresponds to a permutation, and sequences of moves correspond to compositions of permutations.

While this framework belongs to **group theory**, the project uses these concepts only insofar as they are useful for:

- structuring the cube representation,
- understanding the effects of move sequences,
- designing a correct and efficient solving strategy.

The focus remains on **algorithmic implementation**, not on theoretical proofs.

## Limitations

The following limitations are acknowledged:

- color detection may be sensitive to lighting conditions,
- the solving algorithm does not guarantee a minimal number of moves or an optimal solution,
- correct acquisition of all cube faces is required for reliable operation.

These constraints are analyzed and discussed, with possible improvements identified.

## Conclusion

This project provides a complete and coherent approach to solving a complex combinatorial problem, from real-world data acquisition to algorithmic resolution.
It demonstrates the ability to:

- model complex systems,
- design and implement non-trivial algorithms,
- make reasoned engineering trade-offs.


The project serves as a strong foundation for further work in areas such as **algorithmic reasoning**, **system robustness**, and **security-oriented problem solving**, which are central to the Cyberdefense cycle.

## License

[LICENSE](https://github.com/meline-schndr/rubiks-cube-solver/tree/main?tab=Apache-2.0-1-ov-file)
