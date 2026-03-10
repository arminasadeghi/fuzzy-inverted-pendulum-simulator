# Fuzzy Inverted Pendulum Simulator

This project is an inverted pendulum simulator controlled by a custom-built Fuzzy Logic Controller.

The goal of this project is to provide a robust environment for designing and testing fuzzy controllers to solve the classic inverted pendulum control problem—preventing a pendulum with a high center of mass from falling over by applying dynamic, calculated forces to its cart.

It is implemented in **Python 2.7** using `pygame` for real-time visualization and `pyfuzzy` for fuzzy inference.

## ✨ Features

- **Inverted Pendulum Simulation**  
  Realistic physics simulation of a cart–pendulum system with configurable physical parameters.

- **Fuzzy Logic Controller**  
  Controller defined via Fuzzy Control Language (FCL) files, featuring custom rule evaluation and center of gravity (COG) defuzzification.

- **Configurable Environment**  
  Simulation variables (time step, initial angle, controller path, etc.) are adjustable via `.ini` configuration files.

- **Real-time Visualization**  
  Watch the cart and pendulum balance dynamically using the `pygame`-based interface.

## 📁 Project Structure

- `main.py` – Entry point that wires together the config, world, controller, simulator, GUI, and manager.
- `world.py` – Defines the physical model and state of the cart–pendulum system.
- `simulator.py` – Numerical integration and state update for each simulation step.
- `controller.py` – Fuzzy controller that loads an FCL file, evaluates rules, and computes the control force.
- `gui.py` – `pygame`-based visual rendering of the cart and pendulum.
- `manager.py` – High-level simulation loop and coordination.
- `conf.py` – Configuration loading and management.
- `configs/` – `.ini` configuration files (e.g., `default.ini`, `full.ini`).
- `controllers/` – FCL controller definitions (e.g., `simple.fcl`, `complex.fcl`).
- `install-deps.sh` – Helper script to install Python dependencies.
- `requirements.txt` – Python dependency list.

Additional helper modules:

- `CartPosition.py`, `CartVelocity.py`
- `PendulumAngle.py`, `PendulumVelocity.py`
- `Force.py`
