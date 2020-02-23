# ATTiny85-Playground
fun code for ATTiny85

For SpaceInvaders 
I used the ssd1306xled-library from https://github.com/Defragster/ssd1306xled
and adapted the code from https://www.tinyjoypad.com/tiny-joypad

I had to change the ports in the library header file (ssd1306xled.h)
using port PB4 and PB3 instead of PB2 and PB0--> see below!

// -----(+)--------------->	// Vcc,	Pin 1 on SSD1306 Board
// -----(-)--------------->	// GND,	Pin 2 on SSD1306 Board
#ifndef SSD1306_SCL

#define SSD1306_SCL		PB4 //PB2 // SCL,	Pin 3 on SSD1306 Board
#endif
#ifndef SSD1306_SDA
#define SSD1306_SDA		PB3 //PB0 // SDA,	Pin 4 on SSD1306 Board
#endif
#ifndef SSD1306_SA
#define SSD1306_SA		0x78	// Slave address
#endif

// ---------------------
