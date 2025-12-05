# 🔐 Digital Locking System with Unauthorized Access Alert

A hardware-based digital security system built entirely using **combinational and sequential logic ICs**, designed to provide password authentication, access control, and unauthorized access alerts without using any microcontroller.
This project was developed as part of **23ECE381 – Open Laboratory I**.

---

## 📌 Features

* **Customizable password** using keypad input
* **4-digit authentication** using shift registers and comparators
* **Correct password →** Green LED + Motor activation
* **Incorrect password →** Red LED + Buzzer alert
* **Reset function** to clear user inputs
* Built using **encoder, demultiplexer, shift registers, D flip-flops, comparators, AND/OR logic**

---

## 🧩 System Architecture

### **1. Input Stage (Keypad + Encoder)**

* User enters digits using a numeric keypad
* IC **74147** converts keypress to 4-bit binary  

### **2. Password Storage & Control**

* **74194 Shift Registers** store both saved password and entered password
* **4013 D Flip-Flop** tracks digit count
* **4555 Demultiplexer** switches between **Set Mode** and **User Mode**

### **3. Authentication Logic**

* **4-bit Magnitude Comparators (7485)** compare each digit 
* **AND gate** → All digits match
* **OR gate** → Any digit mismatches

### **4. Output Action**

* **Match:** Green LED + Motor runs
* **Mismatch:** Red LED + Buzzer alert 

---

## 🛠️ Components Used

* Push buttons
* **74147** – Priority Encoder
* **74194** – 4-bit Shift Registers
* **4013** – D Flip-Flop
* **4555** – Decoder/Demultiplexer
* **7485** – Magnitude Comparator
* AND/OR/NOT gates
* LEDs, buzzer, motor driver (L293D)

---

## 🚀 Working Principle

1. User enters digits → Encoded to 4-bit binary
2. Digits are sequentially stored in shift registers
3. Comparator checks each digit with the saved password
4. Final AND/OR logic decides:

   * **Correct password → Unlock**
   * **Wrong password → Unauthorized alert**

Simulation outputs from the results:

* **Match:** Motor + green LED 
* **Mismatch:** Buzzer + red LED 

---

## 📊 Simulation Results

* Demonstrated correct entry (1111) and incorrect entry (1234)
* Clear visualization of match/mismatch logic using LEDs, buzzer, and motor



Just tell me what vibe you want — professional, aesthetic, or minimal!
