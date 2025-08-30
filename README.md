# FIFO UVM Verification

This repository presents a **SystemVerilog RTL design** of a FIFO buffer and a **UVM-based verification environment**.  
The project demonstrates a complete verification flow including constrained-random stimulus, reference model checking, assertions, and functional coverage.

---

## 📌 Project Objectives
- Design and verify a **synchronous FIFO** in SystemVerilog.
- Develop a **UVM-based testbench** with reusable and modular components.
- Apply **constrained-random testing** to achieve high verification quality.
- Measure verification completeness using **functional coverage** and assertions.

---

## 📂 Repository Structure
```
rtl/ -> RTL implementation of the FIFO
tb/ -> Testbench interfaces
uvm_env/ -> UVM environment components (agent, driver, monitor, scoreboard, etc.)
sequences/ -> UVM sequences (read, write, reset, mixed)
reference_model/ -> Behavioral FIFO model & assertions
coverage/ -> Coverage model and reports
scripts/ -> Simulation scripts (e.g., ModelSim/Questa)
results/ -> Simulation outputs and logs
```

---

## 🛠️ Tools & Requirements
- **Language**: SystemVerilog (IEEE 1800-2017)
- **Verification Methodology**: UVM (IEEE 1800.2)
- **Simulator**: Mentor QuestaSim / ModelSim  
- **Scripts**: `run.do` provided for compilation and simulation

---

## 🚀 How to Run
1. Open **QuestaSim** or **ModelSim**.
2. Compile all source files:
   ```tcl
   do scripts/run.do
   ```
3.Run simulation:
vsim work.top -coverage
run -all
4.Check simulation log in results/report.txt.

📊 Coverage & Results

Achieved functional coverage > 95% across FIFO operations.

Verified scenarios:

Read-only sequences

Write-only sequences

Read-Write combined operations

Reset under active traffic

Coverage reports are available in coverage/.

📚 Learning Outcomes

Practical experience in UVM testbench development.

Building a reference model and scoreboard for result checking.

Applying assertions and coverage-driven verification.

Structuring an academic/industry-standard verification project.
```
