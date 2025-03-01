# Smart Street Light System Using IR Sensor

## 📌 Introduction
Street lights play a crucial role in ensuring road safety and security, but conventional systems consume excessive energy. This project proposes a **Smart Street Light System** that optimizes energy usage while maintaining safety by integrating **Light Dependent Resistors (LDRs), Infrared (IR) sensors, and Rain Sensors**.

## 🔧 Project Concept
The system comprises the following key components:

- **LDR (Light Dependent Resistor):** Detects ambient light levels to turn lights on/off automatically.
- **IR Sensor:** Detects the presence of vehicles or pedestrians, controlling light intensity dynamically.
- **Rain Sensor:** Adjusts lighting conditions based on rainfall.
- **Arduino Uno:** Microcontroller that processes sensor inputs and controls the lighting system.

## 🎯 Objectives
1. **Energy Optimization:** Reduce unnecessary energy consumption by activating lights only when needed.
2. **Adaptive Brightness:** Adjust light intensity based on real-time traffic and weather conditions.
3. **Cost Reduction:** Lower operational expenses for municipalities.
4. **Safety Enhancement:** Ensure well-lit roads when required.
5. **Environmental Sustainability:** Reduce carbon footprint and light pollution.

## ⚙️ Working Principle
### 1. **Daytime Operation:**
   - LDR detects sufficient sunlight → Street lights remain OFF.
   - Energy savings during daylight hours.

### 2. **Evening/Night Operation:**
   - LDR senses darkness → Street lights turn ON.
   - IR sensors monitor road activity:
     - No movement → Lights stay DIM.
     - Motion detected → Lights brighten.
   - Rain sensor adjusts light intensity during rainfall.

## 📑 Literature Survey
The project builds upon previous research on **Smart Street Lighting Systems**, leveraging IoT and automation. Some key studies:
- **"Smart Street Lighting Using IoT" (2020):** Highlights the impact of IoT-based adaptive lighting in reducing energy costs by 50%.
- **"Smart Street Light System" (2022):** Examines various sensor technologies such as IR and PIR sensors for efficiency.
- **"IoT-Based Smart Street Lighting Surveillance System" (2022):** Focuses on real-time control and cost-effectiveness.

## 🔄 Implementation

### Block Diagrams

![blockdiagram](https://github.com/sandesh-ar/sem-4-project-smart-street-light-system-using-IR-sensor-/blob/main/BLOCK%20DIAGRAM%202.png?raw=true)


![blockdiagram](https://github.com/sandesh-ar/sem-4-project-smart-street-light-system-using-IR-sensor-/blob/main/BLOCK%20DIAGRAM%201.png?raw=true)




### 📌 Methodology
The system consists of the following functional blocks:
- **Sensor Module:** LDR, IR Sensor, Rain Sensor for input detection.
- **Control System:** Arduino Uno processes sensor data and manages lighting.
- **Lighting System:** LED-based street lights for energy-efficient illumination.
- **Power Supply:** AC/DC power with an option for solar energy.

### 📌 Hardware Components
- **Arduino Uno:** Microcontroller for processing and control.
- **LDR Sensor:** Detects daylight intensity.
- **IR Sensor:** Detects moving objects (vehicles/pedestrians).
- **Rain Sensor:** Adjusts lighting during rainfall.
- **LED Lights:** Energy-efficient illumination.

### 📌 Software Tools
- **Arduino IDE:** For writing, compiling, and uploading the control code to the Arduino board.

### 📌 Circuit Design
The circuit includes:
- LDR connected to Arduino analog pin **A0**.
- IR sensors at **A1, A2, A3, A4** for motion detection.
- Rain sensor at **A5**.
- LEDs controlled via digital output pins **2, 3, 4, 5, 6**.

### 🔢 Code Implementation
```cpp
int led = 6;
int led1 = 5;
int led2 = 4;
int led3 = 3;
int led4 = 2;

int ldr = A0;
int ir = A1;
int ir1 = A2;
int ir2 = A3;
int ir3 = A4;
int rainsensorpin = A5;

void setup() {
  Serial.begin(9600);
  pinMode(led, OUTPUT);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(ldr, INPUT);
  pinMode(ir, INPUT);
  pinMode(ir1, INPUT);
  pinMode(ir2, INPUT);
  pinMode(ir3, INPUT);
  pinMode(rainsensorpin, INPUT);
}

void loop() {
  int ldrStatus = analogRead(ldr);
  int rainValue = analogRead(rainsensorpin);

  if (analogRead(A1) < 500 && ldrStatus >= 80 || analogRead(A1) < 500 && rainValue < 500)
    digitalWrite(led, HIGH);
  else
    digitalWrite(led, LOW);
    
  delay(100);
}
```

## 📊 Results & Discussions
### ✅ Advantages
✔ **Energy Efficiency:** Reduces power wastage and electricity costs.  
✔ **Cost Savings:** Reduces maintenance expenses with automated control.  
✔ **Safety & Security:** Brighter streets reduce accidents and crime.  
✔ **Environmental Impact:** Lowers carbon emissions and light pollution.  

### 🚧 Limitations
❌ **Initial Cost:** Higher investment in sensors and controllers.  
❌ **Maintenance Complexity:** Requires regular checks for sensor accuracy.  
❌ **Sensor Dependency:** Performance depends on proper sensor functioning.  

## 🔮 Future Scope
1. **Machine Learning Integration:** Improve brightness control using AI.  
2. **Smart City Integration:** Link with traffic management for optimization.  
3. **Wireless Communication:** Implement IoT for remote monitoring.  
4. **Data Logging:** Track energy usage and optimize further.  

---

## 📜 References
1. Patel J., Thorat S., Dusane S. (2020). *Automatic Street Lighting Control Using Microcontroller & Sensors*, IJSRSET.
2. Ms. Priti S., Dhaygude S., Dhage S. (2022). *Smart Street Light Using Arduino*, IJRTI.
3. Jain K., Surana M. (2022). *Smart Street Light System Based on Arduino*, International Research Journal of Modernization in Engineering Technology and Science.

---

## 📷 Project Images
![Prototype Model](https://github.com/sandesh-ar/sem-4-project-smart-street-light-system-using-IR-sensor-/blob/main/PROJECT%20MODEL%201.jpg?raw=true)  

![Prototype Model](https://github.com/sandesh-ar/sem-4-project-smart-street-light-system-using-IR-sensor-/blob/main/PROJECT%20MODEL%202.jpg?raw=true)

---
