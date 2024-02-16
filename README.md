# Lab Report 5 - The Brain: Microcontrollers
Eli Barrow & Isaac Stevens

Feb. 15, 2024

## Summary of Lab ##

There were multiple goals for this lab, with the main purpose being to learn how to run code through a breadboard using Arduino IDE. To understand this we created four different circuits involving LEDs and resistors and ran code through the breadboard to learn how the code behaved when it interacted with the circuit. The first circuit contained an LED that was blinking due to code and the second circuit involved controlling an LED through a potentiometer and setting the blinking time to the value read from the potentiometer. The third circuit contained an LED with a photoresistor and by implementing code, as the photoresistor detected a lower brightness, the LED would turn on. Lastly, the fourth circuit involved using the same circuit as the second circuit connected to the oscilloscope and observing the pulse width modulation and how it was affected by changes in resistance caused by the potentiometer. By completing this lab, some secondary goals were also achieved with us learning about the persistence of vision and how it affects light and sensors, learning the difference between analog and digital signals, understanding the purpose of a photoresistor, and becoming familiar with pulse width modulation (PWM) and how it is affected by changes in resistance.

### Lab Objective: Familiarize yourself with the Arduino IDE and Red Board (Arduino Uno) ###  


## Lab Assignment Specific Items ##

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


## Methods and Testing ##

## Part 1 - Blinking an LED ##



 We began Part 1 of the lab by creating the circuit and connecting the RedBoard to our computer.
 
 We then opened the Arduino IDE program and downloaded the Blink Program included in the Arduino IDE application by going to files>examples>basic>blink.

The Blink Program code that is displayed upon opening is shown below: 

<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Screenshot%202024-02-15%20at%203.43.09%20PM.png width = 50%> 
</p>  

**Code Display 1: Blink Code**    
  This example code is in the public domain.     

  https://www.arduino.cc/en/Tutorial/BuiltInExamples/Blink     

The following schematic was given to show how to build the circuit.

Figure 1: Schematic of Blinking LED Circuit
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Schematic%201.png width = 50%> 
</p>

We then connected a 330 &Omega; resistor and an LED in series to pin 13 on our RedBoard. The circuit that we built in class is shown below.

Image 1: Our Blinking LED circuit

 <p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3455.JPG width = 50%> 
</p>

<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Blinking%20LED%20Circuit.jpeg width=50%>
</p>    


After having this code in the Arduino IDE program and the circuit built, we ran it while the computer was connected to the RedBoard to find the results.
   
## Part 2 - Controlling an LED with a potentiometer ##   

To begin part 2 of this lab we started by creating the circuit and connecting the Redboard to our computer.

We then connected our potentiometer to power with the variable resistance pin connected to A0. This connection schematic is shown below. 

Figure 2: Schematic of LED circuit with Potentiometer
 <p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/circuit.png>
</p>


After building the circuit, we opened the given sample program, "Analog Read Serial", and ran it on our Arduino. The code from that program is given below.    
      
 <p align="center">
  <img src=  https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Screenshot%202024-02-15%20at%204.17.02%20PM.png width = 50%>
</p>

**Code Display 2: Analog Read Serial**    
This example code is in the public domain.  
  https://www.arduino.cc/en/Tutorial/BuiltInExamples/AnalogReadSerial


We then were sure that the program could run and verified the Baud rate to be 9600 bpm.  
After this step, we combined the two previous steps to control the brightness of the LED with the potentiometer.   
A photo of the circuit that we built is shown below. 

Image 2: Our LED circuit with Potentiometer 
<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3456.JPG width=50%>
</p>

The code to control the LED brightness with the potentiometer is shown below.
<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Screenshot%202024-02-15%20at%203.54.37%20PM.png width = 50%>
</p>

**Code Display 3: Potentiometer & LED Brightness**    
Part of this example code is in the public domain.  
  https://www.arduino.cc/en/Tutorial/BuiltInExamples/AnalogReadSerial

## Part 3 - Controlling an LED with a photoresistor ##    

For this part of the lab, we used the program from part 2 and replaced the potentiometer with a photoresistor in series with a 10k&Omega; resistor. We then connected the pin to the photoresistor and ground to the resistor. The analog input was connected to the node between the photoresistor and the resistor. The photo of that circuit is shown below.




