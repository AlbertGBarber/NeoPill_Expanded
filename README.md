# NeoPill
An expanded version of the Blue Pill Neopixel Emulator. Includes new options for LED disk and custom layouts. 

Otherwise is the same as the original code. 

To build with STM32CubeMX (6.1.1), open bluepill_neoemu_clk.ioc, generate code in a selected folder. 
Locate and copy over the 3 files main.c, usbd_cdc_if.c, usbd_cdc_if.h .
Build with selected environment (originally used Keil uVision 5.26.)
Flash into a Blue Pill.
Follow instructions at https://hackaday.io/project/179916-neopill

Or use STM32CubeProgrammer v2.6.0 to flash the Hex file.

Note that for ESP8266's (and possibly ESP32's), you may need to add a single physical LED between the ESP and the Bluepill to help filter the pixel data. 

Python code for the PC side is 'stripsym.py', and four YAML config files ledstrip.yaml, ledmatrix.yaml, leddisk.yaml, and ledcustom.yaml.

Command Lines:

  python stripsim.py ledstrip.yaml

  python stripsim.py ledmatrix.yaml

  python stripsim.py leddisk.yaml

  python stripsim.py ledcustom.yaml
