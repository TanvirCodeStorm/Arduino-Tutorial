💡 Arduino UNO — Blink External LED

<p align="center">
  <strong>Our First Arduino Program</strong>
</p>---

🎯 Objective

In this project, we will make an external LED connected to an Arduino UNO blink repeatedly using a 220 Ω resistor.

This is one of the simplest Arduino projects and is commonly used to verify that the board, IDE, program, and external circuit are working correctly.

---

🧰 Requirements

- 🔵 Arduino UNO
- 🔴 External LED
- 🟦 220 Ω resistor
- 🔌 Breadboard and jumper wires
- 🔌 USB Type-A to Type-B cable
- 💻 Computer
- 🖥️ Arduino IDE

«💡 The 220 Ω resistor limits the current flowing through the LED and helps protect both the LED and the Arduino pin.»

---

🔌 Connection

Connect the components as follows:

Arduino UNO Pin 8 ── 220 Ω Resistor ── LED Anode (+)
LED Cathode (-) ─────────────────────── GND

The longer leg of the LED is usually the anode (+), and the shorter leg is usually the cathode (-).

«⚠️ Always connect the LED in series with the 220 Ω resistor. Do not connect an LED directly to an Arduino output pin.»

---

💻 Arduino Blink Code

// Arduino UNO External LED Blink

void setup() {
  // Configure digital pin 8 as an output
  pinMode(8, OUTPUT);
}

void loop() {
  // Turn the LED ON
  digitalWrite(8, HIGH);

  // Wait for 1 second
  delay(1000);

  // Turn the LED OFF
  digitalWrite(8, LOW);

  // Wait for 1 second
  delay(1000);
}

---

🧠 Code Explanation

1️⃣ "void setup()"

void setup() {

The "setup()" function runs once when the Arduino starts or resets.

We configure digital pin 8 as an output:

pinMode(8, OUTPUT);

This tells the Arduino that pin 8 will be used to control the external LED.

---

2️⃣ "void loop()"

void loop() {

The "loop()" function runs repeatedly while the Arduino is powered.

This allows the external LED to continuously turn ON and OFF.

---

3️⃣ Turn the LED ON

digitalWrite(8, HIGH);

"digitalWrite()" sets the specified digital output to "HIGH".

Here, "HIGH" makes the Arduino output pin active and current flows through the resistor and LED.

---

4️⃣ Wait for 1 Second

delay(1000);

The "delay()" function pauses the program for 1000 milliseconds.

1000 ms = 1 second

Therefore, the LED remains ON for approximately 1 second.

---

5️⃣ Turn the LED OFF

digitalWrite(8, LOW);

Setting pin 8 to "LOW" stops the normal current path through the LED and turns it OFF.

---

6️⃣ Wait Again

delay(1000);

The Arduino waits for another 1 second before returning to the beginning of "loop()".

---

🔄 How the Program Works

The Arduino repeatedly performs these steps:

       ┌─────────────────────┐
       │      LED ON          │
       └─────────┬───────────┘
                 ↓
          Wait 1 second
                 ↓
       ┌─────────────────────┐
       │      LED OFF         │
       └─────────┬───────────┘
                 ↓
          Wait 1 second
                 ↓
          Repeat forever
                 │
                 └───────────────↺

---

📋 Program Flow

Step| Command| Action
1| "pinMode(8, OUTPUT)"| Configures pin 8 as an output
2| "digitalWrite(8, HIGH)"| Turns the external LED ON
3| "delay(1000)"| Waits 1 second
4| "digitalWrite(8, LOW)"| Turns the external LED OFF
5| "delay(1000)"| Waits 1 second
6| "loop()"| Starts the sequence again

---

⚙️ Changing the Blink Speed

You can change the value inside "delay()" to change the blinking speed.

⚡ Faster Blink

delay(200);

The Arduino waits only 200 milliseconds.

🐢 Slower Blink

delay(2000);

The Arduino waits 2 seconds.

For example:

void loop() {
  digitalWrite(8, HIGH);
  delay(2000);

  digitalWrite(8, LOW);
  delay(2000);
}

---

🏆 What You Learned

After completing this project, you should understand:

- ✅ "setup()"
- ✅ "loop()"
- ✅ "pinMode()"
- ✅ "digitalWrite()"
- ✅ "delay()"
- ✅ "HIGH" and "LOW"
- ✅ How to connect an external LED with a 220 Ω resistor
- ✅ How an Arduino program repeatedly executes instructions
- ✅ How to control an Arduino pin without creating a user-defined variable

---

<p align="center">🚀 <strong>Congratulations!</strong></p><p align="center">
You have written your first Arduino program using an external LED. 🎉
</p><p align="center">
  <em>Next: Let's control more external components and learn about digital outputs!</em>
</p>