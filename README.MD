Alexander Martin
March 30th, 2015
NUsolar


This is an implementation of Nemith's SerialLCD library for the SparkFun Serial LCD's which uses HardwareSerial ports instead of SoftwareSerial--Since this is not implemented on the Arduino Due. The only difference is that you must specify the serial port to use at declaration:

	serLCD lcd(Serial1);

and must call

	lcd.begin();

within setup();

The serLCD works with all standard print(), println(), write(), etc. that are built into the Arduino Print class. There are also several extended functions for special operations such as clearing the screen, moving the cursor to a new position, disabling the display, etc. The header file contains a list of all library functions.

------------------------
Buffered LCD
------------------------
This library also includes a buffered version of the serLCD class, called serLCD_buffered. Initialization is the same as with serLCD. Text that is printed with print(), write(), etc. are not immediately written to the screen. A new function update() must be called to write the buffered text to the screen. The following functions remain non-buffered and are enacted immediately:

void setBrightness(int);
void setSplash();
void toggleSplash();
void blink();
void noBlink();
void cursor();
void noCursor();
void display();
void noDisplay();
void leftToRight();
void rightToLeft();
void autoscroll();
void noAutoscroll();

A description of the behavior of the buffered functions can be found in the header file.