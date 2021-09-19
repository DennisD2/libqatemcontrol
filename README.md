libqatemcontrol
===============

libqatemcontrol implements the protocol used to connect to BlackMagic ATEM switches.

The protocol has been documented here:
http://skaarhoj.com/fileadmin/BMDPROTOCOL.html

Packet documentation:
http://atemuser.com/forums/atem-vision-mixers/developers/controlling-atem#comment-251

## To build the library
```
qmake
make
```

## To install
```
make install
```

## Test the installation
```shell
# Simple switcher UI test application
cd example/qatemswitcher
qmake
make
make install
./qatemswitcher
```

The library is installed to ```/usr/lib```. For OpenSuse Leap,
the correct local is ```/usr/lib64```. 
As a hack, this can be quickly fixed:
```shell
# As root
mv /usr/lib/libqatemcontrol* /usr/lib64/````
```

# File upload test application
```
cd example/qatemuploader
qmake
make
# Upload some file
./qatemuploader <ip_adress> <position> <filepath>
```

## Preparements
This application requires Qt5. Make sure that the correct ```qmake``` is in PATH.
On OpenSuse Leap, it is added this way:
```shell
PATH=/usr/lib64/qt5/bin:${PATH}
# Check version
qmake -v
```

