# HC-SR04 Ultrasonic Sensor Distance Measurement (Arduino)

## 📘 Project Description
This project measures distance using the **HC-SR04 ultrasonic sensor** and displays the result through the Arduino Serial Monitor.  
This is one of my early Arduino learning projects where I practiced sensor interfacing and Arduino programming.

---

## 🛠 Components Used
- Arduino UNO  
- HC-SR04 Ultrasonic Sensor  
- Jumper Wires  

---

## 🔌 Circuit Connections
| HC-SR04 Pin | Arduino Pin |
|-------------|-------------|
| VCC         | Vin         |
| GND         | GND         |
| TRIG        | D7          |
| ECHO        | D6          |

---

## 💻 Code
int trig=7;
int echo=6;
int timeInMicro;
int distanceInCm;
void setup() {
  Serial.begin(9600);
  pinMode(7,OUTPUT);
  pinMode(6,INPUT);
}
void loop() {
  digitalWrite(trig,LOW);
  delayMicroseconds(2);
  digitalWrite(trig,HIGH);
  delayMicroseconds(10);
  digitalWrite(trig,LOW);
  timeInMicro=pulseIn(echo,HIGH);
  distanceInCm=timeInMicro /29 /2;
  Serial.println(distanceInCm);
  delay(100);
}
## 📷 Circuit Diagram  
(Uploaded in the folder) [ the image is by Tinkercad ]

---

## 🎯 What I Learned
- How ultrasonic sensors work  
- Measuring distance using sound waves  
- Using `pulseIn()`  
- Converting time to distance  
- Basic hardware interfacing  

---

## 🚀 Future Improvements
- Add LCD to show distance  
- Add buzzer alarm for short distance  
- Make a full obstacle-avoiding robot  

---

## 👤 Author
**MD. Hamidur Rhaman Bhuyan**  
EEE Student | AUST Robotics Club  
```
