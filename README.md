# contest-irc

Author: Clayton Smith  
Email: <argilo@gmail.com>

The intent of this project is to turn a laptop computer into a WiFi-accessible
IRC server with a web interface. This can be used to make contacts on the 2.4
GHz amateur band in contests such as the
[ARRL June VHF Contest](http://www.arrl.org/june-vhf).

## Building a bootable USB flash drive

Install the dependencies:

* qemu-utils
* qemu-system-x86

Run the following:
```
./create.sh
```
This will generate a disk image (`contest-irc.img`), which can be flashed to a USB
drive using `dd`.

Optionally, create a VirtualBox VDI:
```
VBoxManage convertfromraw --format VDI contest-irc.img contest-irc.vdi
```

## Usage

Boot from the flash drive and double click the "Contest IRC" icon on the
desktop. Enter your call sign in the "Nickname" field and click "Start..." to
join the chat room.

From another laptop or smartphone, connect to the VE3WCC access point. Then
launch a web browser and visit http://10.42.0.1:7778/. Enter your call sign in
the "Nickname" field and click "Start..." to join the chat room.

## License

Copyright 2017-2023 Clayton Smith

This file is part of contest-irc

contest-irc is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3, or (at your option)
any later version.

contest-irc is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with contest-irc; see the file COPYING.  If not, write to
the Free Software Foundation, Inc., 51 Franklin Street,
Boston, MA 02110-1301, USA.
