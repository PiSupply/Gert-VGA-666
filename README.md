![Alt text](https://user-images.githubusercontent.com/1878314/73882099-6448c000-4859-11ea-88d7-2363b44d9596.png)
# Gert-VGA-666
Resources for Gert VGA 666

## OS configuration
Note that for the Gert VGA 666 to work correctly you will need **SPI and I2C to be disabled**.

These instructions have been specifically provided for Raspbian but should apply to the majority of OSs.
```bash
sudo nano /boot/config.txt
```
Add these lines at the bottom of the file
```
dtoverlay=vga666
enable_dpi_lcd=1
display_default_lcd=1
```
You also need to specify your screen resolution. After the lines you added above you will also have to then add one of the following configurations:
```
#For 1920x1080 60Hz
dpi_group=2
dpi_mode=82
#For 1280x1024 60Hz
dpi_group=2
dpi_mode=35
#For 1024x768 60Hz
dpi_group=2
dpi_mode=16
#For 800x600 60Hz
dpi_group=2
dpi_mode=9
```
If the resolution that you are looking for is not among these then you can [check this link](https://www.raspberrypi.org/documentation/configuration/config-txt/video.md).

## Further information
Please [check this article](https://www.pi-supply.com/make/gert-vga-666-assembly-tips-and-gotchas/) on our website for:
* Assembly guide
* Configuration settings
* Pinout
* FAQ

The full design files, schematics and other details are [available on GitHub](https://github.com/fenlogic/vga666).
