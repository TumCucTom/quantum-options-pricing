# Quantum Monte Carlo for Exotic Options

## Overview
This repository contains the codebase and resources for a project focused on leveraging Quantum Monte Carlo (QMC) simulations to price and analyze exotic financial options. Exotic options, such as Asian, barrier, and lookback options, present complex challenges in derivative pricing that can be addressed using the computational advantages of quantum computing.

---

## Features
- **Classical Monte Carlo Benchmarking**: A classical Monte Carlo (CMC) implementation for comparison.
- **Quantum Algorithms**: Quantum circuits for amplitude estimation and stochastic path simulations.
- **Hybrid Simulation Framework**: Combines quantum and classical resources to handle high-dimensional problems efficiently.
- **Flexible Parameters**: Support for customizable option types, strike prices, volatilities, and maturities.
- **Visualization**: Interactive plots for payoff distributions, pricing trajectories, and quantum-classical comparisons.

---

## Technical Stack
### Quantum Frameworks
- [Qiskit](https://qiskit.org/): For building and executing quantum circuits.
- [PennyLane](https://pennylane.ai/): For hybrid quantum-classical algorithms.

### Classical Support
- Python Libraries:
  - `numpy`, `scipy`: Numerical computations.
  - `pandas`: Data manipulation.
  - `matplotlib`, `seaborn`: Visualization.
- Quantum and Classical Integration:
  - `Amazon Braket`, `Azure Quantum`, or other quantum platforms for hybrid simulations.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/quantum-monte-carlo-exotic-options.git
   ```
2. Navigate to the project directory:
   ```bash
   cd quantum-monte-carlo-exotic-options
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage
### Running Simulations
1. **Classical Benchmark**:
   Run classical Monte Carlo simulations to price exotic options:
   ```bash
   python classical_simulation.py --option-type asian --strike 100 --maturity 1
   ```

2. **Quantum Simulation**:
   Execute QMC simulations using a supported quantum backend:
   ```bash
   python quantum_simulation.py --option-type asian --strike 100 --maturity 1 --backend ibmq_qasm_simulator
   ```

3. **Hybrid Framework**:
   Combine classical preprocessing with quantum computation:
   ```bash
   python hybrid_simulation.py --option-type barrier --strike 120 --volatility 0.2
   ```

### Configuration
Modify the `config.json` file to set global parameters such as backends, precision levels, and paths for saving results:
```json
{
    "backend": "ibmq_qasm_simulator",
    "shots": 1024,
    "output_dir": "results/"
}
```

---

## Project Structure
```
quantum-monte-carlo-exotic-options/
├── classical_simulation.py     # Classical Monte Carlo implementation
├── quantum_simulation.py       # Quantum Monte Carlo implementation
├── hybrid_simulation.py        # Hybrid simulation framework
├── config.json                 # Configuration file
├── results/                    # Output directory for simulation results
├── tests/                      # Unit tests
├── requirements.txt            # Python dependencies
├── LICENSE                     # License file
└── README.md                   # Project documentation
```

---

## Roadmap
- [ ] Extend support for additional exotic options (e.g., chooser, rainbow options).
- [ ] Optimize quantum circuits for noisy intermediate-scale quantum (NISQ) devices.
- [ ] Integrate real-time market data feeds for dynamic pricing.
- [ ] Develop a web-based frontend for user-friendly access.

---

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your proposed changes. Ensure your code follows the existing style and includes tests.

---

## License
This project is licensed under a [private license](LICENSE). The content, code, and associated intellectual property are proprietary and restricted for personal and collaborative use only. Redistribution or commercial use without explicit permission is prohibited. For inquiries, contact [tokbale@outlook.com].

---

## Acknowledgments
- IBM Quantum and Qiskit for tools and tutorials.
- Quantum computing community for resources and inspiration.

For questions or feedback, feel free to open an issue or contact [tokbale@outlook.com].

