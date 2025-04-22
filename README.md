# Memory Allocation Strategies Simulation

🎯 **Live Demo**: [Try the Simulation](https://megam1n4.github.io/os-memory-sim1/)

---

## 🟦 Overview

This project is an interactive, browser-based simulation that compares the performance of four classical memory allocation strategies:

- **First Fit**
- **Next Fit**
- **Best Fit**
- **Worst Fit**

It visually represents how these strategies behave when servicing memory requests and releases in dynamic environments.

---

## 🎯 Objective

Simulate and evaluate:

- How different allocation strategies affect **memory utilization**
- How many **holes** each strategy examines to fulfill a memory request
- Behavior under varying request patterns (mean `d` and standard deviation `v`)

---

## 🚀 Features

- 🔘 Select among four strategies
- ⚙️ Adjustable memory settings: `d`, `v`, `n`
- 🧠 Animated memory allocation & release process
- 📊 Graphs:
  - Average Utilization vs. Request Size
  - Average Search Time vs. Request Size
- 🔁 Try different configurations anytime

---

## 🧠 How It Works

### 🔧 Memory Model

- Memory is an array of size `n`
- Positive value → **allocated block**
- Negative value → **hole (free space)**

### 🔁 Simulation Loop

1. **Initialize memory** using normal distribution:
   - Mean request size = `d`
   - Std deviation = `v`
2. For 200 steps:
   - Randomly release one allocated block
   - Coalesce adjacent holes
   - Try up to 5 requests based on the same distribution
   - Log performance metrics

---

## 📊 How Metrics Are Calculated

- **Memory Utilization**

  - `(sum of allocated block sizes) / n`

- **Average Search Time**

  - `average number of holes examined per successful allocation`

- **Allocation Success Rate**
  - `(successful allocations / total attempts) × 100`

---

## 🧪 How to Use

1. Open: [https://megam1n4.github.io/os-memory-sim1/](https://megam1n4.github.io/os-memory-sim1/)
2. Input:
   - Mean (`d`)
   - Std Dev (`v`)
   - Memory Size (`n`)
3. Click **Start Simulation**
4. Click strategy buttons to switch approaches
5. Use **Try Different Parameters** to rerun experiments

---

## 🧑‍🏫 Course Info

- **Course**: COMP 5313 - Advanced Operating Systems
- **Instructor**: Dr. Mary Kim
- **Semester**: Spring 2025
- **Team**: Kernel Krew

---

## 📄 License

This simulation is created for educational purposes only.
All rights reserved © 2025.
