
# Simulating COVID-19 Spread with Python

This repository contains a Python program that simulates the spread of a virus, using COVID-19 as an example. The simulation leverages Numpy and Matplotlib for mathematical calculations and data visualization.

## Features

- **Virus Simulation:** Models the spread of a virus using parameters such as reproduction number (R0), incubation period, recovery times, and fatality rates.
- **Visualization:** Provides a polar plot animation visualizing the spread, recovery, and fatalities over time.
- **Configurable Parameters:** Allows customization of virus parameters to simulate different scenarios.

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

- `virus.py`: Main script containing the `Virus` class and simulation logic.
- `main()`: Entry point of the script that initializes the virus simulation and starts the animation.

## Visualization

The simulation provides a polar plot animation to visualize the spread of the virus. Here's an example of the visualization:

![Virus Spread Visualization](image/virus.png)

## Contributing

We welcome contributions! Please read our [Contributing Guidelines](CONTRIBUTING.md) for more information.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Inspired by real-world COVID-19 data and modeling.
- Uses Numpy for efficient numerical computations.
- Uses Matplotlib for creating animations and visualizations.
