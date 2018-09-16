OTA write BIN
==========

This simple bash script will find compiled arduino sketch in /tmp directory and uploads it to ESP using espota.py program.

## Usage

Download this repository and run script using:   
`bash OTAwriteBIN`   
or   
`chmod +x OTAwriteBIN`   #make script executeable   
`./OTAwriteBIN`   #run script   

## Options

Options are same as for the espota.py. Script will make basic check which options are specified.   
 * `-h` or `--help` for help
 * `-f` or `--file=` for file, otherwise script will try find compiled arduino sketch in /tmp directory
 * `-i` or `--ip=` for set IP address of ESP or use **User settings variables**
 * `-p` or `--port=` for set PORT of ESP or use **User settings variables**

## User settings variables

Inside script you can find three user variables:   
 * `espota_path` - Uncomment this variable to set location of espota.py, otherwise the script will try find espota.py in your home directory.
 * `default_ip` - If you don't specify IP address using `-i` or `--ip=` option, the script will try use this variable.
 * `default_port` - If you don't specify PORT using `-p` or `--port=` option, the script will try use this variable.

## Example of usage

```
matrn@matrn-PC ~ $ ./OTAwriteBIN -i 192.168.1.100   
1) ESP_OTA.ino.bin   
Choose .bin file for OTA upload: 1   
Uploading: /tmp/arduino_build_397672/ESP_OTA.ino.bin   
Uploading..........................................................................................................................................................................   
matrn@matrn-PC ~ $
```  

## espota.py source

<a href="https://github.com/esp8266/Arduino/blob/master/tools/espota.py">https://github.com/esp8266/Arduino/blob/master/tools/espota.py</a>
