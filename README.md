# 🚪 Ultrasonic Sensor Gate Controller  

This Arduino project controls a servo-operated gate using an **HC-SR04 ultrasonic sensor**. When an object (e.g., a person) is detected within **50cm**, the gate opens (servo rotates), a **blue LED lights up**, and a **gentle buzzer beeps**. After **5 seconds** of no detection, the gate closes, and a **red LED turns on**.  

---

## 📦 **Hardware Setup**  
### **Components Required**  
- Arduino (Uno/Nano)  
- HC-SR04 Ultrasonic Sensor  
- SG90 Servo Motor  
- Red & Blue LEDs (with resistors, ~220Ω)  
- Buzzer (passive)  
- Jumper Wires  

### **Wiring Guide**  
| Component       | Arduino Pin |
|----------------|------------|
| HC-SR04 Trigger | D2         |
| HC-SR04 Echo    | D3         |
| Red LED (Anode) | D4         |
| Red LED (Cathode) | D8        |
| Blue LED (Cathode) | D7       |
| Blue LED (Anode) | D5         |
| Servo Signal    | D6         |
| Buzzer (+)      | D12        |

> **Note:** Ensure proper grounding (`GND`) for all components.  

---

## ⚙️ **Software Setup**  
### **1. Install Required Library**  
This code uses the **Servo library**, which comes pre-installed with Arduino IDE. If missing:  
- Open Arduino IDE → **Sketch → Include Library → Manage Libraries** → Search for **"Servo"** → Install.  

### **2. Upload the Code**  
1. Copy the provided code into a new Arduino sketch.  
2. Select the correct board (**Tools → Board → Arduino Uno/Nano**).  
3. Select the correct port (**Tools → Port**).  
4. Click **Upload** (▶️).  

---

## 🎛️ **How It Works**  
- **Detection**: Ultrasonic sensor measures distance (object within **50cm** triggers the gate).  
- **Gate Control**:  
  - **Open**: Servo moves to **90°**, blue LED on, buzzer beeps gently.  
  - **Close**: After **5 seconds** of no detection, servo returns to **0°**, red LED on.  
- **Buzzer**: Short beeps (**50ms ON, 500ms cycle**) while gate is open.  

---

## 🔧 **Troubleshooting**  
- **Servo jitters?** Check power supply (use external power if needed).  
- **Sensor not working?** Verify wiring (`Trigger` → `D2`, `Echo` → `D3`).  
- **LEDs not lighting?** Confirm correct polarity and resistor values.  

---

## 📜 **License**  
MIT License – Free to use, modify, and distribute.  

**Happy Coding!** 💻⚡  

---

### 🔗 **Need Help?**  
Open an issue or contribute on [GitHub](https://github.com/your-repo-link).  

> "Born to Code" – Because every great project starts with a single line. 🚀
