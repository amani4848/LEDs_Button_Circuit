# Tinkercad LED Control Circuit using Pushbuttons and Arduino
**About the Project**

This is a simple electronics project created as part of a training task in the electronics path.  
The circuit contains:
- 3 pushbuttons
- 3 LEDs (red, green, blue)
- 3 resistors (220Ω)
- 3 resistors (10kΩ)
- Arduino

Each button controls a specific LED. When the button is pressed, the corresponding LED lights up.The LED turns off as soon as the button is released.

**Components Used**
- 3 LEDs (Red, Green, Blue)  
- 3 Pushbuttons  
- 3 Resistors (220Ω)  
- 3 Resistors (10kΩ for pull-down)
- Arduino
- Breadboard  
- jumper wires  

**How It Works**
- Each pushbutton is connected to a digital input pin on the Arduino.
- A pull-down resistor ensures a LOW signal when the button is not pressed.
- When the button is pressed, the signal becomes HIGH and lights up the corresponding LED.
- The LED stays on while the button is pressed and turns off when released.

**Arduino Code**
```cpp
//
int btn = 0;
int btn1 = 0;
int btn2 = 0;

void setup()
{
  pinMode(4, INPUT); 
  pinMode(12, OUTPUT); 
  pinMode(3, INPUT); 
  pinMode(11, OUTPUT);
  pinMode(2, INPUT); 
  pinMode(10, OUTPUT); 
}

void loop()
{
  btn = digitalRead(4);
  if (btn == HIGH) {
    digitalWrite(12, HIGH);
  } else {
    digitalWrite(12, LOW);
  }

  btn1 = digitalRead(3);
  if (btn1 == HIGH) {
    digitalWrite(11, HIGH);
  } else {
    digitalWrite(11, LOW);
  }

  btn2 = digitalRead(2);
  if (btn2 == HIGH) {
    digitalWrite(10, HIGH);
  } else {
    digitalWrite(10, LOW);
  }

  delay(100);
}

```
![Circuit](https://github.com/amani4848/LEDs_Button_Circuit/blob/3c5ec393a61dda7ac56b3f682c09ce1b0806ecb1/LED_BUTTON.png)
