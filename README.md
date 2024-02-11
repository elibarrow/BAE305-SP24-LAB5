# Lab Report 5 - The Brain: Microcontrollers
Eli Barrow & Isaac Stevens

Feb. 15, 2024

## Summary of Lab ##



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

kjkljklajdsf;;;;;;;;;flpvb***********************************

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

 




## Conclusion of Lab 4 ##

