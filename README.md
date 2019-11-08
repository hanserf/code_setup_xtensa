# VScode c_cpp_properties development ESP32 Xtensa Debian Ubuntu Linux Environment.

To make life easier, use this to get full intellisense for ESP32 development.
Assumes Xtensa and IDF has been installed according to instructions by the "official" esp32 guide

#### Environment setup:

``` bash
nano ~/.bashrc
#Add this to your config
export XTENSA_PATH=$HOME/workarea-esp32/xtensa-esp32-elf
export PATH="$XTENSA_PATH/bin:$PATH"
export IDF_PATH="~/workarea-esp32/esp-idf"
#Ctrl+x to save and exit. 'y' then enter save
#Reload your bash environment:
source ~/.bashrc
#Test Variables:
printenv PATH
```

__This should succeed without error.__

# Start a project:
``` bash
mkdir -p esp_dev && cd esp_dev
cp -r $IDF_PATH/examples/get-started/hello_world .
code .
```
press ctrl + shift + p to open command palette.
C/C++ Edit configurations (JSON) to autogenerate a config in hidden project folder `.vscode` .
replace that file with this and you are good to go