Image 3: Our LED circuit with Photoresistor
<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3457.JPG width=50%>
</p>  

After building the circuit, we then used an if/else statement to turn on the LED light only when the brightness sensed by the photoresistor was low, similar to a night light. The code written for this step is shown below. 

<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Screenshot%202024-02-15%20at%203.56.35%20PM.png width=50%>
</p>  

**Code Display 4: Nightlight Code**    


We then tried different objects to block the light of the photoresistor. This allowed us to answer the question of what the min. and max. analog values we were able to detect with this circuit. We found the min. to be 1 and the max. to be 1004.  

## Part 4 - LED dimmer using PWM ## 
We used the same circuit as that in part 2 with the potentiometer, except the LED pin was switched to one that was PWM capable. Below is a photo of the circuit as well as the setup with the Oscilloscope.

Image 4: Our LED circuit with Potentiometer
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/LED%20Potentiometer%20Circuit.jpg width=50%>
</p>

Image 5: Setup of our LED circuit with Potentiometer
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/LED%20Potentiometer%20Measurement.jpg width=75%>
</p>

We then read the voltage from the potentiometer and mapped the voltage (0 to 1023) to a value from 0 to 255 using the function map(value, fromLow, fromHigh, toLow, toHigh). We wrote the map value to the LED pin using the function analogWrite(pin,value). The code for this part is shown below.

<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Screenshot%202024-02-15%20at%204.00.49%20PM.png width=75%>
</p>

**Code Display 5: Mapping**   


## Results ##

**Part 1**

Created the Blinking LED circuit and learned how to run code through Arduino IDE to the breadboard. We also learned what the blinking LED circuit did and how delay could be changed to affect the code.

**We were able to answer the following questions after completing part 1**    
**What does the program do?**

The blink program causes the TX (green light/serial communication) to flash every few seconds while the 13 (blue light) remains on and then turns off over and over. When an LED is connected, the LED turns on for a second and then turns off.     

**What are the major sections of the computer program and what does each section do?****
        
The major sections of the computer program are initialization, void setup (), and void loop (). The initialization sets all the values for the program, void setup () checks the communication between the Arduino and the computer and initializes pins in the circuit, and void loop () loops the code and causes the blinking.

Image 1: Our Blinking LED circuit
 <p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3455.JPG width = 50%> 
</p>

<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Blinking%20LED%20Circuit.jpeg width=50%>
</p>  

**Part 2**

Created the LED circuit with a Potentiometer and found the Baud Rate at 9600bpm as well as set the blinking time to value read from the potentiometer.

Image 2: Our LED circuit with Potentiometer 
<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3456.JPG width=50%>
</p>

**Part 3**

Created the LED circuit with a Photoresistor and we found the min. to be 1 and the max. to be 1004 that you could detect with the circuit. We also created a code that would only turn on the LED when the brightness detected by the photoresistor is low.

Image 3: Our LED circuit with Photoresistor
<p align="center">
  <img src= https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/IMG_3457.JPG width=50%>
</p>  

**Part 4**

Created the LED circuit with a Potentiometer from Part 2. Using the oscilloscope, we were able to observe the pulse width modulation (PWM) and understand how it was affected by a change in resistance from the potentiometer.

Image 4: Our LED circuit with Potentiometer
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/LED%20Potentiometer%20Circuit.jpg width=50%>
</p>

Image 5: Setup of our LED circuit with Potentiometer
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/LED%20Potentiometer%20Measurement.jpg width=75%>
</p>

Image 6: PWM with low resistance
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Min%20R%20in%20Potentiometer.jpg width=75%>
</p>

Image 7: PWM with medium resistance
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Normal%20R%20in%20Potentiometer.jpg width=75%>
</p>

Image 8: PWM with high resistance
<p align="center">
  <img src=https://github.com/elibarrow/BAE305-SP24-LAB5/blob/main/Max%20R%20in%20Potentiometer.jpg width=75%>
</p>


## Discussion Questions ##

**Part 1**

Your LED flashes with a delay from the uploaded code. Decrease this delay until the LED just stops blinking. That is, the point where the light is still blinking, but appears to stay constantly illuminated. 

**1. What is the value of your delay now?**      
The Value of the delay now is 0.05. The persistence of vision has a maximum frequency or speed at which you will not be able to detect the change in light.      

