<h1>Automated Projector Cabinet Control System</h1><br/>
An automation system using an Arduino controller to manage the opening and closing of a cabinet containing a video projector. The system controls the cabinet doors, the shelf holding the projector and legs which holding the shelf after sliding out of the cabinet. All of this are powered by linear actuators. Key features of the project include:
<ul>
<li><b>Remote control:</b> Users can open or close the cabinet doors and extend or retract the shelf using a remote control.</li>
<li><b>Manual control:</b> Physical buttons on the cabinet allow for local control of the system.</li>
<li><b>Home automation integration:</b> The system is integrated with the Home Assistant app, enabling control via mobile devices, allowing the user to manage the cabinet and shelf through the app.</li>
<li><b>Smart system:</b> The Arduino controller manages the actuators, ensuring smooth and precise operation of both the shelf and cabinet doors, enhancing the convenience of using the video projector.</li>
</ul><br/>

<h1>Circuit Documentation</h1><br/>
<h2>Summary</h2>
This circuit is designed to interface an Arduino Mega 2560 with various components including a DS3231 Real-Time Clock (RTC), an IR Receiver, a 5V 8-Channel Relay module, pushbuttons, linear actuators, and power sources. The Arduino Mega 2560 serves as the central processing unit, controlling the relays which in turn drive the linear actuators. The DS3231 RTC provides timekeeping functionality, while the IR Receiver allows for remote control capabilities. Pushbuttons are used for manual input, and the circuit is powered by 12V batteries.<br/>
<h2>Component List</h2>
<h3>Arduino Mega 2560</h3>
    • Microcontroller board based on the ATmega2560<br/>
    • It has 54 digital input/output pins (of which 15 can be used as PWM outputs), 16 analog inputs, 4 UARTs (hardware serial ports), a 16 MHz crystal oscillator, a USB connection, a power jack, an ICSP header, and a reset button.<br/>
<h3>DS3231 RTC</h3>
    • A precise real-time clock module with an integrated temperature-compensated crystal oscillator (TCXO) and crystal.<br/>
    • It communicates with the Arduino via I2C.<br/>
<h3>IR Receiver</h3>
    • An infrared receiver that can decode IR signals from a remote control.<br/>
    • It is connected to one of the digital pins of the Arduino.<br/>
<h3>5V 8-Channel Relay</h3>
    • A relay module with 8 channels that can be controlled independently.<br/>
    • Each relay can be used to switch higher voltage loads.<br/>
<h3>Pushbuttons</h3>
    • Simple push-to-make buttons for user input.<br/>
    • They are connected to the digital pins of the Arduino.<br/>
<h3>Linear Actuators</h3>
    • Devices that convert electrical energy into linear motion.<br/>
    • They are controlled by the relays and are powered by the 12V batteries.<br/>
<h3>12V Batteries</h3>
    • Provide the power source for the linear actuators and the relay module.<br/>
<h3>2.1mm DC Barrel Jack</h3>
    • A power connector that allows the 12V battery to connect to the circuit.<br/>

<h2>Wiring Details</h2>
<h3>Arduino Mega 2560</h3>
    • GND connected to the ground of DS3231 RTC, IR Receiver, and both pushbuttons.<br/>
    • 5V supplies power to the 5V 8-Channel Relay, DS3231 RTC, IR Receiver, and both pushbuttons.<br/>
    • D2 PWM to IN1 on the 5V 8-Channel Relay.<br/>
    • D3 PWM to IN2 on the 5V 8-Channel Relay.<br/>
    • D7 PWM to IN3 on the 5V 8-Channel Relay.<br/>
    • D8 PWM to IN4 on the 5V 8-Channel Relay.<br/>
    • D4 PWM to IN5 on the 5V 8-Channel Relay.<br/>
    • D5 PWM to IN6 on the 5V 8-Channel Relay.<br/>
    • D10 PWM to IN7 on the 5V 8-Channel Relay.<br/>
    • D11 PWM to IN8 on the 5V 8-Channel Relay.<br/>
    • D21/SCL to SCL on DS3231 RTC.<br/>
    • D20/SDA to SDA on DS3231 RTC.<br/>
    • D12 PWM to DATA on IR Receiver.<br/>
    • D9 PWM to Pin 3 on the first pushbutton.<br/>
    • D6 PWM to Pin 3 on the second pushbutton.<br/>
<h3>DS3231 RTC</h3>
    • GND to ground.<br/>
    • VCC to 5V from Arduino.<br/>
    • SCL to D21/SCL on Arduino.<br/>
    • SDA to D20/SDA on Arduino.<br/>
<h3>IR Receiver</h3>
    • DATA to D12 PWM on Arduino.<br/>
    • VCC to 5V from Arduino.<br/>
    • GND to ground.<br/>
<h3>5V 8-Channel Relay</h3>
    • VCC to 5V from Arduino.<br/>
    • GND to ground.<br/>
    • IN1 to D2 PWM on Arduino.<br/>
    • IN2 to D3 PWM on Arduino.<br/>
    • IN3 to D7 PWM on Arduino.<br/>
    • IN4 to D8 PWM on Arduino.<br/>
    • IN5 to D4 PWM on Arduino.<br/>
    • IN6 to D5 PWM on Arduino.<br/>
    • IN7 to D10 PWM on Arduino.<br/>
    • IN8 to D11 PWM on Arduino.<br/>
    • NC (Normally Closed) pins are not connected.<br/>
    • NO (Normally Open) pins are connected to the positive side of the 12V battery.<br/>
    • C (Common) pins are connected to the positive or negative side of the linear actuators, depending on the desired direction of motion.<br/>
<h3>Pushbuttons</h3>
    • One side connected to 5V from Arduino.<br/>
    • The other side connected to D9 PWM and D6 PWM on Arduino respectively.<br/>
    • Ground connected to the ground.<br/>
<h3>Linear Actuators</h3>
    • Positive and negative pins connected to the C and NO pins of the 5V 8-Channel Relay respectively.<br/>
<h3>12V Batteries</h3>
    • One battery's positive terminal connected to the center pin of the 2.1mm DC Barrel Jack and NO on the 5V 8-Channel Relay.<br/>
    • The negative terminal connected to the sleeve pin of the 2.1mm DC Barrel Jack and NC on the 5V 8-Channel Relay.<br/>
<h3>2.1mm DC Barrel Jack</h3>
    • center connected to the positive terminal of the 5V battery.<br/>
    • sleeve connected to the negative terminal of the 5V battery.<br/>

<h2>Watch video</h2>

[![Video Title](https://img.youtube.com/vi/lF0zBU_XDEI/mq1.jpg?)](https://youtu.be/lF0zBU_XDEI)


<h2>Circuit:</h2>

![Picture of schema](circuit.png)
