# Experiment--07-Design-and-control-of-Mobile-robot-motion-
 

### AIM: 
To Design a wheel base for mobile robot and control the motion using forward and reverse motion 
 
### COMPONENTS REQUIRED:
1.	 Patch cables 
2.	L293D motor shield 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	Wheels
7.	DC motor 


### THEORY: 
We can control the speed of the DC motor by simply controlling the input voltage to the motor and the most common method of doing that is by using PWM signal.


DC Motor Speed Control Input Voltage
PWM DC Motor Control
PWM, or pulse width modulation is a technique which allows us to adjust the average value of the voltage that’s going to the electronic device by turning on and off the power at a fast rate. The average voltage depends on the duty cycle, or the amount of time the signal is ON versus the amount of time the signal is OFF in a single period of time.
 

PWM Working Principle - Pulse Width Modulation How It Works
 
 

![image](https://user-images.githubusercontent.com/36288975/174224618-c8d83fea-4456-4706-9974-c8c7641a27e5.png)



![image](https://user-images.githubusercontent.com/36288975/174224728-daf998f2-8ca4-44b8-828d-a3229688cf1e.png)


### PROCEDURE:
1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select the board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device 
10.	Plot the graph for the output voltage vs the resistance 


### PROGRAM 
 
 ```
 const int button1 = 4; 
const int button2 = 5; 
int buttonstate1 = 0;
int buttonstate2 = 0;
void setup()

{
   
pinMode(2,OUTPUT); 
pinMode(3,OUTPUT); 
pinMode(8,OUTPUT);
pinMode(9,OUTPUT); 
pinMode(button1,INPUT);
pinMode(button2,INPUT); 

}

void loop()
{
    buttonstate1 = digitalRead(button1);
        buttonstate2 = digitalRead(button2);



  if (buttonstate1 == HIGH){

    digitalWrite(8,HIGH);
        digitalWrite(9,LOW);
    delay(5000);
  }

    else {

          digitalWrite(8,LOW);
              digitalWrite(9,HIGH);
      
    }
if (buttonstate2 == HIGH){

    digitalWrite(2,HIGH);
        digitalWrite(3,LOW);
  delay(5000);
}

    else {

          digitalWrite(2,LOW);
              digitalWrite(3,HIGH);
      
    }

}
```
### OUTPUT :
![O](./1.png)
 
 
 
 
 

### RESULTS : 
Arduino uno is interfaced with FSR and output values are indicated on a graph.
