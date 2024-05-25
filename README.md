
# Simulating COVID-19 Spread with Python

This repository contains a Python program that simulates the spread of a virus, using COVID-19 as an example. The simulation leverages Numpy and Matplotlib for mathematical calculations and data visualization.

## Features

- **Virus Simulation:** Models the spread of a virus using parameters such as reproduction number (R0), incubation period, recovery times, and fatality rates.
- **Visualization:** Provides a polar plot animation visualizing the spread, recovery, and fatalities over time.
- **Configurable Parameters:** Allows customization of virus parameters to simulate different scenarios.
- **Dynamic Plotting:** Uses Matplotlib's animation capabilities to provide real-time updates of the simulation.

## Installation

### Prerequisites

- Python 3.6+
- Numpy
- Matplotlib

### Installing Dependencies

To install the necessary dependencies, run:

```bash
pip install numpy matplotlib
```

## Usage

Clone the repository and run the simulation:

```bash
git clone https://github.com/yourusername/simulating-covid-19-python.git
cd simulating-covid-19-python
python virus.py
```

## Simulation Parameters

The simulation uses the following parameters for COVID-19:

```python
COVID19_PARAMS = {
    "r0": 2.28,
    "incubation": 5,
    "percent_mild": 0.8,
    "mild_recovery": (7, 14),
    "percent_severe": 0.2,
    "severe_recovery": (21, 42),
    "severe_death": (14, 56),
    "fatality_rate": 0.034,
    "serial_interval": 7
}
```

### Description of Parameters

- **r0:** Basic reproduction number.
- **incubation:** Incubation period in days.
- **percent_mild:** Percentage of mild cases.
- **mild_recovery:** Range of recovery time for mild cases in days.
- **percent_severe:** Percentage of severe cases.
- **severe_recovery:** Range of recovery time for severe cases in days.
- **severe_death:** Range of time to death for severe cases in days.
- **fatality_rate:** Fatality rate of the virus.
- **serial_interval:** Average time between successive cases in a chain of transmission.

## Code Structure

- `virus.py`: Main script that runs the simulation.
- `README.md`: Project documentation.
- `requirements.txt`: List of dependencies.

## Simulation Process

1. **Initialization**: The `Virus` class initializes the plot and sets up the initial parameters for the simulation.
2. **Simulation Loop**: The simulation updates the state of the population at each time step, recalculating the number of infected, recovered, and deceased individuals based on the virus parameters.
3. **Visualization**: The current state of the simulation is visualized using Matplotlib, with annotations for the day count and the number of infected individuals.

## Prioritization and Scope

### Tackled

- **Core Simulation Mechanics**: Focused on accurately simulating virus spread using key epidemiological parameters.
- **Data Visualization**: Implemented clear and informative visualizations to track the progress of the simulation.

### Not Tackled

- **Advanced Epidemiological Models**: Did not include more complex models like SEIR (Susceptible-Exposed-Infected-Recovered) due to scope limitations.
- **User Interface**: The current version uses a simple script-based interaction rather than a full-fledged GUI.

## Lessons Learned

- **Understanding Epidemiology**: Gained a deeper understanding of how viruses spread and the importance of different epidemiological parameters.
- **Python and Matplotlib**: Improved skills in using Python for scientific computing and data visualization.

## Challenges and Solutions

- **Animation Performance**: Ensuring the animation runs smoothly was challenging. Optimized the plotting functions to handle large datasets efficiently.
- **Parameter Sensitivity**: Finding the right balance of parameters to produce realistic simulations required extensive testing and validation.

## Visualization

Visualization of the virus spread:

![Virus Spread Simulation](image/virus.png)
