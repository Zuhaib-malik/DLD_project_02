# 🧮 8-bit Checksum Generator (Logisim)

## 📌 Overview
This project implements an **8-bit checksum generator** using **1’s complement addition** in **Logisim**.  
Checksums are widely used in data communication to detect errors during transmission.

**Features:**
- Takes **two 8-bit inputs**.
- Performs **1’s complement addition**.
- Handles **carry wrap-around**.
- Outputs the **final 1’s complement checksum**.
- Fully simulated in **original Logisim**.

---

## 🛠 How It Works

### 1️⃣ Inputs
Two 8-bit inputs:
- **Low** (first byte)
- **High** (second byte)

### 2️⃣ Addition
The two bytes are added together using an **8-bit adder**.

### 3️⃣ Carry Wrap-around
If there is a carry-out from the most significant bit (MSB), it is added back to the sum — this is **1’s complement addition**.

### 4️⃣ One’s Complement
The sum is inverted (bitwise NOT) to produce the final checksum.

---

## ⚙️ Circuit Components

| Component          | Purpose                                    |
|--------------------|--------------------------------------------|
| **Pin (8-bit)**    | Input data (Low & High)                    |
| **Adder (8-bit)**  | Performs sum of inputs                     |
| **Register**       | Stores intermediate sum                    |
| **MUX (8-bit)**    | Select between sum and wrapped sum         |
| **NOT Gate**       | Produces 1’s complement                    |
| **Output Pin**     | Displays final checksum                    |
| **Splitter**       | Splits/combines multi-bit signals          |
| **Clock**          | Controls sequential updates (optional)     |

---

