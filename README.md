# checkserial - a simple program to check pins on a serial interface

## Installation

In order to use this program you will need the serial module from
Python.  Install the module first:

pip install pyserial

## Usage

By default the program reads from /dev/cuau1 which is the second
serial port on a FreeBSD based system.  The -p command line switch
allows the user to change the port from which the program reads:

```
sudo checkserial -p /dev/cuau0
```

Note that on most systems reading from the serial port requires super
user permissions.

The checkserial program is looking to see if pins 6 and 7 are shorted
then the program prints an "OK" message but if pins 6 and 8 are
shorted is prints "FAULT"  If neither of these conditions is met the
program exist with no output.