**2. What field may this “persistence of vision” play a greater role in?**              
The field of designing electrical structures including lights or sensors will have “persistence of vision” play a greater role in them. 
This can be used to your advantage when designing structures because the human retina obtains the image seen in our vision for 1/16th of a second after it has already passed, when designing a lighting system you can only have the object blink 16+ times a second and the user would never be able to tell the differnece than if it was constantly on. This could be used in many different scenarios to save energy by pulsating light rather than constantly leaving it on.     


    

**Part 2**

**1. What is the difference between an analog and a digital signal?**         
Digital signals are non-continuous electronic signals while analog signals are continuous electronic signals. 

**2. In your lab report, list a few examples of real-world examples which can be described by an analog signal. Likewise, what are the two states which can be conveyed by a digital signal?**
A few real-world examples of analog signals are temperature sensors that output a voltage that is equal to the temperature, pressure sensors that output the voltage or current level that corresponds to the measured pressure, and light intensity sensors that the strength of the output signal corresponds to the intensity. The two possible states for analog signals are either the Low State, which equals 0, or the High State, which equals 1. 
               
**3. What happens to the Serial Monitor Refresh rate as you move the potentiometer to control the LED blinking time?**     
The Serial Monitor Refresh rate only takes measurements when the light blinks and as you increase the resistance in the potentiometer, the rate of measurements slows down as well.


**Part 3**

**1. Does the LED turn on immediately after blocking the light? What about when you remove the object blocking the light, does the LED turn off immediately?**    
The LED turns on immediately after blocking the light. The LED also turns off immediately after removing the object blocks the light.     

**2. Replace the 10k resistor with another LED (negative leg to ground).  What happens when you place your finger over the photoresistor?**     
When you place your finger over the photoresistor, the new LED dims while the old LED remains lit.     

**3. How does this help you visualize Ohm’s Law?**      
Could not get this functioning in class and was told to drop it.


**Part 4**
   
**1. Connect the oscilloscope to the LED pin and observe and record what happens to the signal and the LED brightness when you turn the knob of the potentiometer.**        
 
Pulse Width Modulation. When you increase the resistance in the potentiometer, the LED shines brighter and vice versa. When you increase the resistance in the potentiometer, the signal width increases with it until it is a line at the top of the page and if you decrease in the potentiometer, the width decreases until it is a line at the bottom of the page 




## Conclusion of Lab 4 ##

As stated in the summary of the lab, we created four circuits in Lab 4. The first circuit contained an LED that was blinking due to code and the second circuit involved controlling an LED through a potentiometer and setting the blinking time to the value read from the potentiometer. The third circuit contained an LED with a photoresistor and by implementing code, as the photoresistor detected a lower brightness, the LED would turn on. Lastly, the fourth circuit involved using the same circuit as the second circuit connected to the oscilloscope and observing the pulse width modulation and how it was affected by changes in resistance caused by the potentiometer. For the conclusions reached for the lab, from the first circuit we learned that the human eye has a frequency (Over 100 Hz) in which the eye cannot see flickering in lights. This effect is called the persistence of vision and is important in the field of designing electrical structures due to the use of sensors and lights. For the second circuit, we verified the Baud Rate and learned the difference between analog and digital signals. By changing the resistance in the potentiometer, the Serial Monitor Refresh would only take measurements when the LED blinks. As you increase the resistance in the potentiometer, the LED blinks less, and therefore measurements are taken less often by Arduino IDE.

For the third circuit, the photoresistor would detect brightness and by using a code, we were able to turn the LED into a night light with it only turning on in the dark. This is due to the behavior of the photoresistor being as it is exposed to more light the resistance goes down, turning off the LED. We were able to effectively demonstrate this in the lab and properly implement the code. For the fourth circuit, using the oscilloscope, we were able to graph the pulse width modulation (PWM) of the LED. As the resistance in the potentiometer was increased, the PWM increased, and the LED became brighter due to increased voltage, and vice versa when the resistance of the potentiometer was decreased. By displaying this on the oscilloscope, we were able to create a better understanding of PWM and the effects resistance has on voltage and therefore the PWM signal. Lab 5 as a whole created a better understanding of how to create and run code through a breadboard in Arduino IDE as well as effectively demonstrated concepts such as the persistence of vision, the difference between digital and analog signals, the purpose of photoresistors, and PWM.
