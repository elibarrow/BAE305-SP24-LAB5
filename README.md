# Lab Report 5 - The Brain: Microcontrollers
Eli Barrow & Isaac Stevens

Feb. 15, 2024

## Summary of Lab ##

•	A 330 Ω resistor

•	Oscilloscope: Tektronix TDS 2012

•	A Computer running Arduino IDE

•	SparkFun Inventor’s kit

- RedBoard breadboard
  
- Photoresistor
  
-	An LED (any color)
  
-	Two 10 kΩ potentiometers

-	A momentary button
  
- Resistors: 10 kΩ


### Lab Objective: Familiarize yourself with the Arduino IDE and Red Board(Arduino Uno) ###  


## Lab Assignment Specific Items ##


## Part 1 - Blinking an LED ##

 We began Part 1 of the lab by connecting the RedBoard to our computer and starting the Arduino IDE program.
 We then opened the Blink Program that was included in the Arduino IDE application.

The Blink Program code that is displayed upon opening is shown below: 

/*
  Blink

  Turns an LED on for one second, then off for one second, repeatedly.

  Most Arduinos have an on-board LED you can control. On the UNO, MEGA and ZERO
  it is attached to digital pin 13, on MKR1000 on pin 6. LED_BUILTIN is set to
  the correct LED pin independent of which board is used.
  If you want to know what pin the on-board LED is connected to on your Arduino
  model, check the Technical Specs of your board at:
  https://www.arduino.cc/en/Main/Products

  modified 8 May 2014
  by Scott Fitzgerald
  modified 2 Sep 2016
  by Arturo Guadalupi
  modified 8 Sep 2016
  by Colby Newman

  This example code is in the public domain.     

  https://www.arduino.cc/en/Tutorial/BuiltInExamples/Blink     
*/

// the setup function runs once when you press reset or power the board     
void setup() {     
  // initialize digital pin LED_BUILTIN as an output.     
  pinMode(LED_BUILTIN, OUTPUT);      
}

// the loop function runs over and over again forever    
void loop() {    
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)    
  delay(1000);                      // wait for a second     
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW   
  delay(1000);                      // wait for a second   
}

After having this code in the Arduino IDE program, we ran it while it was connected to the RedBoard to answer the following questions.    
1. **What does the program do?**    
The blink program causes the TX (green light/serial communication) to flash every few seconds while the 13 (blue light) remains on and then turns off over and over. When an LED is connected, the LED turns on for a second and then turns off.     

2. **What are the major sections of the computer program and what does each section do?**        
The major sections of the computer program are initialization, void setup (), and void loop (). The initialization sets all the values for the program, void setup () checks the communication between the Arduino and the computer and initializes pins in the circuit, and void loop () loops the code and causes the blinking.


We then connected a 330 &Omega; resistor and an LED in series to pin 13 on our RedBoard. The circuit that we built in class is shown below.

 <p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3455.JPG width = 50%> 
</p>


***Discussion Questions:***    
Your LED flashes with a delay from the uploaded code. Decrease this delay until the LED just stops blinking. That is, the point where the light is still blinking, but appears to stay constantly illuminated. 

1. **What is the value of your delay now?**      
   The Value of the delay now is 0.05. Persistence of vision has a maximum frequency or speed in which you will not be able to detect the change in light.      

2. **What field may this “persistence of vision” play a greater role in?**              
The field of designing electrical structures including lights or sensors will have “persistence of vision” play a greater role in them. 

3. Discuss this further in your lab report.  
    $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$

   
## Part 2 - Controlling an LED with a potentiometer ##   

To begin part 2 of this lab we started by opening the given sample program, "Analog Read Serial", and ran it on our Adruino.    
The code from that program is given below.    
      
/*
  AnalogReadSerial

  Reads an analog input on pin 0, prints the result to the Serial Monitor.
  Graphical representation is available using Serial Plotter (Tools > Serial Plotter menu).
  Attach the center pin of a potentiometer to pin A0, and the outside pins to +5V and ground.   

  This example code is in the public domain.    

  https://www.arduino.cc/en/Tutorial/BuiltInExamples/AnalogReadSerial    
*/

