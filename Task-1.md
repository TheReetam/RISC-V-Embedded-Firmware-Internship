# What is a firmware library?
- #### Firmware is a specific type of software that sit into a hardware device's non-volatile memory (like Flash or ROM). Its primary purpose is to provide low-level control for that specific piece of hardware. When the device is turned on, the firmware is the first code to run. It "wakes up" the hardware components like clocks, memory, and pins. It is Hardware specific It is Hardware specific, if the hardware is changed , the firmware must be rewritten.

# Why APIs are important in embedded systems?
- #### In embedded systems, an API (Application Programming Interface) acts as the formal bridge between the high-level application logic and the low-level hardware-specific firmware. Without an API, an application developer would need to understand the electrical details of every transistor and register on a chip just to blink a light. For example:- Hardware Team: Can work on the gpio.c implementation to make it efficient for the specific chip. Software Team: Can write the main.c logic using the gpio.h definitions, even before the physical hardware is finished.

# What was understood from the lab code?
- In vsdquadron-mini-core project, code is split into these three file types to keep it organized, reusable, and easy to debug.
- **.h Files** - A header file tells the rest of the program what functions and constants exist, without showing how they work. It’s like a menu at a restaurant: you see what you can order, but you don't see the recipe or the kitchen logic.
- **.c Files** - A Source file is where the actual work happens. In gpio.c, it is defining the logic for the functions that is promised in the header.
- **main.c** - This is the entry point of your program. The computer always looks for the int main() function to start execution.
