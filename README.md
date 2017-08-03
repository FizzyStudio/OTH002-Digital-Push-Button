# OTH002 Digital Push Button

###### Translation

> For `English`, please click [`here.`](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/README.md)

> For `Chinese`, please click [`here.`](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/README_cn.md)

![](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/pic/OTH002.JPG "OTH002") 

### Introduction

> This is a big button which gives the first touch of the physical world. Simply plug to IO expansion board to finish your first taste of Arduino. 

### Specification

* Supply Voltage: 3.3V to 5V
* Indicator LED on board
* Easy to 'plug and play'
* Large button keypad and high-quality first-class hat
* Able to achieve very interesting and an interactive work
* Interface: Digital
* Size:22x30mm

### Connection Diagram

![](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/pic/OTH002_Diagram.png "Connection") 

### Sample Code

    /*
      # Description:
      # When you push the digital button, the Led 13 on the board will turn on. Otherwise,the led turns off.
    */
    int ledPin = 13;                // choose the pin for the LED
    int inputPin = 2;               // Connect sensor to input pin 3 
    
    
    void setup() {
      pinMode(ledPin, OUTPUT);      // declare LED as output
      pinMode(inputPin, INPUT);     // declare pushbutton as input
    }
    
    void loop(){
      int val = digitalRead(inputPin);  // read input value
      if (val == HIGH) {            // check if the input is HIGH
        digitalWrite(ledPin, LOW);  // turn LED OFF
      } else {
        dig**italWrite(ledPin, HIGH); // turn LED ON
      }
    }

### More

