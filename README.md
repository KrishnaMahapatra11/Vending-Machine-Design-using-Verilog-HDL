# FSM-Based Vending Machine Using Verilog HDL

This project implements a Finite State Machine (FSM)-based vending machine using Verilog HDL. The vending machine supports four different items and two coin denominations (5 and 10). The design handles multiple states for each item and ensures accurate operation, including dispensing the item and returning change.

---

## Features

- **Items:**  
  - Item 1: Cost 15  
  - Item 2: Cost 25  
  - Item 3: Cost 35  
  - Item 4: Cost 45  

- **Coins Accepted:**  
  - Coin of 5  
  - Coin of 10  

- **Functionalities:**  
  - Dispenses the selected item once the required amount is entered.  
  - Returns change if the amount inserted exceeds the item's cost.  
  - Reset functionality to initialize the system.  

---

## Files

### 1. **`tb.v`**  
   Testbench file to simulate and verify the vending machine functionality. It includes:
   - Clock initialization.
   - Input stimulus for various scenarios.
   - Waveform dumping for analysis.

### 2. **`vending_machine.v`**  
   Main module and submodules implementing the FSM-based vending machine. Includes:
   - `Firstitem`, `Seconditem`, `Thirditem`, and `Fourthitem` modules for each item's logic.  
   - `VendingMachine` module to integrate all items and manage user selection.

---

## Design Overview

- **FSM Design:**  
  Each item is implemented using a unique FSM with states corresponding to the total inserted amount. Transitions occur based on the coin input and current state.

- **Hierarchy:**  
  - **Main Module:** `VendingMachine`  
  - **Submodules:**  
    - `Firstitem`: Handles item costing 15.  
    - `Seconditem`: Handles item costing 25.  
    - `Thirditem`: Handles item costing 35.  
    - `Fourthitem`: Handles item costing 45.  

---

## Tools Used

- **Design Language:** Verilog HDL  
- **Simulation Tool:** Waveform analysis using VCD  
- **Synthesis Tool:** Xilinx ISE  
- **FPGA Platform:** Spartan-3 FPGA (for implementation)
