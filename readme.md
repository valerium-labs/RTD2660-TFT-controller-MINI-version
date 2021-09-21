LCD-controller "Narodniy" mini-version. 
valerium@rambler.ru, 2021

Yet another implementation of the universal TFT-display controller based in RTD2660 chip.
Minimalistic and compact, intended specially for retrocomputers.

Fully functional prototype is VS-TY2662-V1 device, it is based on well-known PCB800099 board and has 
a lot of input interfaces (HDMI, VGA, 2xA/V etc). This board is excellent for desktop monitors, but 
not the best solution for embedding into portable devices because of its size. 

Mini-version is small (50x59mm) and flat enough to be built into the tablet case to make it a small and 
compact display for retrocomputer like ZX Spectrum and so on. Its functionality is reduced to only one 
VGA input, LVDS output and the fimware supports only three modes (31,2Khz/60Hz, 31,2kHz/50Hz and 
15,6kHz/50Hz of horizontal/vertical sync frequencies). 
Besides analog VGA input the board also has a digital RGBI-HS-VS-input for Speccy-clones with a logical 
level signals to reduce noise and color distirtion.
5-key keyboard is optional and used only for testing purposes; it is not nescessary to built it into 
tablet case - the controller turns screen on when the power is on and input signal sync-freqs are in 
supported range.

Project includes schematics, gerber files for board production, sample *special* firmwares for several 
LVDS-panels and the configuration tool for modding the firmware to make your panels work and the adjust 
it to videomodes of your retrocomputer.

The best and simplest way for flashing the controller is in-system programming using Remizov's programming 
tool (see the link below - this package is NOT included into the project) which can be built on Arduino 
boards (atmega328p or 32u4-based) in 5 minutes.
First you need to flash Arduino board with the appropriate firmware (any tool at your choice - avrdude, 
Khazama AVR Programmer and so on), connect Arduino's A4, A5 and GND pins to SDA, SCL and GND on controller, 
start the program "RTD266X Arduino Burning Serial Flash Memory 2.3.exe" and feed it with the RTD2660 firmware.



Links:
     
Forum topic on "Narodniy" TFT-controller (Russian only)
https://zx-pk.ru/threads/32683-vyvod-izobrazheniya-retrokompyutera-na-tft-matritsu-(-quot-narodnyj-kontroller-quot-).html

Remizov's arduino programming tool - excellent solution for flashing RTD2660 devices (Russian only)
http://www.pccar.ru/showthread.php?p=400231#post400231

Final version 2.3 of Remizov's progtool

http://www.pccar.ru/showpost.php?p=415519&postcount=34
https://disk.yandex.ru/d/jB8rdftST0etYw
