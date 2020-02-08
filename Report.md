Name: Jonathan Voss

EID: jmv3323

Team Number: F3

## Questions

1. Why does your program need a setup and a loop?

    The code needs the setup to initialize and set the initail values, and the loop contains the code for the program to run, repeatedly, forever.

2. What is the downside to putting all your code in a loop?

    The code is, well, ugly. Without modules, the code is difficult to read, dubug, and edit. Please, do not do this.

3. Why does your code need to be compiled?

    The compiler converts high level code into machine code which the computer can read and execute.

4. When lowering the frequency in procedure A, step 4, what is going wrong? Brainstorm some solutions. Dimmers exist in the real world. What is their solution?

    By slowing the frequency too much, the light begins to flash as the off time is so long it becomes visible. In the real world, dimmers operate at high enough 
	frequencies to be unnoticed by the human eye, while adjusting the percentage of "on" time to change the dimmness.

5. Why do you need to connect the logic analyzer ground to the ESP32 ground?

    Without this, the logic analizer will have no frame of reference for high and low, as voltage is merely a potential difference. by grounding the ESP32 to the 
	logic analyzer, they share a common 0V, and therefore the LA will be able to tell what is a 0 and what is a 1 as the ESP32 is sending them.

6. What is the difference between synchronous and asynchronous communication?

    Synchronus is contolled by a shared clock, and is used when everything is running at the same speed, while asynchronus is controlled by signals sent along the 
	communication medium- an external ready signal.

7. Profile of UART: Sent X bytes in Y time 

    13 bytes over 1.12 ms (11.607 B/ms)

8. Profile of SPI: Sent X bytes in Y time

    13 bytes over .348 ms (37.356 B/ms)

9. Why is SPI so much faster than UART?

    SPI makes use of more wires and is synchronized, meaning that the data can much faster and on its own line, seperate from start and stopp commands.

10. list one pro and one con of UART

Pro: very simple, able to interface with most devices with only one connection.
Con: slow and inneficient as compared to other methods.

11. list one pro and one con of SPI

Pro: Faster than the other forms
Con: requires more connections/hardware to run.

12. list one pro and one con of I2C

Pro: only needs two wires and can with them support multiple slaves
Con: only one device can talk at a time.

13. Why does I2C need external resistors to work?

Because the data lines are open drain, they require the external resistors to prevent them from sinking current and being unable to corecly output.

## Screenshots

Procedure A, step 1:
img/TimedBlink.png

Procedure A, step 4:
img/dimmer.png

Procedure B, UART:
img/UARTtest.png

Procedure B, SPI:
img/SPItest.png
