Alexander Martin
Feb. 9th, 2015
NUsolar


This is an implementation of Nemith's SerialLCD library for the SparkFun Serial LCD's which uses HardwareSerial ports instead of SoftwareSerial--Since this is not implemented on the Arduino Due. The only difference is that you must specify the serial port to use at declaration:

serLCD lcd(Serial1);

and must call

LCDobject.begin();

within setup();