// the setup routine runs once when you press reset:    
void setup() {    
  // initialize serial communication at 9600 bits per second:     
  Serial.begin(9600);     
}

// the loop routine runs over and over again forever:     
void loop() {     
  // read the input on analog pin 0:     
  int sensorValue = analogRead(A0);    
  // print out the value you read:    
  Serial.println(sensorValue);    
  delay(1);  // delay in between reads for stability    
}

After this we then connected our potentiometer to power with the variable resistance pin connected to A0. This connection schematic is shown below. 

 <p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/circuit.png>
</p>

We then were sure that the program was able to run and then verified the Baud rate to be 9600 bpm.  
After this step we combined the two previous steps to control the brightness of the LED with the potentiometer.   
A photo of the circuit that we built is shown below. 

<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3456.JPG width=50%>
</p>  
The code that was used for that circuit is shown below:     
$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$  


***Discussion Questions:***    
1.**What is the difference between an analog and a digital signal?**         
Digital signals are non-continuous electronic signals while analog signals are continuous electronic signals. 

2. **In your lab report, list a few examples of real-world examples which can be described by an analog signal. Likewise, what are the two states which can be conveyed by a digital signal?**
A few real-world examples of analog signals are temperature sensor that output a voltage that is equal to the temperature, pressure sensors that output the voltage or current level that corresponds to the measured pressure and light intensity sensors that the strength of the output signal corresponds to the intensity. They two possible states for analog signals is either Low State, which equals 0, or the High State, which equals 1. 
               
3. **What happens to the Serial Monitor Refresh rate as you move the potentiometer to control the LED blinking time?**     
The Serial Monitor Refresh rate only takes measurements when the light blinks and as you increase the resistance in the potentiometer, the rate of measurements slows down as well. 


## Part 3 - Controlling an LED with a photoresistor ##    
For this part of the lab we used the program from part 2 and replaced the potentiometer with a photoresistor in series with a 10k&Omega; resistor. We then connected the pin to the photoresistor and ground to the resistor. The analog input was connected to the node between the photoresistor and the resistor. The photo of that circuit is shown below.

<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3457.JPG width=50%>
</p>  


We then tried different objects to block the light of the photoresistor. This allowed us to answer the question of what the min. and max. analog values we were able to detect with this circuit. We found the min. to be 1 and the max. to be 1004.


We then used an if/else statement to turn on the LED light only when the brightness sensed by the photoresistor was low, similar to a night light. The code written for this step is shown below.    
    
if(sensorValue > 400){ digitalWrite(LED_BUILTIN, HIGH);     
//run if true     
           }     
           else{ digitalWrite(LED_BUILTIN, LOW);    
    //run if false    
       }        

    
***Discussion Questions:***    
1. Does the LED turn on immediately after blocking the light? What about when you remove the object blocking the light, does the LED turns of immediately?     
The LED turns on immediately after blocking the light. The LED also turns off immediately after removing the object blocks the light.     

2. Replace the 10k resistor with another LED (negative leg to ground).  What happens when you place your finger over the photoresistor?     
When you place your finger over the photoresistor, the new LED dims while the old LED remains lit.     

3. How does this help you visualize Ohm’s Law?      
Could not get this functioning in class and was told to drop it.        


## Part 4 - LED dimmer using PWM ## 
We used the same circuit was that in part 2 with the potentiometer, expcept the LED pin was switched to one that was PWM capable.
We then read the voltage from the potentiometer and mapped the voltage (0 to 1023) to a value from 0 to 255 using the function map(value, fromLow, fromHigh, toLow, toHigh). We wrote the map value to the LED pin using the function analogWrite(pin,value).


***Discussion Questions:***      
1. Connect the oscilloscope to the LED pin and observe and record what happens to the signal and the LED brightness when you turn the knob of the potentiometer.        
 
Pulse Width Modulation. When you increase the resistance in the potentiometer, the LED shines brighter and vice versa. When you increase the resistance in the potentiometer, the signal width increases with it until it is a line at the top of the page and if you decrease in the potentiometer, the width decreases until it is a line at the bottom of the page 








## Conclusion of Lab 4 ##

