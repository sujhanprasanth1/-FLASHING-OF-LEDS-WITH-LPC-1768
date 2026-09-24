# FLASHING-OF-LEDS-WITH-LPC-1768



# AIM: 
To interface and toggle the led with ARM LPC 1768 microprocessor           
           
# COMPONENTS REQUIRED:
##  HARDWARE:
ARM LPC1768
LED

## SOFTWARE:
KEIL MICRO VISION 4.0 IDE


# PROCEDURE:


⮚	Open the Keil software and select the New uvision project from Project Menu as shown below.

⮚	Browse to your project folder and provide the project name and click on save.

⮚	Once the project is saved a new pop up “Select Device for Target” opens, Select the 
controller (NXP: LPC1768) from NXP (founded by philips) and click on OK.

⮚	Select the controller (NXP: LPC1768) and click on OK.

⮚	As LPC1768 needs the startup code, click on Yes option to include the LPC17xx 
Startup file.

⮚	Create a new file by file → new to write the program.

⮚	Type the code.

⮚	After typing the code save the file as main.c eg. (abc.c).

⮚	Right click target and Add the suitable files to source group1 and header for the project.

⮚	Add the main.c along with system_LPC17xx.c.

⮚	Build the project and fix the compiler errors/warnings if any.

⮚	Code is compiled with no errors. The .bin file is still not generated.

⮚	Right Click on Target Options to select the option for generating .bin file.

⮚	Set IROM1 start address as 0x2000. Bootloader will be stored from 0x0000- 0x2000 so 
application should start from 0x2000

⮚	Write	the	command	to	generate	the .bin file	from
.axf file

Command: fromelf --bin projectname.axf --output filename.bin

⮚	in c/c++ → include paths → desktop (00-libfiles).

⮚	.Bin file is generated after a rebuild.

⮚	Check the project folder for the generated .Bin file.


# ADD FILES:

Target1:
Source group1:
Startuplpc17xx.s, main.c (t), delay.c (t), systemlpc17xx.c (t), gpio.c (t)
Header:
Delay.h, stdutils.h, gpioi.h

# PIN DIAGRAM :

 
<img width="381" height="402" alt="image" src="https://github.com/user-attachments/assets/85fd3b20-f3cb-4b6f-be02-3b2fd35bc716" />


# CIRCUIT DIAGRAM:


<img width="883" height="619" alt="image" src="https://github.com/user-attachments/assets/83d08e6b-8c42-4211-9f60-1f3f45e47258" />

 
# PROGRAM:
```
void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  delay(1000);

  digitalWrite(13, LOW);
  delay(1000);
}
```

# Output:


<img width="1797" height="890" alt="image" src="https://github.com/user-attachments/assets/c65f1902-9d30-401c-a4f5-cf0a2de5ffde" />

<img width="964" height="1280" alt="image" src="https://github.com/user-attachments/assets/f68c40d2-fa51-49c9-965f-53b9512f57bf" />



# Result:
The experiment on toggling an LED with the ARM LPC1768 microcontroller was successfully performed. The LED flashed ON and OFF at regular intervals as programmed, confirming correct interfacing and functioning of the GPIO operations. The code compiled without errors, and all hardware connections were verified to work as expected. The experiment demonstrated the basic use of GPIO for output and timing control using software delays.








