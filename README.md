intellifix
==========

1. Download [usbreset.c](http://cpansearch.perl.org/src/DPAVLIN/Biblio-RFID-0.03/examples/usbreset.c)
2. Compile & put on PATH
3. `alias intellifix="bus=$(lsusb | grep IntelliMouse | grep -Eo '[0-9]{3}' | head -n2 | tr '\n' '/');bus=$(echo \"${bus%?}\");bus=$(echo \"/dev/bus/usb/$bus\");sudo usbreset $bus"`
