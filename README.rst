ESP-IDF template app
====================

This is a template application to be used with `Espressif IoT Development Framework`_ (ESP-IDF). 

Please check ESP-IDF docs for getting started instructions.

Code in this repository is Copyright (C) 2016 Espressif Systems, licensed under the Apache License 2.0 as described in the file LICENSE.

.. _Espressif IoT Development Framework: https://github.com/espressif/esp-idf


ESP32 App
=========

Windows Setup
-------------

* Download and install MSYS2 for 32 bit (`msys2-i686-xxxxxxx.exe`)
* Add the following environment variables
   * `MSYS32_HOME` - `C:\path\to\msys32`
   * `IDF_PATH` - `C:\path\to\esp-idf`
   * `XTENSA_ESP32_HOME` - `%MSYS32_HOME%\opt\xtensa-esp32-elf`
* Extend the `PATH` variable by
   * `%MSYS32_HOME%\usr\bin`
   * `%MSYS32_HOME%\mingw32\bin`
   * `%XTENSA_ESP32_HOME%\bin`
* Clone esp-idf repository into `$IDF_PATH` (`git clone --recursive https://github.com/espressif/esp-idf.git`)
* Run `$IDF_PATH/tools/windows/windows_install_prerequisites.sh` from MSYS2 terminal
   
Now you can use `esp-idf` from Windows command prompt.

Eclipse Setup
-------------

Create a new Makefile Project or a Makefile Project from existing sources and select "Other toolchain" as your toolchain.

Add the following include directories to your project includes.
Always select "Add to all configurations" and "Add to all languages".

? `${IDF_PATH}\components\driver\include`
* `${IDF_PATH}\components\esp32\include`
* `${IDF_PATH}\components\freertos\include`
* `${IDF_PATH}\components\nvs_flash\include`
* `${XTENSA_ESP32_HOME}\xtensa-esp32-elf\include`

and others needed like

* `${IDF_PATH}\components\bt\include`

