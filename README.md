# Sigrok Decoder for Infineon SWI

## Instructions

First install sigrok, either:
```shell
sudo apt-get install sigrok
```
or download [PulseView](https://sigrok.org/wiki/Downloads) directly

Next clone this directory:
```shell
git clone https://github.com/JonasAlaif/sigrok-infineon-swi.git
cd sigrok-infineon-swi/
```

Then to run you can use:
```shell
SIGROKDECODE_DIR=$(pwd)/decoders pulseview -i capture.sr
```
If you downloaded the PulseView AppImage then replace `pulseview` above. The `SIGROKDECODE_DIR` var is needed to add the custom decoder.

Inside PulseView click the add protocol decoder button (rightmost) and select `SWI`. This will add a new channel `SWI`, below `DIN 0 (SWI)` and `DIN 4 (UART)`.

The captured `DIN 0 (SWI)` channel should now be decoded here. Zoom in with scroll to view at different levels. If you need to change the channel being decoded, click on `SWI` and select a different `SWI channel`.
