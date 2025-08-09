# 🧮 16-bit Checksum Generator (Logisim)

## 📌 Overview
This project implements a **16-bit checksum generator** using **1’s complement addition** in **Logisim**.  
Checksums are widely used in networking (TCP/IP, UDP) to detect errors in transmitted data.

**Features:**
- Takes **two 16-bit inputs**.
- Performs **1’s complement addition**.
- Handles **carry wrap-around**.
- Outputs the **final 1’s complement checksum**.
- Fully built using **original Logisim** components.

---

## 🛠 How It Works

### 1️⃣ Inputs
Two 16-bit inputs:
- **Low** (lower half of data)
- **High** (upper half of data)

### 2️⃣ Addition
The two inputs are added together using a **16-bit adder**.

### 3️⃣ Carry Wrap-around
If there is a carry-out from the most significant bit (MSB), it is added back to the sum — this is **1’s complement addition**.

### 4️⃣ One’s Complement
The sum is inverted (bitwise NOT) to produce the checksum.

---

## ⚙️ Circuit Components

| Component            | Purpose                                    |
|----------------------|--------------------------------------------|
| **Pin (16-bit)**     | Input data (Low & High)                    |
| **Adder (16-bit)**   | Performs sum of inputs                     |
| **Register**         | Stores intermediate sum                    |
| **AND Gate**         | Detects carry-out                          |
| **Adder 2 (16-bit)** | Adds carry to wrapped sum                   |
| **NOT Gate**         | Produces 1’s complement                    |
| **Output Pin**       | Displays final checksum                    |
| **Splitter**         | Splits/combines multi-bit signals          |
