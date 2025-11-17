# Quantum Dice Simulator 

This project simulates a **quantum dice** using Qiskit. Instead of using classical randomness, it relies on real quantum measurements to generate unbiased dice outcomes (1–6). The code uses a 3-qubit circuit, Hadamard gates for superposition, and measurement results to map outcomes to dice values.

---

## Features

* Uses **QuantumCircuit** from Qiskit.
* Generates **true quantum randomness**.
* Maps 3-qubit measurement results to integers between **1 and 6**.
* Ignores invalid outcomes (0 and 7) to maintain fairness.
* Plots a histogram of 1000 quantum dice rolls.

---

##  Code Overview

### **1. `quantum_dice_single_roll()`**

This function:

* Creates a 3-qubit quantum circuit.
* Applies Hadamard gates to generate equal superposition.
* Measures all qubits.
* Converts the measured bitstring into a number.
* Returns only values between 1 and 6.

### **2. `generate_many_rolls(n)`**

Generates **n** quantum dice values by repeatedly calling the roll function.

### **3. Main Execution Block**

* Rolls the dice 1000 times.
* Prints the first 10 results.
* Shows a histogram of the distribution.

---

##  Requirements

Make sure the following packages are installed:

```bash
pip install qiskit numpy matplotlib
```

---

##  How to Run

1. Clone the repository:

```bash
git clone <your-repo-url>
cd <repo-folder>
```

2. Run the script:

```bash
python quantum_dice.py
```

3. You will see:

* First 10 quantum dice values printed in the console.
* A histogram showing distribution of 1000 rolls.

---

## How It Works (Simple Explanation)

* Quantum gates put qubits into all possible states at once.
* Measurement collapses them into one random state.
* 3 qubits → values from 0 to 7.
* Only numbers 1–6 are accepted.

This ensures the dice behaves as a **fair quantum random number generator**.

---

##  Notes

* If you have a real IBM Quantum account, you can modify the backend to run on actual hardware.
* Increase `shots` or `n` to test uniformity.

---

## License

This project is open-source. Feel free to use or modify it.

---

##  Contributions

Pull requests are welcome! If you'd like to add improvements—visualizations, real backend support, or GUI—go ahead.

---

Happy Quantum Rolling! 
